<template>
  <div id="happy">
    <div>
       <h1>{{quoteTitle}}</h1>
        <span style="color:#ccc;" slot="subtitle">Some Subtitle</span>
    </div>
    <hr>
    
  </div>
</template>
<script>
export default {

  data: () => ({

  }),
  props:['quoteTitle']
}
</script>
<style  scoped>
    div{
      border:1px solid #ccc;
      box-shadow: 1px 1px 2px black;
      padding: 30px;
      margin:auto;
    }
    h2{
      color:red;
    }
</style>
