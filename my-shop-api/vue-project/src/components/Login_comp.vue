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

                    <input placeholder="Type here" type="email" class="input max-w-full" />
                    <label class="form-label">
                        <span class="form-label-alt">Please enter a valid email.</span>
                    </label>
                </div>
                <div class="form-field">
                    <label class="form-label">Password</label>
                    <div class="form-control">
                        <input placeholder="Type here" type="password" class="input max-w-full" />
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
import axios from 'axios';

export default {
  methods: {
    async signIn() {
      try {
        const email = this.$data.email; // Remplacez par la variable où vous stockez l'e-mail.
        const password = this.$data.password; // Remplacez par la variable où vous stockez le mot de passe.

        // Effectuer la requête POST avec Axios
        const response = await axios.post('http://localhost:5174/Login', {
          email: email,
          password: password,
        });

        // Vérifier si le statut de la réponse est 200
        if (response.status === 200) {
          // Gérer la réussite de la connexion, par exemple, rediriger l'utilisateur
          // vers une autre page ou stocker le jeton d'authentification.
          console.log('Login successful!');
        } else {
          // Gérer les erreurs de connexion, par exemple, afficher un message d'erreur.
          console.error('Login failed:', response.statusText);
        }
      } catch (error) {
        console.error('An error occurred during login:', error);
      }
    },
  },
};  
</script>

<style>

</style>