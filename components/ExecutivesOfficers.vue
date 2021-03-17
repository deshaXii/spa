<template>
    <section class="executives-officers">
        <span id="getOffsetForNextSection"></span>
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="section-title">
                        <h2>executives officers</h2>
                        <div class="section-title-dots">
                            <span></span>
                            <span></span>
                            <span></span>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div class="big-box">
                        <div class="ex-of-box"> 
                            <div class="img-box">
                                <img :src="getActivePerson[0].img" alt="">
                            </div>
                            <div class="info-box">
                                <h4>{{getActivePerson[0].name}}</h4>
                                <h6>{{getActivePerson[0].title}}</h6>
                                <p>{{ getActivePerson[0].intro }}</p>
                                <ul class="social-media-box"> 
                                    <li>
                                        <a :href="getActivePerson[0].socialMedia.facebook">
                                            <i class="fab fa-facebook"></i>
                                        </a>
                                    </li>
                                    <li>
                                        <a :href="getActivePerson[0].socialMedia.twitter">
                                            <i class="fab fa-twitter"></i>
                                        </a>
                                    </li>
                                    <li>
                                        <a :href="getActivePerson[0].socialMedia.instagram">
                                            <i class="fab fa-instagram"></i>
                                        </a>
                                    </li>
                                    <li>
                                        <a :href="getActivePerson[0].socialMedia.linkedin">
                                            <i class="fab fa-linkedin"></i>
                                        </a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-md-6">
                    <div 
                        class="row"
                        v-for="person in getPersonsWithoutActive"
                        :key="person.id"
                    >
                        <div
                            class="col-md-6 small-box"
                            v-for="(per, index) in person"
                            :key="index"
                            :data-index="per.id"
                            @click="makeItActive"
                        >
                            <div class="ex-of-box"> 
                                <div class="img-box">
                                    <img :src="per.img" alt="">
                                </div>
                                <div class="info-box">
                                    <h4>{{per.name}}</h4>
                                </div>
                            </div>
                        </div>
                    </div>
                    
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    data() {
        return {
            activePerson: 0,
            persons: [
                {
                    id: 0,
                    img: '/per.png',
                    name: 'hazem darwiesh',
                    title: 'chief executive officer',
                    intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam sed assumenda reiciendis cupiditate illo cum iusto vel, atque blanditiis pariatur eius unde id? Eveniet ipsum, harum aspernatur quod possimus odit nihil magni fuga mollitia non, quidem debitis sint reprehenderit sequi corrupti, officiis dolores nulla. Quasi pariatur quas esse ullam aut.',
                    socialMedia: {
                        facebook: '#',
                        twitter: '#',
                        instagram: '#',
                        linkedin: '#'
                    }
                },
                {
                    id: 1,
                    img: '/per1.jpg',
                    name: 'Mr. Mohamed AbdelRasoul',
                    title: 'chief executive officer',
                    intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam sed assumenda reiciendis cupiditate illo cum iusto vel, atque blanditiis pariatur eius unde id? Eveniet ipsum, harum aspernatur quod possimus odit nihil magni fuga mollitia non, quidem debitis sint reprehenderit sequi corrupti, officiis dolores nulla. Quasi pariatur quas esse ullam aut.',
                    socialMedia: {
                        facebook: '#',
                        twitter: '#',
                        instagram: '#',
                        linkedin: '#'
                    }
                },
                {
                    id: 2,
                    img: '/per2.jpg',
                    name: 'Dr. Alaa AlGoweini',
                    title: 'chief executive officer',
                    intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam sed assumenda reiciendis cupiditate illo cum iusto vel, atque blanditiis pariatur eius unde id? Eveniet ipsum, harum aspernatur quod possimus odit nihil magni fuga mollitia non, quidem debitis sint reprehenderit sequi corrupti, officiis dolores nulla. Quasi pariatur quas esse ullam aut.',
                    socialMedia: {
                        facebook: '#',
                        twitter: '#',
                        instagram: '#',
                        linkedin: '#'
                    }
                },
                {
                    id: 3,
                    img: '/per3.jpg',
                    name: 'Dr. Walaa Kadry',
                    title: 'chief executive officer',
                    intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam sed assumenda reiciendis cupiditate illo cum iusto vel, atque blanditiis pariatur eius unde id? Eveniet ipsum, harum aspernatur quod possimus odit nihil magni fuga mollitia non, quidem debitis sint reprehenderit sequi corrupti, officiis dolores nulla. Quasi pariatur quas esse ullam aut.',
                    socialMedia: {
                        facebook: '#',
                        twitter: '#',
                        instagram: '#',
                        linkedin: '#'
                    }
                },
                {
                    id: 4,
                    img: '/per4.jpg',
                    name: 'Mr. AbdelHakim GamalElDin',
                    title: 'chief executive officer',
                    intro: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit. Ullam sed assumenda reiciendis cupiditate illo cum iusto vel, atque blanditiis pariatur eius unde id? Eveniet ipsum, harum aspernatur quod possimus odit nihil magni fuga mollitia non, quidem debitis sint reprehenderit sequi corrupti, officiis dolores nulla. Quasi pariatur quas esse ullam aut.',
                    socialMedia: {
                        facebook: '#',
                        twitter: '#',
                        instagram: '#',
                        linkedin: '#'
                    }
                }
            ]
        }
    },
    computed: {
        getActivePerson() {
            let activePerson = this.activePerson
            const getActivePerson = this.persons.filter(person => person.id == activePerson);
            return {...getActivePerson}
        },
        getPersonsWithoutActive() {
            let activePerson = this.activePerson
            const getPersonsWithoutActive = this.persons.filter(person => person.id != activePerson);
            let first = getPersonsWithoutActive.slice(0, 2),
                second = getPersonsWithoutActive.slice(2, 4);
            return [first, second]
        }
    },
    methods: {
        makeItActive(event) {
            let newActivePerson = event.currentTarget.getAttribute('data-index');
            this.activePerson = newActivePerson
        }
    }
}
</script>

<style>
.big-box {
    box-shadow: 0px 0px 5px rgb(0 0 0 / 20%);
}

.big-box .info-box {
    padding: 25px 30px;
}
.small-box .ex-of-box {
    cursor: pointer;
}
.big-box .img-box img {
    width: 100%;
    max-height: 290px;
    object-fit: cover;
}
.small-box .img-box img {
    width: 100%;
    max-height: 240px;
    height: 240px;
    object-fit: cover;
}
span#getOffsetForNextSection {
    position: absolute;
    top: 50%;
}
.small-box .info-box h4 {
    font-size: 18px;
    font-weight: bold;
    color: #101010;
    text-align: center;
    text-transform: capitalize;
    margin-top: 20px;
}

.small-box .info-box {
    margin-bottom: 40px;
}
.big-box .info-box h4 {
    color: #101010;
    font-size: 30px;
    text-transform: capitalize;
    font-weight: bold;
}

.big-box .info-box h6 {
    color: #d74a2e;
    font-size: 17px;
    font-weight: bold;
    text-transform: capitalize;
    margin-bottom: 20px;
}

.big-box .info-box p {
    font-size: 16px;
    color: #111;
}

.big-box .info-box .social-media-box {
    display: flex;
    align-items: center;
    list-style: none;
    padding: 0;
    margin: 0;
    border-top: 1px solid #e7e7e7;
    padding-top: 20px;
    margin-top: 25px;
}

.big-box .info-box .social-media-box li {
    margin-left: 10px;
}

.big-box .info-box .social-media-box li a {
    width: 35px;
    height: 35px;
    display: block;
    background: #0a2134;
    border-radius: 50%;
    line-height: 35px;
    color: #fff;
    text-align: center;
    font-size: 13px;
}

.big-box .info-box .social-media-box li:first-of-type {
    margin-left: 0;
}
</style>