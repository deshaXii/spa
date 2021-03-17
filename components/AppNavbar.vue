<template>
<div class="site-navbar">
  <b-navbar toggleable="lg" :class="pageScrolled">
    <div class="container-fluid">
    <nuxt-link class="navbar-brand" :to="localePath('/')">
      <img src="/logo.jpg" />
    </nuxt-link>

    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

    <b-collapse id="nav-collapse" is-nav>

      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#"> {{ $t('navbarMenu.home') }} </b-nav-item>
        <div @mouseover="onOver" @mouseleave="onLeave">
            <b-dropdown :text="$t('navbarMenu.about')" ref="dropdown" class="m-md-2">
                <b-dropdown-item>{{ $t('navbarMenu.ourCompany') }}</b-dropdown-item>
                <b-dropdown-item>{{ $t('navbarMenu.partnersAndAccreditations') }}</b-dropdown-item>
                <b-dropdown-item>{{ $t('navbarMenu.corporateStructure') }}</b-dropdown-item>
            </b-dropdown>
        </div>
        <b-nav-item href="#">{{ $t('navbarMenu.businessUnits') }}</b-nav-item>
        <b-nav-item href="#">{{ $t('navbarMenu.projects') }}</b-nav-item>
        <b-nav-item href="#">{{ $t('navbarMenu.partners') }}</b-nav-item>
        <b-nav-item href="#">{{ $t('navbarMenu.partners') }}</b-nav-item>
        <b-nav-item href="#">{{ $t('navbarMenu.contacts') }}</b-nav-item>
        <b-nav-item href="#">{{ $t('navbarMenu.careers') }}</b-nav-item>
        <div class="btns">
          <Search />
          <language-input/>
        </div>
      </b-navbar-nav>
    </b-collapse>
    </div>
  </b-navbar>
</div>
</template>

<script>
import LanguageInput from '../components/LanguageInput.vue';
import Search from '../components/Search';

export default {
  name: 'navbar',
  components: { LanguageInput, Search },
  data() {
    return {
      isScrolled: false
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
      this.isScrolled = window.scrollY > 0
    },
    onOver() {
      this.$refs.dropdown.visible = true;
    },
    onLeave() {
      this.$refs.dropdown.visible = false;
    }
  },
  computed: {
    pageScrolled () {
      if (this.isScrolled) {
        return 'fixed-top'
      }
    }
  },
}
</script>



<style lang="scss">

.navbar.has-background {
  background-image: linear-gradient(red, orange);
}
.site-navbar nav.navbar {
  background: #fff;
  padding: 0;
  height: 69px;
  box-shadow: 0px 0px 5px rgb(51 51 51 / 15%);
  .container-fluid {
    height: 100%;
  }
  #nav-collapse {
    height: 100%;
  }
  .navbar-nav {
    height: 100%;
    line-height: 69px;
    .dropdown {
      height: 100%;
      margin: 0 !important;
      vertical-align: top;
      button {
        position: relative;
        padding-top: 0;
        padding-bottom: 0;
        border-radius: 0;
        background: transparent;
        color: #575757;
        text-transform: capitalize;
        font-size: 18px;
        border: none;
        &:after {
          content: none;
        }
      }
    }
    .nav-item > a {
      padding: 0 12.5px;
      font-size: 18px;
      text-transform: capitalize;
      color: #575757;
    }
  }
  .lansg-area .lang-box img {
    width: 35px;
    height: 35px;
    object-fit: cover;
    border-radius: 50%;
  }
  a.navbar-brand {
      margin: 0;
      padding: 0;
  }
  .nav-item {
    height: 100%;
  }
}
.site-navbar nav.navbar .navbar-nav .dropdown.show button {
    color: #e44b37;
    font-weight: bold;
    background: #f6f6f6;
}
.site-navbar nav.navbar .navbar-nav .dropdown ul.dropdown-menu {
    border: none;
    background: #f6f6f6;
    padding: 0;
    box-shadow: 0px 4px 5px rgb(0 0 0 / 24%);
    margin: 0;
    /* z-index: -1; */
    border-radius: 0;
}
.site-navbar nav.navbar .navbar-nav .dropdown ul.dropdown-menu li .dropdown-item {
    height: 69px;
    font-size: 18px;
    color: #575757;
    min-width: 288px;
    border-bottom: 1px solid #e3e3e3;
    padding: 0 15px;
}
.site-navbar nav.navbar .navbar-nav .dropdown ul.dropdown-menu li:last-of-type .dropdown-item {
    border: 0;
}
</style>