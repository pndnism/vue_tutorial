<template>
  <v-data-table
    v-model="selected"
    dense
    :headers="headers"
    :items="horseData"
    :single-select="singleSelect"
    item-key="horseNumber"
    :items-per-page="20"
    show-select
    class="elevation-1"
  >
    <template v-slot:top>
        <v-switch
          v-model="singleSelect"
          label="Single select"
          class="pa-3"
        ></v-switch>
    </template>
  </v-data-table>
  
</template>

<script>
  export default {
    data () {
      return {
        singleSelect: false,
        selected: [],
        headers: [
          {
            text: '馬番',
            align: 'start',
            sortable: false,
            value: 'horseNumber',
          },
          { text: '馬名', value: 'horseName' },
          { text: '単勝オッズ', value: 'tanshoOdds' }
        ],
        horseData: [
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