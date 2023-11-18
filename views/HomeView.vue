
@tailwind base;
@tailwind components;
@tailwind utilities;
<template>
  <!-- html -->
  <html lang="en">
  <head>
      <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css">
      <meta name="theme-color" content="#0287f7" />
      <meta name="viewport" content="width=device-width, initial-scale=1" />
  </head>
  <body class="font-roboto">
    <div class="container-fluid">
      <header>
        <nav class="navbar navbar-expand-lg">
          <img src="@/assets/logooooo.png" alt="Logo" class="logo" />
          <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
              <li class="nav-item active">
                <RouterLink to='/Admin' class="button" >Admin</RouterLink>
              </li>
              <li class="nav-item active">
                <router-link to="/Product" class="buton" >Product</router-link>                             
              </li>
            </ul>
            <a href="#">
              <img src="http://daweiphotography.free.fr/Images/Cart%20Button.png" alt="caddie" />
            </a>
            <router-link to="/Login" class="button" >Login</router-link>                             
          </div>
        </nav>
      </header>
      <div>
        <div class="researchbar" id="search_div">
          <img id="search_img" src="http://daweiphotography.free.fr/Images/Search.png" alt="Loupe">
          <div class="col-8">
            <form class="form-group">
              <input id="exampleFormControlInput1" type="text" placeholder="Search" class="form-control form-control-underlined">
              <div class="dropdown-menu" aria-labelledby="navbarDropdown"></div>
            </form>
          </div>
        </div>
      </div>
      <main>
        <section class="grid grid-cols-auto-fit gap-10">
          <article class="h-450 w-340 line-height[5px] mt-50">
            <img src="http://daweiphotography.free.fr/Images/img1.jpg" alt="Lounge">
            <bouton>
              <h6>Coombes</h6>
            </bouton>
            <p class="price">$2,600</p>
            <p class="s_titre">LOUNGE</p>
            <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
            <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
            <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
            <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
            <img class="stars" src="http://daweiphotography.free.fr/Images/Star.png" alt="étoile vide">
            <img class="cad" src ="http://daweiphotography.free.fr/Images/Cart%20ButtonPLUS.png" alt="caddie avec un + à l'interieur">
          </article>
          <!-- Repeat similar structure for other articles -->
        </section>
      </main>
      <footer class="flex items-center justify-center text-20 ml-30 px-10">
        <ul class="number-list">
          <li><button onclick="window.location.href = 'http://localhost:5173/'" class="btn1">1</button></li>
          <li><button class="btn">2</button></li>
          <li><button class="btn">3</button></li>
          <li><button class="btn">4</button></li>
          <li><button class="btn">></button></li>
        </ul>
      </footer>
    </div>
  </body>
  </html>
</template>
