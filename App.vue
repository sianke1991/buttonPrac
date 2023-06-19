<template>
  <div v-html="buttonHtml" id="buttonHtml">
  </div>
  <div>
    {{buttonHtml}}
  </div>
</template>

<script>

export default {
  name: 'App',
  components: {
  },
  data() {
    return {
      buttonHtml: ""
    }
  },
  created() {
    const link = 'http://google.com';
    const text = 'google.com';
    this.buttonHtml = '<button id="btn" onclick="window.open(\''
                    .concat(link)
                    .concat('\')">')
                    .concat(text)
                    .concat('</button>');
  }
}
</script>

<style>
#buttonHtml {
  width: 140px;
  height: 100px;
  border: 2px solid grey;
  background-color: white;
}
#btn {
  background-color: blue;
  width: 140px;
  height: 100px;
}
</style>
