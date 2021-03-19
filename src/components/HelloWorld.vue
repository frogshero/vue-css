<template>
  <div style="text-align: center;">  
    <div style="width:500px">
      <!-- div没有居中，是内容居中 -->      
      <textarea rows="20" cols="20"></textarea>
      <div style="display:inline; vertical-align:top">---------</div>
    </div>    
    <div class="content2">
      <textarea rows="20" cols="20"></textarea>
      <div style="">---------</div>
    </div>
    <div style="width:300px">-ff-</div>
    <!-- 高度适应内容, text-align: center;对div无效-->    
		<div class="textarea" contenteditable="true"></div>

  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<style scoped>
  .content2 {
    /*flex元素自动一行排列*/
    display: flex;
    /*text-align: center; 失效*/
    justify-content:center;
  }

  .textarea {
    min-height: 100px;
    border: 1px solid #a0b3d6; 
    width: 300px;
    font-size: 14px;
    max-height: 300px;
    overflow-y: auto;
 
    /*不加不能居中*/
    margin: 0 auto;   
  }
</style>
