<template>
  <div id="header">
       <label class="header-title">SS的奇幻漂流之旅</label>
      <ul>
         
          <li>首页</li>
          <li>管理日志</li>
          
      </ul>
  </div>
</template>

<script>
export default {
  name:'Header'
}
</script>

<style>
    *{
        list-style: none;
        margin: 0;
        padding: 0;
        text-decoration: none;
    }
    #header{
        display: flex;
        position: relative;
        top: 0;
        right: 0;
        bottom: 0;
        background-color:#2c3e50;
    }
    ul{
        display:flex;
        margin: 0 auto;
        width: 60%;
        height: 60px;
        line-height: 60px;
        background-color: rgba(0,0,0,0.3);

    }
    label{
        display:flex;
         color: white;
         height: 60px;
        line-height: 60px;
        margin:0 30px;
    }
    li{
        width: 40%;
        color: white;
        text-align: center;
    }
</style>
