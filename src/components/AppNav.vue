<template>
  <div class="hello">
    <h6>MenuMahen</h6>
    <ul>
      <li><router-link :to=" { name: 'root' }">Home1</router-link></li>
      <li><router-link :to=" { name: 'login' }">myloginAppNav</router-link></li>
      <li><router-link :to=" { name: 'login1' }">mylogin1AppNav</router-link></li>
	  <li><router-link :to=" { name: 'login2' }">Login2AppNav</router-link></li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
