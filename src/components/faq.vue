<template lang="pug">
.faq-section
  .group-tab(@click="question1 = !question1")
    h2 {{lang === &apos;ukr&apos; ? &quot;Хто такі SAB?&quot; : &quot;Who are SAB?&quot;}}
    p {{question1 ? &quot;+&quot; : &quot;-&quot;}}
  Collapse.question-tab(:when="question1")
    p {{lang === &apos;ukr&apos; ? &quot;Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій.&quot; : &quot;Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own.&quot;}}
  hr.line
  .group-tab(@click="question2 = !question2")
    h2 {{lang === &apos;ukr&apos; ? &quot;Чим SAB відрізняється від інших електронних сигарет&quot; : &quot;What makes SAB different from other e-cigarettes?&quot;}}
    p {{question2 ? &quot;+&quot; : &quot;-&quot;}}
  Collapse.question-tab(:when="question2")
    p {{lang === &apos;ukr&apos; ? &quot;Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій.&quot; : &quot;Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own.&quot;}}
  hr.line
  .group-tab(@click="question3 = !question3")
    h2 {{lang === &apos;ukr&apos; ? &quot;З чого складається SAB?&quot; : &quot;What does SAB consist of?&quot;}}
    p {{question3 ? &quot;+&quot; : &quot;-&quot;}}
  Collapse.question-tab(:when="question3")
    p {{lang === &apos;ukr&apos; ? &quot;Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій.&quot; : &quot;Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own.&quot;}}
  hr.line
  .group-tab(@click="question4 = !question4")
    h2 {{lang === &apos;ukr&apos; ? &quot;Чи дійсно SAB має такі хороші технології?&quot; : &quot;Does SAB really have that good technology?&quot;}}
    p {{question4 ? &quot;+&quot; : &quot;-&quot;}}
  Collapse.question-tab(:when="question4")
    p {{lang === &apos;ukr&apos; ? &quot;Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій.&quot; : &quot;Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own.&quot;}}
  hr.line
  .group-tab(@click="question5 = !question5")
    h2 {{lang === &apos;ukr&apos; ? &quot;Де я можу знайти SAB?&quot; : &quot;Where can I find SAB?&quot;}}
    p {{question5 ? &quot;+&quot; : &quot;-&quot;}}
  Collapse.question-tab(:when="question5")
    p {{lang === &apos;ukr&apos; ? &quot;Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій.&quot; : &quot;Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own.&quot;}}
  hr.line
  .group-tab(@click="question6 = !question6")
    h2 {{lang === &apos;ukr&apos; ? &quot;Я зацікавлений у партнерстві з SAB у своєму магазині чи бізнесі, до кого мені звернутися?&quot; : &quot;I am interested in partnering with SAB for my store or business, who should I contact?&quot;}}
    p {{question6 ? &quot;+&quot; : &quot;-&quot;}}
  Collapse.question-tab(:when="question6")
    p {{lang === &apos;ukr&apos; ? &quot;Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій.&quot; : &quot;Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own.&quot;}}
  hr.line
</template>

<!--<template>-->
<!--  <div class="faq-section">-->

<!--    <div class="group-tab" @click="question1 = !question1">-->
<!--      <h2>{{lang === 'ukr' ? "Хто такі SAB?" : "Who are SAB?"}}</h2>-->
<!--      <p>{{question1 ? "+" : "-"}}</p>-->
<!--    </div>-->
<!--    <Collapse :when="question1" class="question-tab">-->
<!--      <p>{{lang === 'ukr' ? "Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій." : "Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own."}}</p>-->
<!--    </Collapse>-->
<!--    <hr class="line">-->

<!--    <div class="group-tab" @click="question2 = !question2">-->
<!--      <h2>{{lang === 'ukr' ? "Чим SAB відрізняється від інших електронних сигарет" : "What makes SAB different from other e-cigarettes?"}}</h2>-->
<!--      <p>{{question2 ? "+" : "-"}}</p>-->
<!--    </div>-->
<!--    <Collapse :when="question2" class="question-tab">-->
<!--      <p>{{lang === 'ukr' ? "Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій." : "Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own."}}</p>-->
<!--    </Collapse>-->
<!--    <hr class="line">-->

<!--    <div class="group-tab" @click="question3 = !question3">-->
<!--      <h2>{{lang === 'ukr' ? "З чого складається SAB?" : "What does SAB consist of?"}}</h2>-->
<!--      <p>{{question3 ? "+" : "-"}}</p>-->
<!--    </div>-->
<!--    <Collapse :when="question3" class="question-tab">-->
<!--      <p>{{lang === 'ukr' ? "Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій." : "Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own."}}</p>-->
<!--    </Collapse>-->
<!--    <hr class="line">-->

<!--    <div class="group-tab" @click="question4 = !question4">-->
<!--      <h2>{{lang === 'ukr' ? "Чи дійсно SAB має такі хороші технології?" : "Does SAB really have that good technology?"}}</h2>-->
<!--      <p>{{question4 ? "+" : "-"}}</p>-->
<!--    </div>-->
<!--    <Collapse :when="question4" class="question-tab">-->
<!--      <p>{{lang === 'ukr' ? "Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій." : "Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own."}}</p>-->
<!--    </Collapse>-->
<!--    <hr class="line">-->

<!--    <div class="group-tab" @click="question5 = !question5">-->
<!--      <h2>{{lang === 'ukr' ? "Де я можу знайти SAB?" : "Where can I find SAB?"}}</h2>-->
<!--      <p>{{question5 ? "+" : "-"}}</p>-->
<!--    </div>-->
<!--    <Collapse :when="question5" class="question-tab">-->
<!--      <p>{{lang === 'ukr' ? "Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій." : "Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own."}}</p>-->
<!--    </Collapse>-->
<!--    <hr class="line">-->

<!--    <div class="group-tab" @click="question6 = !question6">-->
<!--      <h2>{{lang === 'ukr' ? "Я зацікавлений у партнерстві з SAB у своєму магазині чи бізнесі, до кого мені звернутися?" : "I am interested in partnering with SAB for my store or business, who should I contact?"}}</h2>-->
<!--      <p>{{question6 ? "+" : "-"}}</p>-->
<!--    </div>-->
<!--    <Collapse :when="question6" class="question-tab">-->
<!--      <p>{{lang === 'ukr' ? "Наші клієнти кажуть, що смаки SAB максимально близькі до справжніх. Для нас це найкращий показник того, що ми зробили правильний вибір матеріали, технологія створення рідин і виробів. Ми не виходимо за стандарти, встановлені ринком. А ми створюємо свій." : "Our customers say that SAB tastes as close to the real thing as possible. For us, this is the best indicator that we have made the right choice of materials, technology for creating liquids and products. We do not go beyond the standards set by the market. And we create our own."}}</p>-->
<!--    </Collapse>-->
<!--    <hr class="line">-->

<!--  </div>-->
<!--</template>-->

<script>
import { ref } from "vue";
import { Collapse } from 'vue-collapsed'
export default {
  name: 'FaqSection',
  components: {
    Collapse
  },

  setup() {

    let lang = ref(localStorage.getItem('lang'))

    const question1 = ref(false)
    const question2 = ref(true)
    const question3 = ref(false)
    const question4 = ref(false)
    const question5 = ref(false)
    const question6 = ref(false)

    return { question1, question2, question3, question4, question5, question6, lang }
  }
}
</script>

<style scoped lang="scss">

h2 {
  cursor: pointer;
}

.group-tab {
  display: grid;
  grid-template-columns: repeat(2, auto);
  align-items: center;
  justify-content: space-between;
}

.line {
  margin: 20px 0;
  opacity: .3;
}

.group-tab {
  cursor: pointer;
}

.group-tab p {
  font-size: 30px;
  font-family: auto;
}

.question-tab {
  transition: height 300ms cubic-bezier(0.3, 0, 0.6, 1);
}

.question-tab p {
  padding: 10px 0 0;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 140%;
  letter-spacing: -0.01em;
  color: #8B8B8B;
}

</style>
