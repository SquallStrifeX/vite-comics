<script>
import AppComics from './AppComics.vue'

export default {
    name: 'AppMain',
    components: {
        AppComics
    },
    data() {
        return {
            content: [
                {
                    name: 'DIGITAL COMICS',
                    img: '../assets/img/buy-comics-digital-comics.png'
                },
                {
                    name: 'DC MERCHANDISE',
                    img: '../assets/img/buy-comics-merchandise.png'
                },
                {
                    name: 'SUBSCRIPTION',
                    img: '../assets/img/buy-comics-subscriptions.png'
                },
                {
                    name: 'COMICS SHOP LOCATOR',
                    img: '../assets/img/buy-comics-shop-locator.png'
                },
                {
                    name: 'DC POWER VISA',
                    img: '../assets/img/buy-dc-power-visa.svg'
                },
            ],
        comics:    [
  {
      "thumb": "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
      "price": "$19.99",
      "series": "Action Comics",
      "type": "comic book",
  },
  {
      "thumb": "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
      "price": "$3.99",
      "series": "American Vampire 1976",
      "type": "comic book",
  },
  {
      "thumb": "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
      "price": "$16.99",
      "series": "Aquaman",
      "type": "graphic novel",
  },
  {
      "thumb": "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
      "price": "$2.99",
      "series": "Batgirl",
      "type": "comic book",
  },
  {
      "thumb": "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
      "price": "$3.99",
      "series": "Batman",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
      "price": "$2.99",
      "series": "Batman Beyond",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
      "price": "$3.99",
      "series": "Batman/Superman",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
      "price": "$4.99",
      "series": "Batman/Superman Annual",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
      "price": "$5.99",
      "series": "Batman: The Joker War Zone",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
      "price": "$6.99",
      "series": "Batman: Three Jokers",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
      "price": "$4.99",
      "series": "Batman: White Knight Presents: Harley Quinn",
      "type": "comic book",
  },
  {
      "thumb": "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
      "price": "$16.99",
      "series": "Catwoman",
      "type": "graphic novel",
  },
]
}
    },
    methods: {
    getImagePath: function(img) {
      return new URL(`${img}`, import.meta.url).href;
    }
  }
}

</script>
<template lang="">
    <main><div class="contenuto"> 
           <div class="img"></div>
           <div class="containerx" > <button class="current p-1 px-3"> CURRENT SERIES</button> </div>
        <div class="content row">
         <AppComics v-for="item, index in comics" :item="item"></AppComics>
         <button class="load_more"> LOAD MORE </button>
    </div>
   </div>
        <div class="christian">
        <div class="pellino"    >
        <ul >
            <li v-for="(object, index ) in content" :key="index"><img :src="getImagePath(object.img)" alt=""><span>{{object.name}}</span></li>
        </ul>  
       
    </div>
   
</div>
    </main>
</template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use  '../styles/generals.scss' as *;
    @use '../styles/partials/mixin' as*;

    main{
         .contenuto{
            background-color: black;
            .img{
                background-image: url(../assets/img/jumbotron.jpg);
                height: 320px;
                background-size: cover;
                background-repeat: no-repeat;
                
            }
            .containerx{
                  @include max-width;
                  .current{
                background-color: $blue;
                color: $white;
                margin: -85px auto;
            }
            }

            
            .content{
            @include max-width;
             color: $white;
             padding: 40px 0px;
             font-size: 25px;
             img{
                width: 150px;
                height: 180px

             }
             .name{
                font-size: 13px;
                margin-bottom: 40px;
             }
        }

        .load_more{
            @include max-width;
            background-color: $blue;
           color: $white;
           width: 150px;
           font-size: 12px;
           padding: 8px;
        }
         }
        .christian{
            background-color: $blue;
            .pellino{
             @include max-width;
            padding: 40px 0px;
            color: $white;
            ul{
                display: flex;
                flex-direction: row;
                li{
                    list-style: none;
                    font-size: 15px;
                    padding: 20px;
                    img{
                        width: 22px;
                    }
                    span{
                        padding-left: 10px;
                    }

                }
            }
        }
        }
        
    }

</style>