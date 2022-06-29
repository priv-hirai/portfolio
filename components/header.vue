<template>
  <div class="header h100 w100">
    <h2>ヘッダー</h2>
    <ul>
      <li>コンテンツ</li>
      <li>a</li>
      <li>a</li>
      <li>a</li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'header'
}
</script>
<style scoped>
.header {
  display: flex;
  border-right: solid 1px #caddde;
  background-color: #caddde;
  max-height: 130px;
  position: fixed;
  top: 0;
  z-index: 10;
}

.header ul {
  display: flex;
}
</style>
