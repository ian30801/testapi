<template>
  <div id="nav">
    <!-- <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link> -->
<!-- 
     <div>
       <p>第一題</p>
     <input>
     <ul></ul></div><div><p>第二題</p>
     <select>
       <option>臺北市</option>
       <option>臺中市</option>
       <option>高雄市</option>
       </select>
       <select>
         </select>
         <select>
         </select>
         <ul>
         </ul>
         </div> -->
         </div>
  <!-- <router-view/> -->
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>

<script>
export default {
  data(){},
  mounted() {
    let data={};
    const url='https://www.twingo.com.tw:8443/search/getPostalCodeData';
     this.$http.get(url)
        .then((response) => {
          console.log(response);
          data=response;
          console.log(data);
        });
  }, 
  created() {
    // this.getAddress();
    // console.log(process.env.VUE_APP_API);
    // console.log(this.$route.params);
  },
  methods: {
    // getAddress() {
    //   this.$http.get('https://www.twingo.com.tw:8443/search/getPostalCodeData')
    //     .then((res) => {
    //       console.log(res);
    //     });
    // },
  },
};
</script>
