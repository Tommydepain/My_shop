<!-- <template>
    <router-link to="/admin" >Admin</router-link>
    </template>
id="login-button"ms-hide-element="true" href="" class="button admin w-button " -->

<template>
  <!-- html -->
  <html lang="en">
  <head>
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">
      <link rel="stylesheet"
            href="https://fonts.googleapis.com/css?family=Roboto">
            <meta name="theme-color" content="#0287f7" />
            <meta name="viewport" content="width=device-width, initial-scale=1" />
      <link rel="stylesheet" type="text/css" href="rush.css">
  </head>
  <body>
  <div class="container-fluid">
      <header>
              <nav class="navbar navbar-expand-lg">
                  <img src="http://daweiphotography.free.fr/Images/Logo.png" alt="logo site"/>
                  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                      <span class="navbar-toggler-icon"></span>
                  </button>
                  <div class="collapse navbar-collapse" id="navbarSupportedContent">
                      <ul class="navbar-nav mr-auto">
                          <li class="nav-item active">
                            <router-link to="/Admin"  ms-hide-element="true" href="" class="button logout login w-button" >Admin</router-link>                            
                          </li>
                          <li class="nav-item active">
                            <button onclick="window.location.href='http://localhost:5174/';">Product</button>                            
                          </li>
                      </ul>
                      <a href="#">
                          <img src="http://daweiphotography.free.fr/Images/Cart%20Button.png" alt="caddie" />
                      </a>
                      <button onclick="window.location.href = 'http://localhost:5174/';">Login</button>                            
                  </div>
              </nav>
      </header>
      <div>
          <div class="researchbar" id="search_div">
            <img id="search_img" src="http://daweiphotography.free.fr/Images/Search.png" alt="Loupe">
              <div class="col-8">
                  <form class="form-group">
                      <input id="exampleFormControlInput1" type="text" placeholder="Search" class="form-control form-control-underlined">
        <div class="dropdown-menu" aria-labelledby="navbarDropdown" >
  </div>
          </form>
             </div>
            </div>
          </div>
          </div>
  <main>
    <section>
      <article><img src="http://daweiphotography.free.fr/Images/img1.jpg" alt="Lounge">
               <h6>Coombes</h6>
               <p class="price">$2,600</p>
               <p class="s_titre">LOUNGE</p>
               <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
               <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
               <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
               <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
               <img class="stars" src="http://daweiphotography.free.fr/Images/Star.png" alt="étoile vide">
               <img class="cad" src ="http://daweiphotography.free.fr/Images/Cart%20ButtonPLUS.png" alt="caddie avec un + à l'interieur">
      </article>
      <article><img src="http://daweiphotography.free.fr/Images/img2.jpg" alt="Table & Chair">
              <h6>Keeves Set</h6>
              <p class="price">$590</p>
              <p class="s_titre">TABLE & CHAIRS</p>
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star.png" alt="étoile vide">
              <img class="cad" src ="http://daweiphotography.free.fr/Images/Cart%20ButtonPLUS.png" alt="caddie avec un + à l'interieur">
      </article>
      <article><img src="http://daweiphotography.free.fr/Images/img3.jpg" alt="Armchair">
              <h6>Nillè</h6>
              <p class="price">$950</p>
              <p class="s_titre">ARMCHAIR</p>
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="cad" src ="http://daweiphotography.free.fr/Images/Cart%20ButtonPLUS.png" alt="caddie avec un + à l'interieur">
      </article>
      <article><img src="http://daweiphotography.free.fr/Images/img4.jpg" alt="SIDE TABLE">
              <h6>Blanko</h6>
              <p class="price"> $90</p>
              <p class="s_titre">SIDE TABLE</p>
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star%20-%20On.png" alt="étoile remplie">
              <img class="stars" src="http://daweiphotography.free.fr/Images/Star.png" alt="étoile vide">
              <img class="cad" src ="http://daweiphotography.free.fr/Images/Cart%20ButtonPLUS.png" alt="caddie avec un + à l'interieur">
      </article>
  </section>
  </main>
  <footer>
    <ul class="number-list">
      <li><button onclick="window.location.href = 'http://localhost:5173/'" class="btn1">1</button></li>
      <li><button class="btn">2</button></li>
      <li><button class="btn">3</button></li>
      <li><button class="btn">4</button></li>
      <li><button class="btn">></button></li>
  </ul>
  </footer>
          </body>
          </html>
  </template>
  <style scoped>
  section{
  display:grid;
  grid-template-columns: repeat (auto-fit, minmax(200px, 1fr));
  }
  arrticle{
    height: 200px;
  }
  .researchbar,
  .barre {
     display: flex;
      width: 1400px;
  }
  .loupe {
      height: 40px;
      width: 40px;
  }
  /*FIN NAVBAR*/
  button {
    background-color: rgb(255, 255, 255);
  }
  a {
    color: black;
  }
  section {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    padding-left: 5vh;
    gap: 10px;
  }
  article {
    height: 450px;
    width: 340px;
    line-height: 5px;
    margin-top: 50px;
  }
  article li {
    list-style-type: none;
    text-decoration: none;
    border-bottom: 1px solid rgb(212, 212, 212);
    line-height: 50px;
    margin-bottom: 14px;
  }
  article img {
    height: 250px;
    width: 250px;
  }
  article li img {
    height: 15px;
    width: 15px;
    margin-left: 24.5vh;
  }
  .stars {
    height: 10px;
    width: 10px;
  }
  .price {
    float: right;
    margin-right: 100px;
  }
  .s_titre {
    font-size: 13px;
    padding-bottom: 13px;
    color: #a9a9a9;
  }
  .cad {
    height: 25px;
    width: 25px;
    margin-left: 150px;
  }
  .espace {
    line-height: 30px;
  }
  ul {
    list-style-type: none;
  }
  footer {
      display: flex;   
  }
  footer {
     font-size: 20px;
     margin-left: 30px;
      text-align: center;
      padding: 10px;
  }
  .number-list li {
      display: inline;
      margin-right: 20px; 
  }
  footer {
      display: flex;
     font-size: 20px;
     margin-left: 30px;
      text-align: center;
      padding: 10px;
  }
  .number-list {
      list-style: none;
      padding: 0;
  }
  .number-list li {
      display: inline;
      margin-right: 40px;
  }
  .btn1 {
  background-color: black;
  color: white;
  padding: 6px 12px;
  font-size: 16px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  
  }
  .button{
      background-color: #ffffff; 
      color: #000000; 
      padding: 10px 20px; 
      border: none; 
      border-radius: 5px; 
      cursor: pointer;
      transition: background-color 0.3s ease;
  }
  .number-list :hover {
      background-color: #000000; 
      color:white ;
    }
  </style>