<template>
  <div class="container">
    <div class="header">
      <div class="logo"></div>
      <div class="search">
        <input type="text" class="search_input" @input="searchChange" :value="this.searchWords">
        <button class="search_btn">
          <i class="el-icon-search"></i>
        </button>
        <div class="search_result"></div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  layout: 'ctrip',
  components: {
    
  },
  data() {
    return {
      searchWords: ''
    }
  },
  methods: {
    searchChange(e) {
      console.log(e.target.value)
      this.searchWords = e.target.value || ''
    }
  }
}
</script>

<style lang="scss" scoped>
.container {
  widows: 100%;
  .header {
    width: 80%;
    height: 80px;
    color: #333333;
    margin: 0 auto;
    .logo {
      float: left;
      width: 203px;
      height: 34px;
      background-image: url('../assets/ctriplogo.png');
      background-size: 100% 100%;
      margin: 23px 0;
    }
    .search {
      float: left;
      margin-left: 50px;
      width: 28%;
      font-family: "Microsoft Yahei", Tahoma;
      position: relative;
      .search_input {
        width: 100%;
        height: 28px;
        padding: 0 45px 0 5px;
        line-height: 28px;
        margin: 23px 0;
        font-size: 12px;
        font-family: "Microsoft Yahei", Tahoma;
        border: 1px solid #8ebefc;
        border-radius: 4px;
        box-shadow: 2px 2px 1px 0 rgba(164, 203, 255, 0.25) inset;
        outline: 0 none;
      }
      .search_btn {
          position:absolute;
          top: 23px;
          right: 0;
          width: 42px;
          height: 28px;
          border-radius: 0 4px 4px 0;
          cursor: pointer;
          border: 0 none;
          background-color: #a4cbff;
          background-position: -52px -603px;
          i {
            color: #ffffff;
            line-height: 28px;
          }
      }
    }
  }
}
</style>
