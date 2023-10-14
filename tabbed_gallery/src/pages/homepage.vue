<template>
    <div class="container">
        <div  style="text-align:center;">
    <h2>Tabbed Image Gallery</h2>
    <p>Click on the images below:</p>
</div>

<div>
    <div  style="width:25%;margin-top:10px;margin-right:20px;display:flex;">
        
    <img  v-for="(item, index) in galleryList" :src="item" style="width:100%" @click='expandimg(index)' :key="index">
    
    </div>
</div>
<div class="images">
    <img :src="img_url" style="width:100%;
    height:75vh;">
</div>


    </div>


</template>

<script>
export default{
data(){
    return{
        galleryList:[
        "public/assets/img_lights.jpg",
       "public/assets/img_mountains.jpg",
        "public/assets/img_nature.jpg",
        "public/assets/img_snow.jpg"

        ],

        img_url:"public/assets/img_lights.jpg",
        displayimg:true,
    }
},
methods:{
    expandimg(index){
        console.log("the vau=lue of indexs is",index)
        this.img_url=this.galleryList[index];
        //this.displayimg=!this.displayimg
    },
  
}

}
</script>

<style>


.container{
    align-content: center;
}
</style>