<template>
  <div id="header">
    <h3>TODO List</h3>
  </div>
</template>

<script>
export default {
  name: 'Header',
};
</script>

<style scoped>

#header {
  text-align:center;
  background: #e9e9e9;
  border-bottom: 1px solid #bbbbbb;
  margin: 0 0 20px 0;
  box-shadow:0 0 15px #999999;
}

h3 {
  font-weight: 800;
  font-size: 24px;
  padding: 20px;
  color: #333;
  margin: 0;
  text-shadow: 0 1px 0 #fff;
}

</style>
