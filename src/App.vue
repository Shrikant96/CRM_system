<template>
  <div id="app">

    <router-view />
  </div>
</template>

<style lang="scss">


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height:100%;
  width: 100%;
  // text-align: center;
  color: #2c3e50;
  @import url('https://fonts.googleapis.com/css2?family=Roboto:ital@1&display=swap');
  @import url('https://fonts.googleapis.com/css2?family=Oswald:wght@500&display=swap');

}
body{
  height:100%;
  width: 100%;
  
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
