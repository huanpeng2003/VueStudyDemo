<template>
  <div id="app">
    <a-button type="primary" @click="btnClick">dianji</a-button>
    <input type="text" v-model="msg">
    <div id="nav" class="row">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
  export default{
    data(){
        return{
          msg:"hello"
        }
    },
    methods:{
      btnClick(){
        alert(this.msg)
      }
    }
  }

</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
