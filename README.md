# Film-website
A website in which we can view or download films.





<!DOCTYPE html>
<html lang="en">
 
 

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

 <style>
   body {
    font-size: 15px;
  }

  button {
    background: #ffc600;
    border: 0;
    padding: 10px 20px;
  }

  img {
    max-width: 100%;
  }



  .wrapper {
    display: grid;
    grid-gap: 20px;
    
  }

  .top {
    display: grid;
    grid-gap: 10px;
    grid-template-areas:
    
      "hero hero cta1"
      "hero hero cta2"
  }

  .hero {
    grid-area: hero;
    min-height: 380px;
    background: white url(ak/1.jpg);
    
    
    
    background-size: 79%;
    background-position: 100%;
    padding: 80px;
    display: flex;
    
    flex-direction: column;
    align-items: start;
    justify-content: center;
  }

  .hero > * {
    background: var(--yellow);
    padding: 6px;
    backface-visibility: hidden;
    
  }

  .cta {
    background: var(--yellow);
    

    display: grid;
    align-items: center;
    justify-items: center;
    align-content: center;
    
  }

  .cta p {
    margin: 0;
  }

  .cta1 {
    grid-area: cta1;
    background-image: url(ak/22.jpg);
    background-size: 65%;
    
    
    
    
  }

  .cta1 > * {
    background: var(--yellow);
    padding: 1px;
    
    
  }

  .cta2 {
    grid-area: cta2;
    background-image: url(ak/44.jpg);
    background-size: 122%;
    align-items: center;
  }

  .cta2 > * {
    background: var(--yellow);
    padding: 1px;
    
    
  }


  /* Navigation */

  .menu ul {
    display: grid;
    grid-gap: 10px;
    padding: 0;
    list-style: none;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
  }

  .menu a {
    background: var(--yellow);
    display: block;
    text-decoration: none;
    padding: 10px;
    text-align: center;
    color: var(--black);
    text-transform: uppercase;
    font-size: 20px;
  }

  [aria-controls="menu-list"] {
    display: none;
  }

  /* Features! */

  .features {
    display: grid;
    grid-gap: 20px;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }

  .feature {
    background-image: url(4.jpg);
    align-items: center;
    padding: 10px;
    border: 1px solid white;
    text-align: center;
    box-shadow: 0 0 4px  rgba(0,0,0,0.1);
    
  }

  .feature > * {
    background: var(--yellow);
    padding: 1px;
    min-width: 0%;
    
    
  }


  .feature2 {
    background-image: url(5.jpg);
    padding: 10px;
    border: 1px solid white;
    text-align: center;
    box-shadow: 0 0 4px  rgba(0,0,0,0.1);
  }

  .feature2 > * {
    background: var(--yellow);
    padding: 1px;
    
    
    
  }

  .feature3 {
    background-image: url(8.jpg);
    
    padding: 10px;
    border: 1px solid rgb(255, 255, 255);
    text-align: center;
    box-shadow: 0 0 4px  rgba(0,0,0,0.1);
  }

  .feature3 > * {
    background: var(--yellow);
    padding: 1px;
    
    
    
  }
  

  .feature4 {
    background-image: url(7.jpg);
    padding: 10px;
    border: 1px solid white;
    text-align: center;
    box-shadow: 0 0 4px  rgba(0,0,0,0.1);
  }

  .feature4 > * {
    background: var(--yellow);
    padding: 1px;
    
    
  }


  .feature .icon {
    font-size: 50px;
  }
  .feature p {
    color: rgba(0,0,0,0.5);
  }

  /* About Section */

  .about {
    background: white;
    padding:50px;
    display: grid;
    grid-template-columns: 400px 1fr;
    align-items: center;
  }

  .about2 {
    background: white;
    padding:50px;
    display: grid;
    grid-template-columns: 400px 1fr;
    align-items: center;
  }


  /* Gallery! */

  .gallery {
    display: grid;
    grid-gap: 20px;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  }

  .gallery img {
    width: 100%;
  }

  .gallery h2 {
    grid-column: 1 / -1;
    display: grid;
    grid-template-columns: 1fr auto 1fr;
    grid-gap: 20px;
    align-items: center;
  }

  .gallery h2:before, .gallery h2:after {
    display: block;
    content: '';
    height: 10px;
    background: linear-gradient(to var(--direction, left), var(--yellow), transparent);
  }

  .gallery h2:after {
    --direction: right;
  }

  @media (max-width: 1000px) {
    .menu {
      perspective: 800px;
    }
    [aria-controls="menu-list"] {
      display: block;
      margin-bottom: 10px;
    }

    .menu ul {
      max-height: 0;
      overflow: hidden;
      transform: rotateX(90deg);
      transition: all 0.5s;
    }

    [aria-expanded="true"] ~ ul {
      display: grid;
      max-height: 500px;s
      transform: rotateX(0);
    }

    [aria-expanded="false"] .close {
      display: none;
    }

    [aria-expanded="true"] .close {
      display: inline-block;
    }

    [aria-expanded="true"] .open {
      display: none;
    }

  }

  @media (max-width: 700px) {
    .top {
      grid-template-areas:
        "hero hero"
        "cta1 cta2"
    }
    /* About */
    .about {
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 500px) {
    .top {
      grid-template-areas:
        "hero"
        "cta1"
        "cta2"
    }
  }
  </style>

  <style>
    /*
  Oh Hello!
  These are some base styles so that our tutorial looks good.
  Let's go through the important bits real quick
*/
:root {
    --yellow: #ffc600;
    --black: #272727;
  }

  html {
    /* border-box box model allows us to add padding and border to our elements without increasing their size */
    box-sizing: border-box;
    /* A system font stack so things load nice and quick! */
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica,
      Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
    font-weight: 900;
    font-size: 10px;
    color: var(--black);
    text-shadow: 0 2px 0 rgba(0, 0, 0, 0.07);
  }

  /*
    WAT IS THIS?!
    We inherit box-sizing: border-box; from our <html> selector
    Apparently this is a bit better than applying box-sizing: border-box; directly to the * selector
  */
  *,
  *:before,
  *:after {
    box-sizing: inherit;
  }

  body {
    background-image: url("./images/topography.svg"),
      linear-gradient(110deg, #f93d66, #6d47d9);
    background-size: 340px, auto;
    min-height: calc(100vh - 100px);
    margin: 50px;
    /* background: white; */
    background-attachment: fixed;
    letter-spacing: -1px;
  }

  h1,
  h2,
  h3,
  h4,
  h5,
  h6 {
    margin: 0 0 5px 0;
  }
  /* Each item in our grid will contain numbers */
  .item {
    /* We center the contents of these items. You can also do this with flexbox too! */
    display: grid;
    justify-content: center;
    align-items: center;
    border: 5px solid rgba(0, 0, 0, 0.03);
    border-radius: 3px;
    font-size: 35px;
    background-color: var(--yellow); /* best colour */
  }

  .item p {
    margin: 0 0 5px 0;
  }
  </style>
  <title>ABFilms - By Akshay</title>
</head>

<body>

  <h1 style="border:dashed yellow 1px"><marquee> <U>Indian Movies , <U> Hollywood Movies , </U>  <u> Horror Movies , </u>  <u> Crime Dramas , </u> <u> Sci-Fi & Fantasy  </u> </marquee></h1>
    <hr style="color:whitesmoke">
    <h1 style="color:rgb(231, 218, 36); font-family:  sans- serif, Arial, Helvetica;"> -- ABFilms.com --_______________________________________________________________________SIGN IN </h1>
    <hr style="color:whitesmoke"><br>


  <div class="wrapper">
      <nav class="Movie list">
          <button aria-expanded="false" aria-controls="Movie-list">
            <span class="open">☰</span>
            <span class="close">×</span>
            Movie In Demand
          </button>
          <ul id="movie-list">
            <li>
              <a href=""></a>
            </li>
            <li>
              <a href=""> <h2>Trending In Movies </h2></a>
            </li>
            <li>
              <a href=""> <h2>Trending In Web shows</h2></a>
            </li>
            <li>
              <a href=""> <h2>Latest Movies</h2></a>
            </li>
            <li>
              <a href=""> <h2>Latest Web shows</h2></a>
            </li>
            <li>
              <a href=""> <h2>Evergreen Movies</h2></a>
            </li>
          </ul>
        </nav>
    <div class="top">
      <header class="hero">
        <h1># No. 1 Tranding Movie </h1>
        <h2> Pushpa : The Rise </h2>
      </header>
      <div class="cta cta1">
        <h1># No. 2 Tranding Movie </h1>
        <p>Dil Bechara </p>
      </div>
      <div class="cta cta2">
        <h1># No. 3 Tranding Movie </h1>
        <p>Squid Game</p>
        
      </div>

    </div>

    <section class="features">
      <div class="feature">
        <h3>Flight</h3>
        <h4> Action/Drama  </h4>
        <h5> 2hr 27m </h5>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
        <p></p>
      </div>
      <div class="feature2">
        <h3>Spiderman</h3>
        <h4> Action/Drama  </h4>
        <h5> 2hr 23m </h5>
      </div>
      <div class="feature3">
        <h3>Cheechore</h3>
        <h4> Action/Drama  </h4>  
        <h5> 2hr 7m </h5>
      </div>
      <div class="feature4">
        <h3>Dil Bechara</h3>
        <h4> love/Drama  </h4>
        <h5> 2hr 37m </h5>

      </div>
    </section>

    <section class="about">
      <img src="8.jpg" alt="Yummy Taco" class="about__mockup">


      <div class="about__details">
        <h2>Chhichhore</h2>
        <p>Shushant Singh's film which is based on a straggle of a Student's life.</p>
        <p>50 Crore Budget film collect more than 250 Crore on box office.</p>
        <button>Stream Now </button>
      </div>
    </section>

    <section class="about2">
      <img src="3.jpg" alt="Yummy Taco" class="about__mockup">


      <div class="about__details">
        <h2>Jai Bheem</h2>
        <p>Surya's film which is based on a straggle of poor family against currupt police officer .</p>
        <p>20 Crore Budget film collect more than 150 Crore on box office.</p>
        <button>Stream Now </button>
      </div>
    </section>


    <section class="gallery">
      <h2>New BlockBuster Movie </h2>
    
      <img src="ak/3.jpg">
      <img src="ak/106.jpg">
      <img src="ak/4.jpg">
      <img src="ak/8.jpg">
      <img src="ak/2.jpg">
      <img src="ak/102.jpg">
      <img src="ak/7.jpg">
      <img src="ak/104.jpg">
      <img src="ak/105.jpg">
      <img src="ak/107.jpg">
      
      

      
    </section>
  </div>

  

</body>

</html>
