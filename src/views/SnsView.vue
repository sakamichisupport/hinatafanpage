<template>
<h1 class="title">SNS</h1>
<h2>X</h2>
<a href="https://twitter.com/hinatazaka46" target="_blank" rel="noopener noreferrer" class="sns-list">日向坂46公式X</a>
<h2>YouTube</h2>
<a href="https://www.youtube.com/channel/UCR0V48DJyWbwEAdxLL5FjxA" target="_blank" rel="noopener noreferrer" class="sns-list">日向坂46 OFFICIAL YouTube CHANNEL </a><br>
<a href="https://www.youtube.com/@hinatazakachannel/featured" target="_blank" rel="noopener noreferrer" class="sns-list">日向坂ちゃんねる</a>
<h2>Instagram</h2>
<ul>
  <li v-for="(link, index) in links" :key="index">
    <a :href="link.url" target="_blank" rel="noopener noreferrer" class="sns-list">{{ link.text }}</a>
  </li>
</ul>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'SnsView',
  components: {
  },
  data() {
    return {
      links: [
        { text: '加藤史帆', url: 'https://www.instagram.com/katoshi.official' },
        { text: '佐々木久美', url: 'https://instagram.com/kumisasaki_' },
        { text: '佐々木美玲', url: 'https://instagram.com/mireisasaki_official' },
        { text: '高本彩花', url: 'https://instagram.com/ayacheri._.official' },
        { text: '東村芽依', url: 'https://instagram.com/mei.higashimura' },
        { text: '金村美玖', url: 'https://instagram.com/miku_osushi' },
        { text: '河田陽菜', url: 'https://instagram.com/hina17_kawata' },
        { text: '富田鈴花', url: 'https://instagram.com/suzy.tomita' },
        { text: '丹生明里', url: 'https://instagram.com/nibuchan_akari' },
        { text: '濱岸ひより', url: 'https://instagram.com/hiyotan928_official"' },
        { text: '松田好花', url: 'https://instagram.com/matsudakonoka.yahos' },
        { text: '上村ひなの', url: 'https://www.instagram.com/hinanokamimura.official' },
        { text: '森本茉莉', url: 'https://www.instagram.com/mariemorimoto_official' },
        { text: '髙橋未来虹', url: 'https://www.instagram.com/mikuni.takahashi__' }
      ]
    }
  }
}
</script>

<style>
li {
  list-style: none;
}

</style>