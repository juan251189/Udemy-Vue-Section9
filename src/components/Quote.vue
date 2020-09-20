<template>
  <div id="">
    <div>
       <slot name="title"></slot>
        <span style="color:#ccc;" slot="subtitle">Some Subtitle</span>
    </div>
    <hr>
    <div>
      <slot name="content"></slot>
    </div>
  </div>
</template>
<script>
export default {

  data: () => ({

  }),
  props:['quote']
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
