<template>
  <div>
    <span v-html="tiktok"></span>
  </div>
</template>

<script lang="ts" setup>
useHead({
  script: [
      { src: 'https://www.tiktok.com/embed.js', async: true}
  ]
})

const tiktok: Ref<string | null> = ref(null)
//const tiktokRef: Ref = ref(null)

//const delay = async (n: number) => {
//  return new Promise((resolve) => {
//  setTimeout(resolve,n * 1000)
//  })
//}

const loadTikTok = async () => {
  // await delay(1)
  return '<blockquote class="tiktok-embed" cite="https://www.tiktok.com/@kaginowo.japan.official/video/7474132266386476310" data-video-id="7474132266386476310" style="max-width: 605px;min-width: 325px;" > <section> <a target="_blank" title="@kaginowo.japan.official" href="https://www.tiktok.com/@kaginowo.japan.official?refer=embed">@kaginowo.japan.official</a> <p>#くら寿司バズっちゃうよ#くら寿司#これダメでしょ</p> <a target="_blank" title="♬ nhạc nền  - カギノヲ" href="https://www.tiktok.com/music/nhạc-nền-カギノヲ-7474132253790997270?refer=embed">♬ nhạc nền  - カギノヲ</a> </section> </blockquote>'
}

tiktok.value = await loadTikTok()

//onMounted(()=>{
//  var script = document.createElement('script');
//  script.src = 'https://www.tiktok.com/embed.js';
//  tiktokRef.value.appendChild(script);
//})

</script>


<style>

</style>