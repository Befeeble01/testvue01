<template>  
  <div id="app">
  {{ posts }}
</div>
</template>

<script>   
var dataURL = 'https://jsonplaceholder.typicode.com/posts';

var App = new Vue({
  el: '#app',
  data: {
    posts: [] // initialize empty array
  },
  mounted() { // when the Vue app is booted up, this is run automatically.
    var self = this // create a closure to access component in the callback below
    $.getJSON(dataURL, function(data) {
      self.posts = data;
    });
  }
})
</script>

<style>  
.test-list {
  font-family: Roboto;
  list-style: none;
  margin: 20px auto;
  width: 50%;
}

.test-list--item {
  border: 1px solid rgb(41, 41, 41);
  border-radius: 5px;
  text-align: center;
  display: block;
  box-shadow: 2px 2px rgba(138, 124, 124, 0.4);
}

.test-list--id {
  font-weight: 300;
  margin: 10px auto;
}

.test-list--title {
  font-weight: 500;
  margin: 20px auto;
  text-transform: capitalize;
}

.test-list--complete {
  font-weight: 600;
  margin: 10px auto;
  color: #56ca86;
}

.test-list--incomplete {
  font-weight: 600;
  margin: 10px auto;
  color: #ca5656;
}
</style>  