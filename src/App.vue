<template>
  <div>
    <h1>2021-10-31 天皇賞・秋</h1>
    <table class='horse-info-table'>
      <thead>
        <tr>
          <th v-for="(header, index) in headers"
              v-bind:key="index">
            {{header.text}}
          </th>
        </tr>
      </thead>
      <tbody>
      <tr v-for="(horseRecord, index) in horseRecords"
          v-bind:key="horseRecord.horseNumber">
        <th>{{index + 1}}</th>
        <td>{{horseRecord.horseNumber}}</td>
        <td>{{horseRecord.horseName}}</td>
        <td>{{horseRecord.tanshoOdds}}</td>
      </tr>
    </tbody>
    </table>
    <div class="obj-horses">
      <p>1頭目</p>
      <input v-model="message" class="sanrenpuku-1st"><br>
      <p>2頭目</p>
      <input v-model="message" class="sanrenpuku-2nd"><br>
      <p>3頭目</p>
      <input v-model="message" class="sanrenpuku-3rd">
    </div>

  </div>
</template>

<script>
  export default {
    data () {
      return {
        headers: [
          { text: 'No.', value: 'index'},
          { text: '馬番', value: 'horseNumber'},
          { text: '馬名', value: 'horseName' },
          { text: '単勝オッズ', value: 'tanshoOdds' }
        ],
        horseRecords: [
          {
            horseNumber: 1,
            horseName: 'コントレイル',
            tanshoOdds: 2.5
          },
          {
            horseNumber: 2,
            horseName: 'カデナ',
            tanshoOdds: 257.8
          },          
          {
            horseNumber: 3,
            horseName: 'モズベッロ',
            tanshoOdds: 104.6
          },          
          {
            horseNumber: 4,
            horseName: 'ポタジェ',
            tanshoOdds: 23.3
          },          
          {
            horseNumber: 5,
            horseName: 'エフフォーリア',
            tanshoOdds: 3.4
          },          
          {
            horseNumber: 6,
            horseName: 'トーセンスーリヤ',
            tanshoOdds: 67.1
          },
          {
            horseNumber: 7,
            horseName: 'ワールドプレミア',
            tanshoOdds: 30.2
          },
          {
            horseNumber: 8,
            horseName: 'サンレイポケット',
            tanshoOdds: 113.5
          },
          {
            horseNumber: 9,
            horseName: 'グランアレグリア',
            tanshoOdds: 2.8
          },
          {
            horseNumber: 10,
            horseName: 'カイザーミノル',
            tanshoOdds: 67.1
          },
          {
            horseNumber: 11,
            horseName: 'ムイトオブリガード',
            tanshoOdds: 332.6
          },
          {
            horseNumber: 12,
            horseName: 'ラストドラフト',
            tanshoOdds: 190.4
          },
          {
            horseNumber: 13,
            horseName: 'ペルシアンナイト',
            tanshoOdds: 159.1
          },
          {
            horseNumber: 14,
            horseName: 'カレンブーケドール',
            tanshoOdds: 19.6
          },
          {
            horseNumber: 15,
            horseName: 'ヒシイグアス',
            tanshoOdds: 40.4
          },
          {
            horseNumber: 16,
            horseName: 'ユーキャンスマイル',
            tanshoOdds: 153.0
          },

        ],
      }
    },
  }
</script>

<style>
h1 {
  color:gray;
}

table {
  float: left;
  border: solid 1px #ccc;
  border-collapse:collapse;
}
th {
  padding: 5px;
  border: solid 1px #ccc;
  background-color: #eee;
}
td {
  padding: 5px;
  border: solid 1px #ccc;
}

input {
  float: left;
  border: 2px solid black; /*枠線*/
}

.obj-horses div   {
  margin-left: 100px;
}

</style>