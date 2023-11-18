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
  
            this.$router.push('/');
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
              'Authorization': 'Bearer eyJ0eXAiOiJKV1QiLCJhbGciOiJSUzI1NiJ9.eyJpYXQiOjE3MDAzMjcxMzUsImV4cCI6MTcwMDMzMDczNSwicm9sZXMiOlsiUk9MRV9BRE1JTiIsIlJPTEVfVVNFUiJdLCJ1c2VybmFtZSI6InRvbW15LmplYW4tamVhbkBlcGl0ZWNoLmRpZ2l0YWwifQ.CXskLNaY4If7GfvFJfqiXCaXTVIfkTWRbayH9jH7mMUZ8mI1DqOO_9dZNuGw0kQhcyMVndVEjjY7C0IPLkNIbuNvNrWaaF9ag7G3fQfYsH7ByDnl1QAS43IaMdLOKc86JH_TKPq_3QGqHZMQv5skFDSKVDvgnMAUD_vnohVamtbfceTJXa0dnsTvrpQiPPQG0jM6Efd20wJTGw895TV9lOb7te44i1oycZUoJJAk4NqqwglWnEngn2Opoauod2IRmE0AnpuTMvcfyRGmDAG_3Yybr_usPGeJFgbpivqPtEc3L36eoXVbLXKZJ6tz2YdVNtchWrTUSmHkNktnffkGUg',
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
  
  
