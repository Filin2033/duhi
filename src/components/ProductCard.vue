<template>
  <div class="card d-flex-column">
    <div class="img d-flex j-c">
      <img :src="`src/assets/${imageUrl}`" :alt="productName">
    </div>
    
    <div class="info">

      <div class="info-name d-flex-column align-flex-start">
        <span class="category">{{ productCategory }}</span>
        <span class="name">{{ productName }}</span>
      </div>
      <div class="pay d-flex-row j-sb">
        <div class="info-price d-flex align-flex-end ">
          <span class="new-price">{{ newPrice }}</span>
          <span class="old-price" v-if="oldPrice">{{ oldPrice }}</span>
        </div>

        <div class="btn-pay">
          <button class="add-to-cart d-flex align-center j-c">
            +
          </button>
        </div>
      </div>
      

    </div>
  </div>
</template>

<script>
import '../global.css';

export default {
  props: {
    imageUrl: {
      type: String,
      required: true
    },
    productCategory: {
      type: String,
      required: true
    },
    productName: {
      type: String,
      default: '' 
    },
    oldPrice: {
      type: [String, Number],
      default: null
    },
    newPrice: {
      type: [String, Number],
      required: true
    }
  }
};
</script>

<style scoped>
.card {
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
}

img {
  width: 300px;
  height: 250px;
  top: 200px;
  left: 76px;
  background-color: #999;
}
.product-price {
  margin-bottom: 1rem;
}
.old-price {
  text-decoration: line-through;
  color: #999;
  width: 47px;
  height: 15px;
  top: 446px;
  left: 151px;
  gap: 0px;
  opacity: 0px;
  font-family: Anselm Sans;
  font-size: 12px;
  font-weight: 400;
  line-height: 15.43px;
  text-align: center;


}
.new-price {
  font-family: Anselm Sans;
  font-size: 12px;
  font-weight: 400;
  line-height: 15.43px;
  text-align: center;
  width: 47px;
  height: 15px;
  top: 446px;
  left: 93px;
  gap: 0px;
  opacity: 0px;
}
.info-name {
  gap: 4px;
}
.category {
  color: #999;
  font-family: Anselm Sans;
  font-size: 11px;
  font-weight: 400;
  line-height: 14.15px;
  text-align: center;
}
.name {
  font-family: Anselm Sans;
  font-size: 14px;
  font-weight: 400;
  line-height: 18px;
  text-align: center;
}
.info {
  padding: 1rem;
}

.info-price{
  gap: 10px;
}
</style>