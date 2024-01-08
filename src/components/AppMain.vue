<script>
export default {
    name: 'AppMain',
    data() {
        return {
            content: [
                {
                    name: 'DIGITAL COMICS',
                    img: '../assets/img/buy-comics-digital-comics.png'
                },
                // Puoi aggiungere ulteriori oggetti all'array 'content' se necessario
            ]
        };
    },
}
</script>
<template lang="">
    <main>
        <div class="contenuto">
        <div class="content"> --> Content goes here <-- </div>
    </div>
        <div class="christian">
        <div class="pellino"    v-for="(object, index ) in content" :key="index">
        <ul>
            <li><img :src=object.img alt="">{{object.name}}</li>
        </ul> 
    </div>
</div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use  '../styles/generals.scss' as *;
    main{
         .contenuto{
            background-color: black;
            .content{
             max-width: 991px;
             margin: 0 auto;
             color: $white;
             padding: 40px 0px;
             font-size: 25px
        }
         }
        .christian{
            background-color: $blue;
            .pellino{
            max-width: 991px;
            margin: 0 auto;
            padding: 40px 0px;
            color: $white
        }
        }
        
    }

</style>