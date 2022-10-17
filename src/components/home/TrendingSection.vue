<template>
  <section class="trending-product section">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="section-title">
            <h2>Trending Product</h2>
            <p>There are many variations of passages of Lorem Ipsum available, but the majority have
              suffered alteration in some form.</p>
          </div>
        </div>
      </div>
      <div class="row">
        <div class="col-lg-3 col-md-6 col-12" v-for="(product,key) in products" :key="key">

          <div class="single-product">
            <div class="product-image">
              <img :src="product.image" alt="#" class="img-height">
              <div class="button">
                <a href="product-details.html" class="btn"><i class="lni lni-cart"></i> Add to Cart</a>
              </div>
            </div>
            <div class="product-info">
              <span class="category">Watches</span>
              <h4 class="title">
                <router-link :to="{name: 'detail', params:{id: product.id}}">
                  {{product.name}}
                </router-link>
              </h4>
              <ul class="review">
                <li><i class="lni lni-star-filled"></i></li>
                <li><i class="lni lni-star-filled"></i></li>
                <li><i class="lni lni-star-filled"></i></li>
                <li><i class="lni lni-star-filled"></i></li>
                <li><i class="lni lni-star"></i></li>
                <li><span>4.0 Review(s)</span></li>
              </ul>
              <div class="price">
                <span>Tk.{{product.selling_price}}</span>
              </div>
            </div>
          </div>

        </div>

      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios'
export default {
  name: "TrendingSection",
  data(){
    return {
      products : [],
    }

  },
  created() {
    this.getLatestProduct();
  },
  methods: {
    getLatestProduct(){
      axios.get('http://localhost/ecom2(front)-app/public/api/latest-product').then((response) => {
        this.products = response.data;

      });

    }

  }
}
</script>

<style scoped>
.img-height{
  height: 250px;
}


</style>