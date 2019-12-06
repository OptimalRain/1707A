<template>
  <div id="app">
    <div class="con">
      <router-view/>
    </div>
    
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </div>
</template>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  list-style: none;
}
html,body,#app{
  width: 100%;
  height: 100%;
}
#app{
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
.con{
  flex:1;
  overflow: auto;
}
#nav{
  width: 100%;
  height: 40px;
  display: flex;
  a{
    flex:1;
    text-align: center;
    line-height: 40px;
  }
}
</style>
