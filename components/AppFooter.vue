<template>
  <footer>
      <div class="container-fluid">
          <div class="row">
              <div class="col-12">
                  <h3 class="explore-more-btn">Explore More</h3>
              </div>
              <div class="col-md-3">
                  <h3 class="footer-list-title">Quick Links</h3>
                  <ul class="footer-links">
                      <li>
                          <nuxt-link :to="localePath('/')">home</nuxt-link>
                      </li>
                      <li>
                          <nuxt-link :to="localePath('/')">About us</nuxt-link>
                      </li>
                      <li>
                          <nuxt-link :to="localePath('/')">Careers</nuxt-link>
                      </li>
                      <li>
                          <nuxt-link :to="localePath('/')">events</nuxt-link>
                      </li>
                      <li>
                          <nuxt-link :to="localePath('/')">news</nuxt-link>
                      </li>
                      <li>
                          <nuxt-link :to="localePath('/')">contact</nuxt-link>
                      </li>
                  </ul>
              </div>
              <div class="col-md-3">
                  <h3 class="footer-list-title">OUR HOSPITALS</h3>
                  <ul class="footer-links">
                      <li>
                          <a href="#"> Al Shalalat </a>
                      </li>
                      <li>
                          <a href="#"> semouha </a>
                      </li>
                      <li>
                          <a href="#"> antoniades </a>
                      </li>
                      <li>
                          <a href="#"> maadi </a>
                      </li>
                      <li>
                          <a href="#"> hai el jamaa </a>
                      </li>
                  </ul>
              </div>
              <div class="col-md-6">
                  <h3 class="footer-list-title">News letter</h3>
                  <form action="#">
                      <input type="email" placeholder="Email Address">
                      <button type="submit">subscribe now</button>
                  </form>
                  <p class="copyright">
                      copyright © 2021 - Andalusia Group
                  </p>
                  <ul class="social-media-links">
                      <li>
                          <a href="#">
                              <i class="fab fa-facebook"></i>
                          </a>
                      </li>
                      <li>
                          <a href="#">
                              <i class="fab fa-twitter"></i>
                          </a>
                      </li>
                      <li>
                          <a href="#">
                              <i class="fab fa-google-plus"></i>
                          </a>
                      </li>
                  </ul>
              </div>
          </div>
      </div>
  </footer>
</template>

<script>
export default {

}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rufina&display=swap');
@import url(//db.onlinewebfonts.com/c/3dd6e9888191722420f62dd54664bc94?family=Myriad+Pro);
@import url('https://fonts.googleapis.com/css2?family=Sintony:wght@700&display=swap');
footer {
    background: #363636;
    padding: 40px 0;
}
footer .footer-list-title {
    font-size: 18px;
    text-transform: uppercase;
    color: #fff;
    margin-bottom: 30px;
    font-family: "Myriad Pro";
}
footer .explore-more-btn {
    color: #fff;
    text-transform: capitalize;
    font-family: 'Rufina', serif;
    font-size: 30px;
    margin-bottom: 50px;
    border-bottom: 1px solid rgb(126 128 125 / 10%);
    padding-bottom: 15px;
}
footer .footer-links {
    padding: 0;
    list-style: none;
    margin: 0;
}
footer .footer-links li a {
    color: #aeb0ab;
    font-size: 13px;
    font-family: "Myriad Pro";
    transition: all .2s linear;
    text-transform: uppercase;
}
footer .footer-links li a:hover {
    color: #fff;
}
footer .footer-links li {
    margin-bottom: 10px;
}
footer .footer-links li:last-of-type {
    margin: 0;
}
footer form {
    display: flex;
    align-items: center;
    margin-bottom: 50px;
}
footer form input {
    outline: none;
    width: 380px;
    max-width: 390px;
    height: 49px;
    border: none;
    padding: 15px 30px;
    font-size: 13px;
    font-family: 'Sintony', sans-serif;
}
footer form button {
    width: 175px;
    max-width: 180px;
    height: 49px;
    border: none;
    font-family: 'Sintony', sans-serif;
    background: #e8663b;
    color: #fff;
    text-transform: uppercase;
    font-size: 14px;
}
footer form input::placeholder {
    color: #7a7a7a;
}
footer .copyright {
    font-size: 13px;
    color: #aeb0ab;
    text-transform: uppercase;
    font-family: "Myriad Pro";
    margin-bottom: 20px;
}
footer .social-media-links {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    align-items: center;
}
footer .social-media-links li {
    margin-right: 10px;
}
ul.social-media-links li a {
    color: #9a9a9a;
    font-size: 18px;
    transition: all .2s linear;
}
ul.social-media-links li a:hover {
    color: #fff;
}
footer .social-media-links li:last-of-type {
    margin: 0;
}
</style>