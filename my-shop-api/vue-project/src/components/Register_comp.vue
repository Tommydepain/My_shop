<template>
    <section>
        <div class="mx-auto flex w-full max-w-sm flex-col gap-6 mt-48">
            <div class="flex flex-col items-center">
                <h1 class="text-3xl font-semibold"> Register </h1>
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
                    <label class="form-label">Comfirm Password</label>
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
                    </div>
                </div>
                <div class="form-field pt-5">
                    <div class="form-control justify-between">
                        <button class="btn btn-primary w-full"> Register </button>
                    </div>
                </div>

                <div class="form-field">
                    <div class="form-control justify-center">
                        <router-link to="/Login"  class="link link-underline-hover link-primary text-sm">Don't have an account yet? Sign in.</router-link>
                        
                    </div>
                </div>
                
            </div>
        </div>
    </section>
</template>

<script>
</script>

<style>
</style>