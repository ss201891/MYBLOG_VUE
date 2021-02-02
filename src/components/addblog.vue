<template>
    <div>
        <h2 class="title_write">写博客</h2>
        <form class="form_writeblog" v-if="!submitted">
            <label for="">博客标题 ：</label>
            <input type="text" v-model="blog.title" required />
<br>
            <label for="">博客内容 ：</label>
            <textarea name="" v-model="blog.content"></textarea>     
            <!-- // TODO标签可添加的 -->
            <div id="checkboxes">
                <label for="">Vue.js</label>
                <input type="checkbox" value="Vue.js" v-model="blog.categories">
                 <label for="">node.js</label>
                <input type="checkbox" value="node.js" v-model="blog.categories">
                 <label for="">css</label>
                <input type="checkbox" value="css" v-model="blog.categories">
            </div>
            <label for="">作者：{{blog.author}}</label>
            <button @click.prevent="post">添加博客</button>
        </form>
        <div v-if="submitted">
            <h3>你的博客发布成功</h3>
        </div>
        <hr>
        <div id="preview">
            <h3>博客总览</h3>
            <p>博客标题：{{blog.title}} </p>
            <p>博客内容：</p>
            <p>{{blog.content}}</p>
            <p>博客分类：</p>
            <ul>
                <li v-for="(item,index) in blog.categories" :key="index">  {{item}}  </li>
            </ul>
        </div>
    </div>
</template>

<script>
import Vue from 'vue'
export default {
    
    // http://jsonplaceholder.typicode.com/
     name:'Addblog',
    data(){
       
        return{
            blog:{
                title:'',
                content:'', 
                categories:[],
                author:'SS'
            },
            submitted:false
        }
    },
    methods:{
        post(){
        Vue.axios.post('http://jsonplaceholder.typicode.com/posts',{
            title:this.blog.title,
            body:this.blog.content,
            userId:1
            }).then((response)=>{
               alert("添加成功")
               console.log(response)
               this.submitted = true;
            }).catch((error)=>{
                console.log(error);
            });
      }}
}
</script>

<style>
 *{
        list-style: none;
        margin: 0;
        padding: 0;
        text-decoration: none;
    }
    .title_write{
       
        margin: 20px auto;
    }
    .form_writeblog{

    }

</style>
