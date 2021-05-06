<template>
  <div class="container-fluid">
    <h1>ProductInfo</h1>
    <ProductInfoTabs />
    <ProductInfoRelatedSlider />
  </div>
</template>

<script>
import ProductInfoTabs from "./ProductInfoTabs.vue";
import ProductInfoRelatedSlider from "./ProductInfoRelatedSlider.vue";

export default {
  name: "ProductInfo",
  components: { ProductInfoTabs, ProductInfoRelatedSlider },
};
</script>
