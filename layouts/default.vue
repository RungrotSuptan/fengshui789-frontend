<template>
  <div class="main">
    <section>
      <aside class="column is-12 section">
        <p class="menu-label is-hidden-touch">

        </p>
        <ul class="menu-list">
          <li
            v-for="(item, key) of items"
            :key="key"
          >
            <nuxt-link
              :to="item.to"
              exact-active-class="is-active"
            >
              <b-icon :icon="item.icon" /> {{ item.title }}
            </nuxt-link>
          </li>
        </ul>
      </aside>
      <div class="container column is-10">
        <nuxt />
      </div>
    </section>
    <footer class="footer">
      <div class="content has-text-centered">
        <p>
          © 2020 FengShui789. All Rights Reserved
        </p>
      </div>
    </footer>
    <div class="product-bottom-panel-wrapper">
      <div class="product-bottom-panel">
        <div class="product-cart-and-buy-buttons">
          <div class="product-bottom-panel__buy-now">
            <div class="buttons">
              <a class="button is-fullwidth view-product" href="https://shopee.co.th/product/293435528/6052428063/" target="_blank">
                <b-icon icon="cart" />&nbsp; รายละเอียดสินค้าที่ Shopee
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          title: 'สินค้าของเรา',
          icon: 'home',
          to: { name: 'index' }
        },
        {
          title: 'ซื้อได้ที่...',
          icon: 'cart',
          to: { name: 'shop' }
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>
aside {
  text-align: center;
}
.main {
  position: relative;
  max-width: 767.98px;
  margin: 0 auto;
}
.product-bottom-panel-wrapper {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: white;
  -webkit-box-shadow: 0 -0.5rem 1rem rgba(0,0,0,0.075);
  box-shadow: 0 -0.5rem 1rem rgba(0,0,0,0.075);
  z-index: 1021;
}
</style>
