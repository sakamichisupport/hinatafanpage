<template>
    <h1 class="title">DISCOGRAPHY</h1>
  <h2>SINGLE</h2>
  <div id="app" class="container mt-5">
    <table class="table">
      <thead>
        <tr>
          <th>#</th>
          <th>タイトル</th>
          <th>リリース日</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user, index) in singles" :key="index" >
          <td>{{ user.id }}</td>
          <td>{{ user.name }}</td>
          <td>{{ user.release }}</td>
        </tr>
      </tbody>
    </table>
    <h2>ALBUM</h2>
    <table class="table">
      <thead>
        <tr>
          <th>#</th>
          <th>タイトル</th>
          <th>リリース日</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user, index) in albums" :key="index" >
          <td>{{ user.id }}</td>
          <td>{{ user.name }}</td>
          <td>{{ user.release }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
// @ is an alias to /src
export default {
  name: 'DiscographyView',
  components: {
  },
  data() {
    return {
      singles: [
        { id: 1, name: 'キュン', release: '2019年3月27日' },
        { id: 2, name: 'ドレミソラシド', release: '2019年7月17日' },
        { id: 3, name: 'こんなに好きになっちゃっていいの', release: '2019年10月2日' },
        { id: 4, name: 'ソンナコトナイヨ', release: '2020年2月19日' },
        { id: 5, name: '君しか勝たん', release: '2021年5月26日' },
        { id: 6, name: 'ってか', release: '2021年10月27日' },
        { id: 7, name: '僕なんか', release: '2022年6月1日' },
        { id: 8, name: '月と星が踊るMidnight', release: '2022年10月26日' },
        { id: 9, name: 'One choice', release: '2023年4月19日' },
        { id: 10, name: 'Am I ready?', release: '2023年7月26日' },
        { id: 11, name: '君はハニーデュー', release: '2024年5月8日' }
      ],
      albums: [
        { id: 1, name: '走り出す瞬間', release: '2018年6月20日' },
        { id: 2, name: 'ひなたざか', release: '2020年9月23日' },
        { id: 3, name: '脈打つ感情', release: '2023年11月8日' }
      ],
    }
  }
}
</script>
