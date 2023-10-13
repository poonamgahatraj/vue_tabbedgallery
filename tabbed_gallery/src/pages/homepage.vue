<template>
    <div class="container">
        <div  style="text-align:center;">
    <h2>Tabbed Image Gallery</h2>
    <p>Click on the images below:</p>
</div>

<div>
    <div  style="width:25%;margin-top:10px;margin-right:20px;display:flex;">
    <img :src=galleryList[0] style="width:100%" @click="expandimg">
    <img :src=galleryList[1] style="width:100%">
    <img :src=galleryList[2] style="width:100%">
    <img :src=galleryList[3] style="width:100%">
    </div>
</div>
<div class="images"  v-if="displayimg">
    <img :src="galleryList[0]" style="width:100%;
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
        displayimg:false
       
    }
},
methods:{
    expandimg(){
        this.displayimg=!this.displayimg
    }
}

}
</script>

<style>


.container{
    align-content: center;
}
</style>