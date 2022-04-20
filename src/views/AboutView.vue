<script>
  import HeroText from "@/components/utils/HeroText.vue"
  import AboutContent from "@/components/about/AboutContent.vue"
  import json from './json/About.json'
  export default {
    data(){
      return {
        aboutData: json
      }
    },
    components: {
      HeroText, AboutContent
    }
  } 
</script>

<template>
    <HeroText
      blueTheme
      subTitle="RS Melinda 2"
      title="About Us"
      content="Various health facilities with state-of-the-art medical equipment and the latest. Making the quality of hospital services the best, safe, comfortable, friendly, effective, and efficient."
    />
    <AboutContent />
</template>
