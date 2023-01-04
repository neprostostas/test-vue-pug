<template lang="pug">
.partner-section
  h2.text-partner {{lang === &apos;ukr&apos; ? &quot;Ми завжди відкриті до партнерства та співпраці!&quot; : &quot;We are always open to partnership and cooperation!&quot;}}
  p {{lang === &apos;ukr&apos; ? &quot;Ми чітко бачимо, що чекає нас на горизонті та за ним. Ми постійно йдемо, їдемо, летимо, аби лише не стояти на місці та розвиватися.&quot; : &quot;We can clearly see what awaits us on the horizon and beyond. We are constantly walking, driving, flying in order not to stand still and develop.&quot;}}
  p.last-text {{lang === &apos;ukr&apos; ? &quot;Якщо хочеш стати дистриб’ютором, партнером чи маєш ідею для колаборації, то виходь на зв’язок з нами!&quot; : &quot;If you want to become a distributor, partner or have an idea for collaboration, get in touch with us!&quot;}}
  .media-block
    Button(:background="'transparent'", :color="'171717'") {{lang === &apos;ukr&apos; ? &quot;стати партнером&quot; : &quot;become a partner&quot;}}
    img(src="../assets/product.png", alt="product")
</template>

<!--<template>-->
<!--  <div class="partner-section">-->
<!--    <h2 class="text-partner">{{lang === 'ukr' ? "Ми завжди відкриті до партнерства та співпраці!" : "We are always open to partnership and cooperation!"}}</h2>-->
<!--    <p>{{lang === 'ukr' ? "Ми чітко бачимо, що чекає нас на горизонті та за ним. Ми постійно йдемо, їдемо, летимо, аби лише не стояти на місці та розвиватися." : "We can clearly see what awaits us on the horizon and beyond. We are constantly walking, driving, flying in order not to stand still and develop."}}</p>-->
<!--    <p class="last-text">{{lang === 'ukr' ? "Якщо хочеш стати дистриб’ютором, партнером чи маєш ідею для колаборації, то виходь на зв’язок з нами!" : "If you want to become a distributor, partner or have an idea for collaboration, get in touch with us!"}}</p>-->
<!--    <div class="media-block">-->
<!--      <Button :background="'transparent'" :color="'171717'">{{lang === 'ukr' ? "стати партнером" : "become a partner"}}</Button>-->
<!--      <img src="../assets/product.png" alt="product">-->
<!--    </div>-->
<!--  </div>-->
<!--</template>-->

<script>

import Button from "@/components/base/Button";
import {ref} from "vue";
export default {
  name: 'PartnerSection',
  components: {
    Button
  },
  setup() {

    let lang = ref(localStorage.getItem('lang'))

    return { lang }
  }
}
</script>

<style scoped lang="scss">

.last-text {
  padding: 16px 0 40px;
}

.text-partner {
  padding-bottom: 16px;
}

.media-block {
  display: grid;
  align-items: start;
  grid-template-columns: auto 1fr;
  gap: 20px;
  justify-items: center;
}

.partner-section {
  padding: 32px 40px 40px;
  background: #E8E8E8;
  border-radius: 24px;
}

</style>
