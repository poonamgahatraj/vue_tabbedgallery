<template>
    <div class="container">
        <div  style="text-align:center;">
    <h2>Tabbed Image Gallery</h2>
    <p>Click on the images below:</p>
</div>

<div>
    <div  style="width:25%;margin-top:10px;margin-right:20px;display:flex;">
    <img :src=galleryList[0] style="width:100%" @click="expandimg">
    <img :src=galleryList[1] style="width:100%" @click="expandimg1">
    <img :src=galleryList[2] style="width:100%" @click="expandimg2">
    <img :src=galleryList[3] style="width:100%" @click="expandimg3">
    </div>
</div>
<div class="images"  v-if="displayimg">
    <img :src="galleryList[0]" style="width:100%;
    height:75vh;">
</div>

<div class="images1"  v-if="displayimg1">
    <img :src="galleryList[1]" style="width:100%;
    height:75vh;">
</div>

<div class="images2"  v-if="displayimg2">
    <img :src="galleryList[2]" style="width:100%;
    height:75vh;">
</div>

<div class="images3"  v-if="displayimg3">
    <img :src="galleryList[3]" style="width:100%;
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
        displayimg:false,
        displayimg1:false,
        displayimg2:false,
        displayimg3:false,
        
       
    }
},
methods:{
    expandimg(){
        this.displayimg=!this.displayimg
    },
    expandimg1(){
        this.displayimg1=!this.displayimg1
    },

    expandimg2(){
        this.displayimg2=!this.displayimg2
    },

    expandimg3(){
        this.displayimg3=!this.displayimg3
    },

}

}
</script>

<style>


.container{
    align-content: center;
}
</style>