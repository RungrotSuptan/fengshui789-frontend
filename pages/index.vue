<template>
    <div>
        <figure class="image is-128x128 logo">
            <img src="~/assets/images/logo-fengshui-789.png" alt="ร้าน FengShui789">
        </figure>
        <div class="shopname">
            <h1 class="title is-3">
                ร้าน FengShui789
            </h1>
        </div>

        <div class="product-name">
            <h4 class="title is-4">เรือสำเภา ขนาดใหญ่</h4>
            <p class="subtitle is-6">
                สัดส่วนเป็นมงคล<br>
                ยาว 55 สูง 60 เซนติเมตร
            </p>
        </div>
        <b-carousel :indicator-inside="false">
            <b-carousel-item v-for="(item, i) in productsXL" :item="item" :key="item.imageName" :img-src="item.imageName">
                <figure class="image is-square">
                    <img :src="require(`~/assets/images/products/xl-tallship/${item.imageName}.jpeg`)">
                </figure>
            </b-carousel-item>
            <template slot="indicators" slot-scope="props">
                <figure class="al image">
                    <img class="indicatorsImage" :src="require(`~/assets/images/products/xl-tallship/001.jpeg`)" :title="props.imageName" @click="aa(props)">
                </figure>
            </template>
        </b-carousel>
        
        <div><br><br></div>

        <div class="product-name">
            <h4 class="title is-4">เรือสำเภา ขนาดใหญ่</h4>
            <p class="subtitle is-6">
                สัดส่วนเป็นมงคล<br>
                ยาว 24 สูง 22 เซนติเมตร
            </p>
        </div>
        <b-carousel :indicator-inside="false">
            <b-carousel-item v-for="(item, i) in 6" :key="i+10">
                <figure class="image is-square">
                    <img :src="getImgUrl(i)">
                </figure>
            </b-carousel-item>
            <template slot="indicators" slot-scope="props">
                <figure class="al image">
                    <img class="indicatorsImage" :src="getImgUrl(props.i)" :title="props.i">
                </figure>
            </template>
        </b-carousel>
    </div>
</template>

<script>
export default {
      data () {
        return {
            productsXL: [
                {
                    name: 'ชมสินค้า',
                    imageName: '001'
                },
                {
                    name: 'ชมสินค้า',
                    imageName: '002'
                },
                {
                    name: 'ชมสินค้า',
                    imageName: '003'
                },
                {
                    name: 'ชมสินค้า',
                    imageName: '004'
                }
            ]
        }
    },                
    methods: {
      getImgUrl(value) {
          return `https://picsum.photos/id/43${value}/1230/500`
      },
      aa(a) {
          console.log(a)
      }
    }
}
</script>

<style>
.shopname {
    text-align: center;
    margin: 25px;
}
.logo {
    margin: 0 auto;
}
.indicatorsImage {
    height: 50px !important;
    width: 50px !important;
    border-radius: 5px;
}
.carousel-indicator > a{
    border: #f79f0f 2px solid;
    border-radius: 7px;
}
.carousel-indicator > a.is-active{
    border: #e82b2b 2px solid;
}
.menu-list a.is-active {
    background-color: #e82b2b;
}
.is-active .al img {
    filter: grayscale(0%);
}
.al img {
    filter: grayscale(100%);
}
.product-name {
    text-align: center;
    margin-bottom: 15px;
}

</style>