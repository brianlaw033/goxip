<template>
  <div id="nav">
    <div class="title">SHOPSTYLE</div>
    <div id="search-bar">
      <el-input placeholder="What are you looking for?" v-model="input">
        <el-button class="submit" slot="append" icon="el-icon-search"></el-button>
      </el-input>
      <el-select v-model="category" placeholder="Select">
        <el-option label="All" value="0"></el-option>
        <el-option label="Women" value="1"></el-option>
        <el-option label="Men" value="2"></el-option>
        <el-option label="Kids" value="3"></el-option>
        <el-option label="Home" value="4"></el-option>
      </el-select>
    </div>
    <div class="auth-btn">Join Now</div>
    <div class="auth-btn">Log In</div>
  </div>
</template>

<style scoped lang="scss">
  #nav {
    display: flex;
    justify-content: space-between;
    align-items: center;

    .title {
      font-size: 1.4rem;
    }

    #search-bar {
      position: relative;
      width: 40vw;

      .el-select {
        position: absolute;
        right: 58px;
        width: 80px;

        input {
          background-color: transparent;
          border: none;
        }
      }
    }

    .auth-btn {
      background-color: #000;
      color: #fff;
      height: 40px;
      width: 80px;
      display: flex;
      justify-content: center;
      align-items: center;
    }

  }

</style>

<script>

export default {
  name: 'NavBar',
  data() {
    return {
      input: '',
      category: '0',
    };
  },
};
</script>
