<template>
  <div class="hello">
    <h1>{{ text1 }}</h1>
    <h2 v-html="text2"></h2>
    <div :id="text3"></div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data(){
    return{
      text1: "早上好",
      text2: "下午好",
      text3: "晚上好",
    }
  }
}
</script>
