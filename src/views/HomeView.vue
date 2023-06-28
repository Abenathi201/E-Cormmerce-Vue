<template>
  <HeroComp/>
  <MainSection />
</template>

<script>
// @ is an alias to /src
import MainSection from '@/components/MainSection.vue'
import HeroComp from '@/components/HeroComp.vue'

export default {
  name: 'HomeView',
  components: {
    MainSection,
    HeroComp
  }
}
</script>
