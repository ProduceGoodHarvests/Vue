<template>
  <div id="root" :class='[this.open ? "isactive" : "unisactive"]'>
    <div class="rootCalss" @click="openTheDown" >
      <span v-show="open">天黑请闭眼</span>
      <span v-show="!open">天亮了</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      open: true,
      msg: "Welcome to Your Vue.js App",
    };
  },
  methods: {
    openTheDown() {
      this.open = !this.open
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#root{
  position: relative;
  text-align: center;
  height: 100%;
  width: 100%;
}
.rootCalss{
  position: absolute;
  left: 50%;
  top: 50%;
  font-size: 100px;
  margin-left: -500px;
  margin-top: -150px;
  height: 300px;
  width: 1000px;
  line-height: 300px;

}
.isactive{
  background: #000;
  color: #fff;
}
.unisactive{
  background: #fff;
  color: #000;
}
h1,
h2 {
  font-weight: normal;
}
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
