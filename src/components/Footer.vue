<template lang="pug">
.custom-footer
  footer.footer-wrapper
    p {{lang === &apos;ukr&apos; ? &quot;Автор Станіслав Кінаш&quot; : &quot;Made by neprostostas&quot;}}
</template>

<!--<template>-->
<!--  <div class="custom-footer">-->
<!--    <footer class="footer-wrapper">-->
<!--      <p>{{lang === 'ukr' ? "Автор Станіслав Кінаш" : "Made by neprostostas"}}</p>-->
<!--    </footer>-->
<!--  </div>-->
<!--</template>-->

<script>

import {ref} from "vue";

export default {
  name: 'CustomFooter',

  setup() {

    let lang = ref(localStorage.getItem('lang'))

    return { lang }
  }
}
</script>

<style scoped lang="scss">

.footer-wrapper {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;
}

</style>
