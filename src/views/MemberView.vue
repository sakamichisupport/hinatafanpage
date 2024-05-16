<template>
<div class="wrapper">
  <h1 class="title">MEMBER</h1>
  <div id="app" class="container mt-5">
  <ul class="nav nav-tabs">
    <li class="nav-item" v-for="(category, index) in categories" :key="index">
      <a class="nav-link" :class="{ 'active': activeCategory === index }" @click="activeCategory = index">{{ category.name }}</a>
    </li>
  </ul>
  <div v-for="(category, index) in categories" :key="index" v-show="activeCategory === index">
    <h3>{{ category.name }}</h3>
    <ul class="nav nav-tabs">
      <li class="nav-item" v-for="(tab, tabIndex) in category.tabs" :key="tabIndex">
        <a class="nav-link" :class="{ 'active': activeTab[index] === tabIndex }" @click="activeTab[index] = tabIndex">{{ tab.name }}</a>
      </li>
    </ul>
    <div class="tab-content mt-3">
      <div class="tab-pane" :class="{ 'active': activeTab[index] === tabIndex }" v-for="(tab, tabIndex) in category.tabs" :key="tabIndex">
        <h4>{{ tab.name }}</h4>
        <p>{{ tab.birth }}</p>
        <img :src="tab.image" alt="" class="img-fluid">
      </div>
    </div>
  </div>
</div>
</div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'MemberView',
  components: {
  },
  data() {
    return {
      activeCategory: 0,
      activeTab: [],
      categories: [
        {
          name: '一期生',
          tabs: [
            { name: '加藤史帆', birth:'1998年2月2日', image: require('@/assets/shiho.jpg') },
            { name: '佐々木久美', birth: '1996年1月22日', image: require('@/assets/kumi.jpg') },
            { name: '佐々木美玲', birth: '1999年12月17日', image: require('@/assets/mirei.jpg') },
            { name: '高瀬愛奈', birth: '1998年9月20日', image: require('@/assets/mana.jpg') },
            { name: '高本彩花', birth: '1998年11月2日', image: require('@/assets/ayaka.jpg') },
            { name: '東村芽依', birth: '1998年8月23日', image: require('@/assets/mei.jpg' )},
          ]
        },
        {
          name: '二期生',
          tabs: [
            { name: '金村美玖', birth: '2002年9月10日', image: require('@/assets/miku.jpg') },
            { name: '河田陽菜', birth: '2001年7月23日', image: require('@/assets/hina.jpg') },
            { name: '小坂菜緒', birth: '2002年9月7日', image: require('@/assets/nao.jpg' )},
            { name: '富田鈴花', birth: '2001年1月18日', image: require('@/assets/suzuka.jpg') },
            { name: '丹生明里', birth: '2001年2月15日', image: require('@/assets/akari.jpg')},
            { name: '濱岸ひより', birth: '2002年9月28日', image: require('@/assets/hiyori.jpg') },
            { name: '松田好花', birth: '1999年4月27日', image: require('@/assets/konoka.jpg') },
          ]
        },
        {
          name: '三期生',
          tabs: [
            { name: '上村ひなの', birth: '2004年4月12日', image: require('@/assets/hinano.jpg') },
            { name: '髙橋未来虹', birth: '2003年9月27日', image: require('@/assets/mikuni.jpg') },
            { name: '森本茉莉', birth: '2004年2月23日', image: require('@/assets/marie.jpg')},
            { name: '山口陽世', birth: '2004年2月23', image: require('@/assets/haruyo.jpg') }
          ]
        },
        {
          name: '四期生',
          tabs: [
            { name: '石塚瑶季', birth: '2004年8月6日', image: require('@/assets/tamaki.jpg') },
            { name: '小西夏菜実', birth: '2004年10月3日', image: require('@/assets/nanami.jpg') },
            { name: '清水理央', birth: '2005年1月15日', image: require('@/assets/rio.jpg')},
            { name: '正源司陽子', birth: '2007年2月14日', image: require('@/assets/yoko.jpg') },
            { name: '竹内希来里', birth: '2006年2月20日', image: require('@/assets/kirari.jpg') },
            { name: '平尾帆夏', birth: '2003年7月31日', image: require('@/assets/hiraho.jpg') },
            { name: '平岡海月', birth: '2002年4月9日', image: require('@/assets/mitsuki.jpg') },
            { name: '藤嶌果歩', birth: '2006年8月7日', image: require('@/assets/kaho.jpg') },
            { name: '宮地すみれ', birth: '2005年12月31日', image: require('@/assets/sumire.jpg') },
            { name: '山下葉留花', birth: '2003年5月20日', image: require('@/assets/haruka.jpg') },
            { name: '渡辺莉奈', birth: '2009年2月7日', image: require('@/assets/rina.jpg') }
          ]
        },
      ]
    };
  },
  created() {
    this.activeTab = new Array(this.categories.length).fill(0);
  }
}
</script>