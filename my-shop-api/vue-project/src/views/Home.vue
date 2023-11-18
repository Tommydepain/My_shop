<template>
  <div>
    <header class="bg-blue-500 p-4">
      <nav class="container mx-auto flex items-center justify-between">
        <img src="@/assets/logooooo.png" alt="Logo" class="w-16" />
        <div class="flex items-center space-x-4">
          <router-link to="/Admin" class="text-white">Admin</router-link>
          <a href="#" class="text-white">
            <img src="http://daweiphotography.free.fr/Images/Cart%20Button.png" alt="caddie" class="w-6" />
          </a>
          <router-link to="/Login" class="text-white">Login</router-link>
        </div>
      </nav>
      <div class="researchbar bg-gray-200 p-4">
        <img src="http://daweiphotography.free.fr/Images/Search.png" alt="Loupe" class="w-6" />
        <form class="form-group">
          <input id="exampleFormControlInput1" type="text" placeholder="Search" class="form-control form-control-underlined">
          <div class="dropdown-menu" aria-labelledby="navbarDropdown"></div>
        </form>
      </div>
    </header>

    <main class="container mx-auto mt-8">
      <section class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-4">
        <article class="border p-4">
          <img src="http://daweiphotography.free.fr/Images/img1.jpg" alt="Lounge" class="w-full h-48 object-cover mb-4">
          <h6 class="text-xl font-semibold">Coombes</h6>
          <p class="text-gray-700">$2,600</p>
          <p class="text-gray-500">LOUNGE</p>
          <div class="flex">
            <img src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie" class="w-4 h-4">
            <img src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie" class="w-4 h-4">
            <img src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie" class="w-4 h-4">
            <img src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie" class="w-4 h-4">
            <img src="http://daweiphotography.free.fr/Images/Star.png" alt="étoile vide" class="w-4 h-4">
          </div>
          <img src="http://daweiphotography.free.fr/Images/Cart%20ButtonPLUS.png" alt="caddie avec un + à l'interieur" class="w-6 h-6 mt-2">
        </article>
      </section>
    </main>

    <footer class="bg-gray-200 p-4 mt-8">
      <ul class="flex items-center space-x-4">
        <li><button class="btn1">1</button></li>
        <li><button  class="btn">2</button></li>
        <li><button  class="btn">3</button></li>
        <li><button  class="btn">4</button></li>
        <li><button  class="btn">&gt;</button></li>
      </ul>
    </footer>
  </div>
</template>

<script>
</script>

<style scoped>
</style>
