<template lang="pug">
.custom-main
  nav
    .nav-part
      .swap-buttons
        .choose-button(@click="[faq = true, contacts = false, where = false, partner = false]")
          p(:class="{ active: !faq }") {{lang === &apos;ukr&apos; ? &quot;Популярні запитання&quot; : &quot;FAQ&quot;}}
        .choose-button(@click="[faq = false, contacts = true, where = false, partner = false]")
          p(:class="{ active: !contacts }") {{lang === &apos;ukr&apos; ? &quot;Наші контакти&quot; : &quot;Our contacts&quot;}}
        .choose-button(@click="[faq = false, contacts = false, where = true, partner = false]")
          p(:class="{ active: !where }") {{lang === &apos;ukr&apos; ? &quot;Де придбати?&quot; : &quot;Where to buy?&quot;}}
        .choose-button(@click="[faq = false, contacts = false, where = false, partner = true]")
          p(:class="{ active: !partner }") {{lang === &apos;ukr&apos; ? &quot;Стати партнером&quot; : &quot;Become a partner&quot;}}
      .logos-block
        img(src="../assets/logo-1.png", alt="logo-1")
        img(src="../assets/logo-2.png", alt="logo-2")
        img(src="../assets/logo-3.png", alt="logo-3")
  .main-content
    .faq-content(v-if="faq", :class="{ open: faq }")
      FaqSection
    .contacts-content(v-if="contacts", :class="{ open: contacts }")
      ContactsSection
    .where-content(v-if="where", :class="{ open: where }")
      WhereSection
    .partner-content(v-if="partner", :class="{ open: partner }")
      PartnerSection
</template>

<!--<template>-->
<!--  <div class="custom-main">-->

<!--    <nav>-->
<!--      <div class="nav-part">-->
<!--        <div class="swap-buttons">-->

<!--          <div class="choose-button" @click="[faq = true, contacts = false, where = false, partner = false]">-->
<!--            <p :class="{ active: !faq }">{{lang === 'ukr' ? "Популярні запитання" : "FAQ"}}</p>-->
<!--          </div>-->

<!--          <div class="choose-button" @click="[faq = false, contacts = true, where = false, partner = false]">-->
<!--            <p :class="{ active: !contacts }">{{lang === 'ukr' ? "Наші контакти" : "Our contacts"}}</p>-->
<!--          </div>-->

<!--          <div class="choose-button" @click="[faq = false, contacts = false, where = true, partner = false]">-->
<!--            <p :class="{ active: !where }">{{lang === 'ukr' ? "Де придбати?" : "Where to buy?"}}</p>-->
<!--          </div>-->

<!--          <div class="choose-button" @click="[faq = false, contacts = false, where = false, partner = true]">-->
<!--            <p :class="{ active: !partner }">{{lang === 'ukr' ? "Стати партнером" : "Become a partner"}}</p>-->
<!--          </div>-->

<!--        </div>-->
<!--        <div class="logos-block">-->
<!--          <img src="../assets/logo-1.png" alt="logo-1">-->
<!--          <img src="../assets/logo-2.png" alt="logo-2">-->
<!--          <img src="../assets/logo-3.png" alt="logo-3">-->
<!--        </div>-->
<!--      </div>-->
<!--    </nav>-->

<!--    <div class="main-content">-->

<!--      <div v-if="faq" class="faq-content" :class="{ open: faq }">-->
<!--        <FaqSection />-->
<!--      </div>-->

<!--      <div v-if="contacts" class="contacts-content" :class="{ open: contacts }">-->
<!--        <ContactsSection />-->
<!--      </div>-->

<!--      <div v-if="where" class="where-content" :class="{ open: where }">-->
<!--        <WhereSection />-->
<!--      </div>-->

<!--      <div v-if="partner" class="partner-content" :class="{ open: partner }">-->
<!--        <PartnerSection />-->
<!--      </div>-->

<!--    </div>-->

<!--  </div>-->
<!--</template>-->

<script>
import { ref } from "vue";
import FaqSection from "@/components/faq.vue";
import ContactsSection from "@/components/contacts.vue";
import WhereSection from "@/components/where.vue";
import PartnerSection from "@/components/partner.vue";

export default {
  name: 'CustomMain',
  components: {
    PartnerSection,
    WhereSection,
    ContactsSection,
    FaqSection
  },

  setup() {

    let lang = ref(localStorage.getItem('lang'))

    const faq = ref(true)
    const contacts = ref(false)
    const where = ref(false)
    const partner = ref(false)

    return { faq, contacts, where, partner, lang }
  }
}
</script>

<style scoped lang="scss">

.main-content > div {
  display: none;
}

.main-content > div.open {
  display: block;
  animation: fadeIn 1s;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }

  to {
    opacity: 1;
  }
}

.custom-main {
  padding: 140px 20px 0;
  display: grid;
  grid-template-columns: 250px auto;
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.choose-button p {
  padding: 20px 20px 20px 0;
  border-radius: 15px;
  display: inline-block;
  font-family: 'Dela Gothic One', sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 148%;
  letter-spacing: -0.01em;
}

.choose-button p:hover {
  position: relative;
  top: 1px;
  color: #413f3f;
}

.active {
  color: #8d8d8d;
}

.swap-buttons {
  cursor: pointer;
}

.nav-part {
  display: grid;
  height: 75vh;
  align-content: space-between;
}

.logos-block {
  display: grid;
  align-items: center;
  justify-content: start;
  grid-template-columns: repeat(3, auto);
  gap: 25px;
}

</style>
