<template>
  <div>
    <span v-html="tiktok" ref="tiktokRef"></span>
  </div>
</template>

<script lang="ts" setup>
useHead({
  script: [
      { src: 'https://www.tiktok.com/embed.js', async: true}
  ]
})

const tiktok: Ref<string | null> = ref(null)
const tiktokRef: Ref = ref(null)

//const delay = async (n: number) => {
//  return new Promise((resolve) => {
//  setTimeout(resolve,n * 1000)
//  })
//}

const loadTikTok = async () => {
  // await delay(1)
  return '<blockquote class="tiktok-embed" cite="https://www.tiktok.com/@daiquirihf/video/7320076560076246318" data-video-id="7320076560076246318" style="max-width: 605px;min-width: 325px;" > <section> <a target="_blank" title="@daiquirihf" href="https://www.tiktok.com/@daiquirihf?refer=embed">@daiquirihf</a> How to Really Use a KATANA 🥷💀 <a title="drill" target="_blank" href="https://www.tiktok.com/tag/drill?refer=embed">#drill</a> <a title="katana" target="_blank" href="https://www.tiktok.com/tag/katana?refer=embed">#KATANA</a> <a title="greatmaster" target="_blank" href="https://www.tiktok.com/tag/greatmaster?refer=embed">#greatmaster</a> <a title="warrior" target="_blank" href="https://www.tiktok.com/tag/warrior?refer=embed">#warrior</a> <a title="fight" target="_blank" href="https://www.tiktok.com/tag/fight?refer=embed">#fight</a> <a title="boxing" target="_blank" href="https://www.tiktok.com/tag/boxing?refer=embed">#boxing</a> <a title="viral" target="_blank" href="https://www.tiktok.com/tag/viral?refer=embed">#viral</a> <a title="viralvideo" target="_blank" href="https://www.tiktok.com/tag/viralvideo?refer=embed">#viralvideo</a> <a title="fyp" target="_blank" href="https://www.tiktok.com/tag/fyp?refer=embed">#fyp</a> <a title="foryou" target="_blank" href="https://www.tiktok.com/tag/foryou?refer=embed">#foryou</a> <a title="foryoupage" target="_blank" href="https://www.tiktok.com/tag/foryoupage?refer=embed">#foryoupage</a> <a target="_blank" title="♬ Devil Emperor Phonk - Bgnzinho" href="https://www.tiktok.com/music/Devil-Emperor-Phonk-7200424038450071554?refer=embed">♬ Devil Emperor Phonk - Bgnzinho</a> </section> </blockquote>'
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