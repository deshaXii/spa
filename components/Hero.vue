<template>
  <section class="hero-section" style="padding: 0;">
    <b-carousel
      id="hero"
      :interval="4000"
      controls
      indicators
    >
       
        <!-- Text slides with image -->
        <b-carousel-slide class="slider-item1"
            img-src="/hero-bg.jpg"
        >
         <span class="slider-opacity-img" style="background-image: url('/hero-bg-opacity.png')"></span>
            <div class="container-fluid">
                <div class="row">
                    <div class="col-6">
                        <h1>{{ $t('heroTitleOne') }} <br/> {{ $t('heroTitleTwo') }}</h1>
                        <p>{{ $t('heroParagraphOne') }} </p>
                        <b-button class="gradient-btn">{{ $t('heroButton') }}</b-button>
                    </div>
                </div>
            </div>
        </b-carousel-slide>

        <b-carousel-slide class="slider-item2"
            img-src="/hero-bg2.jpg"
        >
            <div class="slider-2-content">
                <ul class="socialMedia-icons">
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
                    <li>
                        <a href="#">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </li>
                </ul>
                <h1>{{ $t('heroTitleThree') }} <br/> {{ $t('heroTitleFour') }}</h1>
                <p>{{ $t('heroParapraphTwo') }}</p>
            </div>
        </b-carousel-slide>


        <b-carousel-slide
            img-src="/hero-bg3.jpg"
        >
        </b-carousel-slide>

    </b-carousel>
  </section>
</template>

<script>
  export default {
    data() {
      return {
        
      }
    },
    methods: {
     
    }
  }
</script>


<style lang="scss">
.slider-item1 .carousel-caption {
    top: 0;
    transform: none;
    height: 100%;
}

.slider-item1 .carousel-caption .slider-opacity-img {
    z-index: -1;
}

.slider-item1 .carousel-caption .container-fluid {
    top: 50%;
    position: relative;
    transform: translateY(-50%);
}
.hero-section #hero .carousel-item img {
    height: 85vh;
    max-height: 776px;
    object-fit: cover;
}
.carousel-caption {
    left: 0px;
    right: auto;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
    text-align: left;
}
.carousel-fade .carousel-item.active {
    z-index: unset !important;
}
span.slider-opacity-img {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 2;
    opacity: 0.9;
    background-repeat: no-repeat;
    background-size: contain;
}
#hero .carousel-caption h1 {
    color: #e44b37;
    font-size: 48px;
    margin-bottom: 40px;
}

#hero .carousel-caption p {
    color: #848484;
    font-size: 18px;
    margin-bottom: 35px;
}
.gradient-btn {
    background: linear-gradient(to right, #eb6b3d, #ca3423);
    box-shadow: 2px 0px 5px rgb(211 54 33 / 53%);
    min-width: 180px;
    min-height: 48px;
    font-size: 22px;
    border-radius: 10px;
    padding: 0;
    border: none;
}
a.carousel-control-next, a.carousel-control-prev {z-index: 9999;opacity: 1;}
a.carousel-control-next {
    width: auto;
    height: auto;
    bottom: auto;
    top: calc(50% + 70px);
    transform: rotate(90deg) translateY(-50%);
    right: 80px;
}
a.carousel-control-prev {
    width: auto;
    height: auto;
    bottom: auto;
    top: calc(50% - 70px);
    transform: rotate(
90deg
) translateY(-50%);
    right: 80px;
    left: auto;
}
.search-area {
    margin: 0 25px;
}
.search-area i.fa-search {
    font-size: 24px;
    line-height: 69px;
    color: #525252;
}

.carousel-indicators {
    right: 75px;
    left: auto;
    bottom: auto;
    margin: 0;
    top: calc(50%  + 15px);
    transform: translateY(-50%);
    display: block;
}
.carousel-indicators li.active {
    background: #de9c68
}
.carousel-indicators li {
    margin: 0;
    flex: unset;
    width: 11px;
    height: 11px;
    background-clip: unset;
    border: none;
    transform: rotate(45deg);
    margin-bottom: 15px;
    border: 2px solid #fff;
    opacity: 1;
    box-sizing: border-box;
    box-shadow: 2px 0px 5px rgb(174 174 174 / 50%);
}

.carousel-indicators li:focus {
    outline: none;
}
.slider-2-content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    text-align: center;
}

.slider-2-content .socialMedia-icons {
    padding: 0;
    margin: 0;
    list-style: none;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 20px;
}

#hero .carousel-caption .slider-2-content h1 {
    color: #525252;
    font-weight: bold;
    margin-bottom: 20px;
}

.slider-2-content .socialMedia-icons li {
    margin-right: 15px;
}

.slider-2-content .socialMedia-icons li a {
    color: #e44b37;
    font-size: 18px;
}

.slider-2-content .socialMedia-icons li:last-of-type {
    margin: 0;
}
#hero .carousel-caption .slider-2-content p {
    font-size: 18px;
    color: #686868;
}
</style>