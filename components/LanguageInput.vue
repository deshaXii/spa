<template>
  <div class="lansg-area">
    <span class="lang-box" @click="() => { $i18n.locale = 'ar' }" v-if="activeLang === 'en'">  
      <img src="/ar.png" alt="arabic">  
    </span>
    <span class="lang-box" @click="() => { $i18n.locale = 'en' }" v-if="activeLang === 'ar'">  
      <img src="/en.jpg" alt="english">    
    </span>


  </div>
</template>
<script>
export default {
  computed: {
    activeLang() {
      return this.$i18n.locale
    }
  },
  updated() {
    if (this.$i18n.locale === 'ar') {
      document.querySelector('body').classList.add('rtl')
    } else {
      document.querySelector('body').classList.remove('rtl')
    }
  }
}
</script>


<style lang="scss">
  
</style>