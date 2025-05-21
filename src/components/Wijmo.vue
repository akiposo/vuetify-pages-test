<!-- eslint-disable vue/attribute-hyphenation -->
<template>
  <div>
    <h1>Wijmo Flex Grid Quick Start</h1>
  </div>
  <wj-flex-grid :itemsSource="gridData">
    <wj-flex-grid-column binding="id" header="ID" :width="60" />
    <wj-flex-grid-column binding="product" header="商品名" :width="200" />
    <wj-flex-grid-column binding="date" header="受注日" :width="120" />
    <wj-flex-grid-column binding="amount" format="c" header="金額" :width="100" />
  </wj-flex-grid>
</template>

<script setup>
  //WjFlexGridコンポーネントをインポートします。
  import { WjFlexGrid } from '@grapecity/wijmo.vue2.grid';
  //日本語化カルチャをインポートします。
  import '@grapecity/wijmo.cultures/wijmo.culture.ja';

  //グリッド用のデータを定義します。
  const gridData = [
    { id: 15, product: 'ピュアデミグラスソース', date: '2022/10/19', amount: 6000 },
    { id: 17, product: 'だしこんぶ', date: '2022/10/19', amount: 14500 },
    { id: 18, product: 'ピリカラタバスコ', date: '2022/10/19', amount: 4000 },
    { id: 84, product: 'なまわさび', date: '2022/10/19', amount: 8000 },
  ]
</script>

<style>
  /* Wijmoのスタイルファイルをインポートします */
  @import '@grapecity/wijmo.styles/wijmo.css';
</style>
