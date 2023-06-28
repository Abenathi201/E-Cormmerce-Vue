<template>
    <div v-if="product" class="product-detail">
        <img :src="product.image" :alt="product.name">

        <div>
            <h2> {{ product.name }} </h2>
            <p> {{ product.category }} </p>
            <p> {{ product.price }} </p>
        </div>
    </div>
</template>

<script>
export default{
    props: ["id"],

    product() {
        return this.$store.state.product
    },

    mounted() {
        return this.$store.dispatch("getProduct", this.id)
    },
}
</script>