<template>
  <div class="hello">
    <h6>Menu3</h6>
    <ul>
      <li><router-link :to=" { name: 'root' }">Home1</router-link></li>
     <!-- <li><router-link :to=" { name: 'login' }">login</router-link></li>
	  <li><router-link :to=" { name: 'login' }">Login</router-link></li> -->
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
