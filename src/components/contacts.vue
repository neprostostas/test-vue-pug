<template lang="pug">
.contacts-section
  .map-block
    img(src="../assets/map.png", alt="map")
  .info-block
    .group-item
      h4 {{lang === &apos;ukr&apos; ? &quot;Адреса офісу&quot; : &quot;Address office&quot;}}
      p {{lang === &apos;ukr&apos; ? &quot;Київ. вул. В’ячеслава Чорновола, буд. 25&quot; : &quot;Kyiv. St. Vyacheslava Chornovola, bldg. 25&quot;}}
    .group-item
      h4 {{lang === &apos;ukr&apos; ? &quot;Номер телефону&quot; : &quot;Phone number&quot;}}
      p +38(096)744-44-44
    .group-item
      h4 {{lang === &apos;ukr&apos; ? &quot;Поштова скринька&quot; : &quot;Email&quot;}}
      p contact@sabpods.com
    .group-item
      h4 {{lang === &apos;ukr&apos; ? &quot;Соціальні мережі&quot; : &quot;Social networks&quot;}}
      .sub-group-social
        a(href="#") {{lang === &apos;ukr&apos; ? &quot;Телеграм&quot; : &quot;Telegram&quot;}}
        a(href="#") {{lang === &apos;ukr&apos; ? &quot;Інстаграм&quot; : &quot;Instagram&quot;}}
    Button(:background="'171717'", :color="'FAFAF7'") {{lang === &apos;ukr&apos; ? &quot;Зворотній звʼязок&quot; : &quot;Feedback&quot;}}
</template>

<!--<template>-->
<!--  <div class="contacts-section">-->
<!--    <div class="map-block">-->
<!--      <img src="../assets/map.png" alt="map">-->
<!--    </div>-->
<!--    <div class="info-block">-->
<!--      <div class="group-item">-->
<!--        <h4>{{lang === 'ukr' ? "Адреса офісу" : "Address office"}}</h4>-->
<!--        <p>{{lang === 'ukr' ? "Київ. вул. В’ячеслава Чорновола, буд. 25" : "Kyiv. St. Vyacheslava Chornovola, bldg. 25"}}</p>-->
<!--      </div>-->
<!--      <div class="group-item">-->
<!--        <h4>{{lang === 'ukr' ? "Номер телефону" : "Phone number"}}</h4>-->
<!--        <p>+38(096)744-44-44</p>-->
<!--      </div>-->
<!--      <div class="group-item">-->
<!--        <h4>{{lang === 'ukr' ? "Поштова скринька" : "Email"}}</h4>-->
<!--        <p>contact@sabpods.com</p>-->
<!--      </div>-->
<!--      <div class="group-item">-->
<!--        <h4>{{lang === 'ukr' ? "Соціальні мережі" : "Social networks"}}</h4>-->
<!--        <div class="sub-group-social">-->
<!--          <a href="#">{{lang === 'ukr' ? "Телеграм" : "Telegram"}}</a>-->
<!--          <a href="#">{{lang === 'ukr' ? "Інстаграм" : "Instagram"}}</a>-->
<!--        </div>-->
<!--      </div>-->
<!--      <Button :background="'171717'" :color="'FAFAF7'">{{lang === 'ukr' ? "Зворотній звʼязок" : "Feedback"}}</Button>-->
<!--    </div>-->
<!--  </div>-->
<!--</template>-->

<script>
import { ref } from "vue";
import Button from "@/components/base/Button.vue";
export default {
  name: 'ContactsSection',
  components: {Button},

  setup() {
    let lang = ref(localStorage.getItem('lang'))

    return {lang}
  }
}
</script>

<style scoped lang="scss">

.group-item h4 {
  font-family: 'Dela Gothic One', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 16px;
  line-height: 19px;
  letter-spacing: -0.01em;
  color: #8B8B8B;
}

.group-item p {
  padding: 10px 0;
  font-family: 'Dela Gothic One', sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 135%;
  letter-spacing: -0.01em;
  color: #171717;
}

.contacts-section {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 30px;
}

.sub-group-social a {
  padding: 10px 0;
  text-decoration: none;
  color: #171717;
}

.sub-group-social a:hover {
  text-decoration: underline;
}

.map-block img {
  width: 400px;
}

.sub-group-social {
  padding-bottom: 35px;
  display: grid;
  grid-template-columns: repeat(2, auto);
  gap: 15px;
  align-items: center;
  justify-content: start;
}

</style>
