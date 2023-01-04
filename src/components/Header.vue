<template lang="pug">
.custom-header
  header
    .header-wrapper-color
      .header-wrapper
        p.header-text {{lang === &apos;ukr&apos; ? &quot;Інформація&quot; : &quot;Information&quot;}}
        select#custom-select.custom-select(@change="setLang", name="select")
          option(selected, disabled) Lang
          option(value="value1") Укр
          option(value="value2") Eng
</template>

<!--<template>-->
<!--  <div class="custom-header">-->
<!--    <header>-->
<!--      <div class="header-wrapper-color">-->
<!--        <div class="header-wrapper">-->

<!--          <p class="header-text">{{lang === 'ukr' ? "Інформація" : "Information"}}</p>-->

<!--          <select @change="setLang" id="custom-select" class="custom-select" name="select">-->
<!--            <option selected disabled>Lang</option>-->
<!--            <option value="value1">Укр</option>-->
<!--            <option value="value2">Eng</option>-->
<!--          </select>-->

<!--        </div>-->
<!--      </div>-->
<!--    </header>-->
<!--  </div>-->
<!--</template>-->

<script>
import $ from "jquery";
import {ref} from "vue";

export default {
  name: 'CustomHeader',

  setup() {

    let lang = ref(localStorage.getItem('lang'))

    function setLang() {
      let lang = $("#custom-select option:selected").text().toLowerCase();
      if (lang === 'укр') lang = "ukr"
      localStorage.setItem("lang", lang)
      location.reload()
    }

    return { setLang, lang }
  }
}
</script>

<style scoped lang="scss">

.header-wrapper-color {
  background: #FAFAF7;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 999;
}

.header-wrapper {
  z-index: 999;
  max-width: 1200px;
  margin: 0 auto;
  background: #FAFAF7;
  padding: 20px;
  display: grid;
  gap: 40px;
  grid-template-columns: repeat(2, auto);
  justify-content: space-between;
  align-items: center;
}

.header-text {
  font-family: 'Dela Gothic One', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 64px;
  line-height: 108%;
  letter-spacing: -0.01em;
  color: #171717;
}

.custom-select {
  background-color: transparent;
  border: 1px solid #000;
  border-radius: 10px;
  padding: 5px 10px;
}

</style>