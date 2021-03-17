<template>
    <section class="statistics-section" style="background-image: url(/statistics-bg.jpg)">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="section-title">
                        <h2>statistics</h2>
                        <div class="section-title-dots">
                            <span></span>
                            <span></span>
                            <span></span>
                        </div>
                    </div>
                </div>
                <div class="col-md-3 col-6">
                    <div class="statistic-box">
                        <div class="statistic-icon">
                            <img src="/statistic-icon1.png" alt="">
                        </div>
                        <h4>
                            <number
                            ref="number1"
                            from="0"
                            animationPaused
                            to="321570"
                            :duration=duration
                            easing="Power4.easeOut"/>
                        </h4>
                        <span>clients serviced</span>
                    </div>
                </div>
                <div class="col-md-3 col-6">
                    <div class="statistic-box">
                        <div class="statistic-icon">
                            <img src="/statistic-icon2.png" alt="">
                        </div>
                        <h4>
                            <number
                            ref="number2"
                            from="0"
                            animationPaused
                            to="5140"
                            :duration=duration
                            easing="Power4.easeOut"/>
                        </h4>
                        <span>machienes</span>
                    </div>
                </div>
                <div class="col-md-3 col-6">
                    <div class="statistic-box">
                        <div class="statistic-icon">
                            <img src="/statistic-icon3.png" alt="">
                        </div>
                        <h4>
                            <number
                            ref="number3"
                            from="0"
                            animationPaused
                            to="61473"
                            :duration=duration
                            easing="Power4.easeOut"/>
                        </h4>
                        <span>qulified staff</span>
                    </div>
                </div>
                <div class="col-md-3 col-6">
                    <div class="statistic-box">
                        <div class="statistic-icon">
                            <img src="/statistic-icon4.png" alt="">
                        </div>
                        <h4>
                            <number
                            ref="number4"
                            from="0"
                            animationPaused
                            to="126"
                            :duration=duration
                            easing="Power4.easeOut"/>
                        </h4>
                        <span>sites</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import Vue from 'vue'
import VueNumber from 'vue-number-animation'
 
Vue.use(VueNumber)
export default {
    data() {
        return {
            isScrolled: false,
            duration: 5
        }
    },
    mounted () {
        window.addEventListener('scroll', this.setIsScrolled, { passive: true })
        this.setIsScrolled()
    },
    destroyed () {
        window.removeEventListener('scroll', this.setIsScrolled, { passive: true })
    },
    methods: {
        setIsScrolled () {
            let sectionOffset = document.querySelector('.statistics-section').offsetTop - 450
            this.isScrolled = window.scrollY >= sectionOffset
            if (this.isScrolled && window.pageYOffset >= sectionOffset) {
                this.$refs.number1.play()
                this.$refs.number2.play()
                this.$refs.number3.play()
                this.$refs.number4.play()
            } else {
                this.$refs.number1.pause()
                this.$refs.number2.pause()
                this.$refs.number3.pause()
                this.$refs.number4.pause()
            } 
        },
    },
 
}
</script>

<style>
.statistics-section:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: #312722;
    opacity: 0.85;
}

.statistics-section {
    background-size: cover;
    background-position: bottom;
}

.statistic-box {
    text-align: center;
}

.statistic-icon {
    width: 82px;
    height: 82px;
    border: 3px solid #d1d1d1;
    border-radius: 5px;
    line-height: 85px;
    position: relative;
    margin: 0 auto;
    margin-bottom: 30px;
    transition: all .2s linear;
}

.statistic-icon img {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
    margin: 0 auto;
}

.statistic-box h4, .statistic-box h4 span {
    font-size: 30px;
    font-weight: bold;
    color: #fff;
}

.statistic-box span {
    font-size: 22px;
    color: #fff;
    text-transform: capitalize;
}

.statistic-box:hover .statistic-icon {
    background: #fff;
    border-color: #fff;
}

.statistic-box:hover .statistic-icon img {
    filter: invert(53%) sepia(94%) saturate(2256%) hue-rotate(339deg) brightness(100%) contrast(87%);
}

.statistics-section .section-title h2 {
    color: #fff;
}
</style>