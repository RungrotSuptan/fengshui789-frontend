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

        <p class="description">
          ร้านขายของแต่งร้าน แต่งโต๊ะทำงาน แต่งออฟฟิต แต่งบ้าน แต่งคอนโด ของขวัญแต่งบ้าน ของขวัญมงคล ดีไซน์สมัยใหม่ที่เป็นมงคล
        </p>

        <div class="product-name">
            <h4 class="title is-4">เรือสำเภา ขนาดใหญ่</h4>
            <p class="subtitle is-6">
                สัดส่วนเป็นมงคล<br>
                ยาว 55 สูง 60 เซนติเมตร
            </p>
        </div>

        <b-carousel :indicator-inside="false" :autoplay="false" :repeat="true" :items-to-show="2">
            <b-carousel-item v-for="(item, i) in productsXL" :key="`tallship-xl-${i}`">
                <figure class="image is-square">
                    <img :src="require(`~/assets/images/products/xl-tallship/${item.imageName}.jpeg`)">
                </figure>
            </b-carousel-item>
            <template slot="indicators" slot-scope="props">
                <figure class="image">
                    <img class="indicatorsImage" :src="require(`~/assets/images/products/xl-tallship/${productsXL[props.i].imageName}.jpeg`)" :title="`tallship-xl-item-${productsXL[props.i].imageName}`">
                </figure>
            </template>
        </b-carousel>

        <div><br><br></div>

        <b-carousel :indicator-inside="false" :autoplay="false" :repeat="true">
          <b-carousel-item>
            <figure class="image">
                <img :src="require(`~/assets/images/dimension/xl-width.jpg`)">
            </figure>
          </b-carousel-item>
          <b-carousel-item>
            <figure class="image">
                <img :src="require(`~/assets/images/dimension/xl-height.jpg`)">
            </figure>
          </b-carousel-item>
          <template slot="indicators" slot-scope="props">
              <figure class="image">
                  <img class="indicatorsImageM" :src="require(`~/assets/images/dimension/xl-height.jpg`)" :title="`tallship-m-item-${productsM[props.i].imageName}`">
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
        <b-carousel :indicator-inside="false" :autoplay="false" :repeat="true" :gallery="false">
            <b-carousel-item v-for="(item, i) in productsM" :key="`tallship-m-${i}`">
                <figure class="image is-square">
                    <img :src="require(`~/assets/images/products/m-tallship/${item.imageName}.jpg`)">
                </figure>
            </b-carousel-item>
            <template slot="indicators" slot-scope="props">
                <figure class="image">
                    <img class="indicatorsImageM" :src="require(`~/assets/images/products/m-tallship/${productsM[props.i].imageName}.jpg`)" :title="`tallship-m-item-${productsM[props.i].imageName}`">
                </figure>
            </template>
        </b-carousel>

        <div><br><br></div>

        <b-carousel>
          <b-carousel-item>
            <figure class="image">
                <img :src="require(`~/assets/images/dimension/m-width.jpg`)">
            </figure>
          </b-carousel-item>
          <b-carousel-item>
            <figure class="image">
                <img :src="require(`~/assets/images/dimension/m-height.jpg`)">
            </figure>
          </b-carousel-item>
        </b-carousel>

        <div><br><br></div>

        <h5 class="title is-5">
          🏆 การตกแต่ง บ้านด้วยเรือสำเภาหรือเรือใบ
        </h5>
        <p>
          การตกแต่งด้วย เรือสำเภา เรือใบนั้น เพื่อความเจริญก้าวหน้าในชีวิตให้รวดเร็ว <br>
          ✅ เสริมการงานตำแหน่งงาน <br>
          ✅ ทำให้เกิดโชคลาภ <br>
          ✅ ด้านการค้าขาย ค้าขายราบรื่น ได้กำไรงดงาม <br>
          ✅ เสริมดวงชะตาหนุนความสำเร็จมั่นคง <br>
        </p>

        <div><br><br></div>

        <h5 class="title is-5">
          🏺 ตำแหน่ง ตกแต่งแล้วเป็นมงคล
        </h5>
        <p>
          ✅ [ ประตูทางเข้าหลักของบ้าน ] เข้าบ้านพบเรือสำเภา เสริมการมีวิสัยทัศน์ไกล มองข้ามเกม ทำอะไรจะไม่เสียผลประโยชน์ <br>
          ✅ [ ห้องนั้งเล่น ] ทำให้ครอบครัวมีความสุข สานสัมพันธ์คนในบ้าน ชอบเดินทางท่องเที่ยวด้วยกัน <br>
          ✅ [ ห้องทำงาน ] เสริมความคิดให้วางแผนเก่ง สำเร็จเรื่องการงานและการติดต่อ จึงได้รับแต่ผลประโยชน์  <br>
          ✅ [ ตู้โชว์ ] เสริมให้ลูกหลาน อ่อนน้อมถ่อมตน ระบบการคิดเป็นนักวางแผน เข้าหาผู้ใหญ่ เป็นคนมีมารยาท <br>
          ✅ [ ห้องอาหาร ] ช่วยเพิ่มพูนทรัพย์สินเงินทอง มีชื่อเสียง ฐานะมั้นคง <br>
          ✅ [ ห้องรับแขก ] ลูกค้า เพื่องฝูง ต่างไว้ใจ เป็นที่ยอมรับ ไร้อุปสรรคจากคนที่ค่อยขัดขวางความก้าวหน้า <br>
        </p>

        <div><br><br></div>

        <h5 class="title is-5">
          👍 ข้อสังเกตและเทคนิค
        </h5>
        <p>
          ✅ หันหัวเรือเข้าบ้าน <br>
          ✅ ตกแต่งในห้องทำงาน ไม่หันหัวเรือเข้าหาตัวเองหรือถ้าในที่ทำงานห้ามหันประจันกับลูกน้อง จะมีการกระทบกระทั่งกันได้ <br>
          ✅ สัดส่วนเรือต้องเป็นมิติมงคลหรือตามขนาดมงคล ตามตลับเมตรฮวงจุ้ย <br>
          ✅ ใส่เงินเข้าไปในเรือเพื่อเพื่อเสริมทรัพย์สินเงินทอง <br>
        </p>
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
          ],
          productsM: [
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
            },
            {
                name: 'ชมสินค้า',
                imageName: '005'
            },
            {
                name: 'ชมสินค้า',
                imageName: '006'
            },
            {
                name: 'ชมสินค้า',
                imageName: '007'
            },
            {
                name: 'ชมสินค้า',
                imageName: '008'
            },
            {
                name: 'ชมสินค้า',
                imageName: '009'
            },
            {
                name: 'ชมสินค้า',
                imageName: '010'
            },
            {
                name: 'ชมสินค้า',
                imageName: '011'
            }
          ],
          XLdimension: [
            {
              w: "xl-width",
              h: "xl-height",
            }
          ],
          Mdimension: [
            {
              w: "m-height",
              h: "m-height",
            }
          ]
      }
    },
    methods: {
    }
}
</script>

<style>
html {
  font-family: sans-serif;
  line-height: 1.15;
  -webkit-text-size-adjust: 100%;
  -webkit-tap-highlight-color: rgba(0,0,0,0);
}
body {
    position: relative;
    margin: 0 auto;
}
body {
    font-family: "Sarabun",sans-serif;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #212529;
    text-align: left;
    background-color: #fff;
}
.description {
  text-align: center;
}
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
.indicatorsImageM {
  height: 26px !important;
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
.view-product {
  color: #ffffff;
  background-color: #ee4d2d;
}

</style>
