<script>
export default {
    data() {
        return {
            dc_comics: [
                {
                    nome: 'Characters'
                },
                {
                    nome: 'Comics'
                },
                {
                    nome: 'Movies'
                },
                {
                    nome: 'TV'
                },
                {
                    nome: 'Games'
                },
                {
                    nome: 'Videos'
                },
                {
                    nome: 'News'
                }
            ],
            shop: [
                {
                    nome: 'Shop DC'
                },
                {
                    nome: 'Shop DC Collectibles'
                }
            ],
            dc: [
                {
                    nome: 'Terms Of Use'
                },
                {
                    nome: 'Privacy Policy (New)'
                },
                {
                    nome: 'Ad Choises'
                },
                {
                    nome: 'Advertising'
                },
                {
                    nome: 'Jobs'
                },
                {
                    nome: 'Subscription'
                },
                {
                    nome: 'Talent Workshops'
                },
                {
                    nome: 'CPSC Certificates'
                },
                {
                    nome: 'Ratings'
                },
                {
                    nome: 'Shop Help'
                },
                {
                    nome: 'Contact Us'
                },
            ],
         sites: [
                {
                    nome: 'DC'
                },
                {
                    nome: 'MAD Magazine'
                },
                {
                    nome: 'DC Kids'
                },
                {
                    nome: 'DC Universe'
                },
                {
                    nome: 'DC Power Visa'
                },
            ]
        };
    },
}
</script>
<template>
    <footer>
      <div class="all">
        <div class="row">
          <div class="col-2">
            <h6 class="py-3 pt-5"> DC COMICS </h6>
            <ul v-for="(object, index) in dc_comics" :key="index">
              <li>
                {{ object.nome }}
              </li>
            </ul>
           
            <h6 class="py-3"> SHOP </h6>
            <ul  v-for="(object, index) in shop" :key="index">
              <li>
                {{ object.nome }}
              </li>
            </ul>
            <div class="mb-5"></div>
          </div>
        <div class="col-2">
          <h6 class="py-3 pt-5">DC</h6>
          <ul v-for="(object, index) in dc" :key="index">
              <li>
                {{ object.nome }}
              </li>
            </ul>
        </div>

            <div class="col-2">
                <h6 class="py-3 pt-5">SITES</h6>
          <ul v-for="(object, index) in sites" :key="index">
              <li>
                {{ object.nome }}
              </li>
            </ul>
        </div>
        <div class="col-6 back-img">
        </div>
      </div>
    </div>
    </footer>
  </template>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use  '../styles/generals.scss' as *;
    footer{
        background-image: url(../assets/img/footer-bg.jpg);
        .all{
        max-width: 991px;
        margin: 0 auto;
        color: $white;
    }
        
        ul{
            list-style: none;
         li{
                color: $grey;
                font-size: 12px;
            }
            
        }
        .back-img{
            background-image: url(../assets/img/dc-logo-bg.png);
            background-size: cover;
            background-position: center center

        }
    }


</style>