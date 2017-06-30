<template>
  <div class="hello">
    <mt-button type="primary" class="mb" @click="getAccess">获取access_token</mt-button>
    <mt-button type="primary">接收普通消息1</mt-button>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {

    }
  },
  methods:{
    getAccess(){
        this.$http.get('https://api.weixin.qq.com/cgi-bin/token?grant_type=client_credential&appid=wx4478a40d181f2c25&secret=47c5ef55250ea671437a292d97cc4fc1').then(data=>{
            console.log(data);
        })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .mb{margin-bottom: 10px;}
h1, h2 {
  font-weight: normal;
}
0
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
