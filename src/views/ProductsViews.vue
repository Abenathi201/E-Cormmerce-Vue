<template>
    <div v-if="products" class="products-vue">
        <ProductCard v-for="product of products" :key="product.id" :product="product" />
    </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue';

export default{
    components: { ProductCard },

    computed: {
        products() {
            return this.$store.state.products
        }
    },

    mounted() {
        return this.$store.dispatch("getProducts")
    },
}
</script>