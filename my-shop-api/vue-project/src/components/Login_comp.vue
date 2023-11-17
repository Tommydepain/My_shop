<template>
    <section>
      <div class="m-auto flex w-full max-w-sm flex-col gap-6 mt-48">
        <div class="flex flex-col items-center">
          <h1 class="text-3xl font-semibold">Sign in</h1>
          <p class="text-sm">Sign in to access your account</p>
        </div>
        <div class="form-group">
          <div class="form-field">
            <label class="form-label">Email address</label>
            <input v-model="email" placeholder="Type here" type="email" class="input max-w-full" />
            <label class="form-label">
              <span class="form-label-alt">Please enter a valid email.</span>
            </label>
          </div>
          <div class="form-field">
            <label class="form-label">Password</label>
            <div class="form-control">
              <input v-model="password" placeholder="Type here" type="password" class="input max-w-full" />
            </div>
          </div>
          <div class="form-field">
            <div class="form-control justify-between">
              <div class="flex gap-2">
                <input type="checkbox" class="checkbox" />
                <a href="#">Remember me</a>
              </div>
              <label class="form-label">
                <a class="link link-underline-hover link-primary text-sm">Forgot your password?</a>
              </label>
            </div>
          </div>
          <div class="form-field pt-5">
            <div class="form-control justify-between">
              <button @click="signIn" class="btn btn-primary w-full">Sign in</button>
            </div>
          </div>
          <div class="form-field">
            <div class="form-control justify-center">
              <router-link to="/Register" class="link link-underline-hover link-primary text-sm">Don't have an account yet? Register.</router-link>
            </div>
          </div>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        email: '',
        password: '',
        users: [],
      };
    },
    methods: {
      async signIn() {
        try {
          await this.getUsers();
          const user = this.users.find(u => u.email === this.email);
          console.log(user)
  
          if (user) {
            console.log('Login successful!');
  
            this.$router.push('/Register');
          } else {
            console.error('User not found or invalid credentials.');
          }
        } catch (error) {
          console.error('An error occurred during login:', error);
        }
      },
      async getUsers() {
        try {
          const response = await fetch('http://localhost/api/users/', {
            method: 'GET',
            headers: {
              'Content-Type': 'application/json',
              'Authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpYXQiOjE3MDAyMzgwMDAsImV4cCI6MTcwMDI0MTYwMCwicm9sZXMiOlsiUk9MRV9BRE1JTiIsIlJPTEVfVVNFUiJdLCJ1c2VybmFtZSI6InRvbW15LmplYW4tamVhbkBlcGl0ZWNoLmRpZ2l0YWwifQ.o2UVALRepboGITm0RjgGl2mPcmrBEFDg382b43NbZ4UpTsXS2qDDpwe3deHLne7MmPflYnLyR69QWsdpvMX4BL_DbE9P8Y4KcIgJG8NYepTufpDGaUqudjVOkxg3j2R7cazigjz-Zx3zQ9lhilSgJASny_xAb047Nl0iaC4jFUaM2rTygsBsYJIR32URzT7Xzwk4hAJQuvNBK8EBIOHxrVg36FdvMGdJhWSDQuJ19iRwqHAD8eU9EGCkvKqMRwI2-HMZ-vb9Hw1gpkUg1izGIaV2DB8vFyYRS4_EgwwXJrMF4sXF6uxl5ZLqHykNNaHxNW8rHxlCh7bxMOsNlLiP7A',
            },
          });
  
          if (response.ok) {
            const responseData = await response.json();
            this.users = responseData['hydra:member'];
          } else {
            console.error('Error:', response.statusText);
          }
        } catch (error) {
          console.error('An error occurred:', error);
        }
      },
    },
  };
  </script>
  
  <style>
  
  </style>
  
  
