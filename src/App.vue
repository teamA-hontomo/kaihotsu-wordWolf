<template>
  <div>
    <p>IDを入力してください</p>
    <input v-model="myId" />
    <p>{{showWord}}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      ids: {
        "9Cm2H6bULBtnFKOBMool": 0,
        "EjF12B6bV3sIfqip9yQH": 1,
        "KUiVOqJihJX0f53SyNJy": 0,
        "VeiWjmFllSNlbdN93FXQ": 0,
        "YHaGGw6iVyVn4Kh80u3G": 0,
      },
      words: ["絵本", "漫画"],
      myId: "",
    };
  },

  computed: {
    showWord() {
      return this.words[this.ids[this.myId]];
    },
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
