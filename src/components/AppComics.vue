<script>
export default {
    name: 'AppComics',
    props: {
        item: Array
    },
    data() {
        return {
            
        }
    },
}
</script>
<template lang="">
   
            <div class="col-2" :key="index">
            <img class="comics" :src="item.thumb" alt=""> <div class="name">{{item.series}}</div> 
        </div>  
     
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use  '../styles/generals.scss' as *;
    @use '../styles/partials/mixin' as*;
 
             img{
                width: 150px;
                height: 180px

             }
             .name{
                font-size: 13px;
                margin-bottom: 40px;
             }
        

</style>