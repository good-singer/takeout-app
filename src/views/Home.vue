<template>
  <div class="home">
    <div class="header">
      <div class="address_map" @click="$router.push('/address')">
        <i class="fa fa-map-marker"></i>
        <span>{{address || '正在获取...'}}</span>
        <i class="fa fa-sort-desc"></i>
      </div>
      <div class="shop_search">
        <i class="fa fa-search"></i>
        搜索商家&nbsp;商家名称
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "home",
  computed: {
    address(){
      return this.$store.getters.address;
    }
  }
}
</script>

<style scoped>
.home {
  width: 100%;
  height: 100%;
  overflow: auto;
  box-sizing: border-box;
}
.header {
  background-color: #009eef;
  padding: 16px;
}
.header .address_map {
  color: #fff;
  font-weight: bold;
}
.address_map i {
  margin: 0 3px;
  font-size: 18px;
}
.address_map span {
  display: inline-block;
  width: 80%;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.header .shop_search {
  margin-top: 10px;
  background-color: #fff;
  padding: 10px 0;
  border-radius: 4px;
  text-align: center;
  color: #aaa;
}
</style>
