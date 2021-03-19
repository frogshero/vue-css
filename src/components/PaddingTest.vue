<template>
  <div style="text-align: center">  
      <input class="input2">  
    <div class="content2">
      <input class="input2" style="width:50px; margin-right:5px">  
      <input class="input2" style="width:150px; margin-right:5px">  
      <input class="input2" style="width:100px; margin-right:5px">  
      <input class="input2" style="width:80px; margin-right:25px">  
      <button class="button2" style="margin-right:5px">Submit</button>
      <button class="button2" style="margin-right:5px">Cancel</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PaddingTest',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .button2 {
    width:100px; 
    height: 40px;
    /* background-color: white; */
  }

  .content2 {
    /*flex元素自动一行排列*/
    display: flex;
    /* justify-content: space-between; */
  }
  
  .input2 {
    /*为元素设定的宽度和高度决定了元素的边框盒。不然实际高度会高一点*/
    box-sizing: border-box;
    height: 40px;
    line-height: 40px;
    width: 200px;
    font-size: 16px;
  }
</style>
