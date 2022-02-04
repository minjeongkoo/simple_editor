<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/Editor">Text Editor</router-link>
      <router-link to="/about">Gif Testing</router-link>
    </div>
    <router-view/>
  </div>
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

body {
  margin: 0;
}

#app {
  font-family: 'Poppins', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
}

body, #app {
  background-color: #20262c;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #fff;
  margin: 12px;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

a {
  text-decoration: none;
}

</style>
