<template>
  <section class="services-section">
      <img src="/services-pr1.png" class="pr-1" alt="">
      <img src="/services-pr2.png" class="pr-2" alt="">
    <div class="img-par">
        <img src="/services-pr.png" alt="">
    </div>
      <div class="container">
          <div class="row">
              <div class="col-12">
                  <div class="section-title">
                      <h2> {{ $t('servicesTitle') }} </h2>
                      <div class="section-title-dots">
                            <span></span>
                            <span></span>
                            <span></span>
                      </div>
                  </div>
              </div>
              <div class="col-md-4">
                  <div class="service-box">
                      <div class="service-img-box">
                          <img src="/service-icon1.png" alt="">
                      </div>
                      <h4>{{ $t('firstServieTitle') }}</h4>
                      <p>{{ $t('firstServieParagraph') }}</p>
                  </div>
              </div>
              <div class="col-md-4">
                  <div class="service-box">
                      <div class="service-img-box">
                          <img src="/service-icon2.png" alt="">
                      </div>
                      <h4>{{ $t('secondServieTitle') }}</h4>
                      <p>{{ $t('secondServieParagraph') }}</p>
                  </div>
              </div>
              <div class="col-md-4">
                  <div class="service-box">
                      <div class="service-img-box">
                          <img src="/service-icon3.png" alt="">
                      </div>
                      <h4>{{ $t('thirdServieTitle') }}</h4>
                      <p>{{ $t('thirdServieParagraph') }}</p>
                  </div>
              </div>
              <div class="col-12">
                  <div class="btn-show-more">
                      <b-button class="border-btn">
                          {{ $t('servicesBtn') }}
                      </b-button>
                  </div>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
import {gsap} from 'gsap'
import { ScrollTrigger } from "gsap/dist/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);
export default {
mounted() {
    this.startAnimation()
  },
  methods: {
    startAnimation() {
        gsap.to('.pr-1', {
            yPercent: 50,
            scrollTrigger: {
            trigger: '.pr-1',
            start: 'top top',
            toggleActions: 'play none none reverse',
            }
        })
        gsap.to('.pr-2', {
            yPercent: 50,
            scrollTrigger: {
            trigger: '.pr-2',
            start: 'top top',
            toggleActions: 'play none none reverse',
            }
        })
        gsap.to('.img-par', {
            yPercent: 50,
            scrollTrigger: {
            trigger: '.img-par',
            start: 'top top',
            toggleActions: 'play none none reverse',
            }
        })
    }
  }
}
</script>

<style>
.service-box {
    text-align: center;
}

.service-img-box {
    position: relative;
    min-height: 110px;
    margin-bottom: 30px;
}

.service-img-box:before, .service-img-box:after {transition: all .2s linear; transform: translateX(-50%);content:'';position: absolute;top: 0;left: 50%;width: 110px;height: 110px;background: #333;border-radius: 50%;z-index: -1;}
.service-box:hover .service-img-box::before {
    top: 0;
    left: 50%;
}

.service-box:hover .service-img-box::after {
    left: calc(50% + 10px);
    top: 5px;
}
.section-title {
    margin-bottom: 120px;
    text-align: center;
    text-transform: uppercase;
    font-weight: bold;
    position: relative;
}
.section-title h2 {
    font-size: 36px;
    font-weight: bold;
    color: #000000;
    margin-bottom: 15px;
}

.service-img-box img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    transition: all .2s linear;
}

.service-img-box:before {
    left: calc(50% + 10px);
    background: #ddc2db;
    top: 5px;
}

.service-img-box:after {
    background: linear-gradient(to left, #eb6b3d, #ca3423);
}

.service-box h4 {
    color: #686868;
    font-size: 22px;
    text-transform: capitalize;
}

.service-box p {
    color: #848484;
    font-size: 18px;
}
section.services-section {background-size: cover; overflow: hidden;}
img.pr-1 {
    position: absolute;
    top: 0;
    right: -70px;
    transition: all .2s linear;
}

img.pr-2 {
    position: absolute;
    left: -160px;
    bottom: 0;
    transition: all .2s linear;
}
.service-box:hover .service-img-box img {
    transform: scale(0.9) translate(-50%,-50%);
}
section.services-section .img-par {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    z-index: -1;
    bottom: 0;
}

section.services-section .img-par img {
    width: 100%;
    height: 100%;
    object-fit: scale-down;
}
.btn-show-more {
    text-align: center;
    margin-top: 100px;
}

.btn-show-more button {
    border: 1px solid #d1d1d1;
    color: #a0a0a0;
    background: transparent;
    border-radius: 10px;
    min-height: 48px;
    min-width: 258px;
}

.btn-show-more button:hover {
    background: linear-gradient(to right, #eb6b3d, #ca3423);
}
.section-title span:first-of-type {
    width: 11px;
    height: 11px;
    background: #d74a2e;
    display: inline-block;
    transform: rotate(45deg);
}

.section-title span:nth-of-type(2) {
    display: inline-block;
    background: #d74a2e;
    width: 50px;
    height: 7px;
    margin: 0px 7px;
}

.section-title span:nth-of-type(3) {
    display: inline-block;
    background: #d74a2e;
    width: 16px;
    height: 7px;
}
.section-title-dots {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>