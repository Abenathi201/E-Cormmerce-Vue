<template>
    <router-link :to="{name: 'product', params:{id: product.id}}">
        <!-- <img :src="product.image" :alt="product.name">
        <div class="info">
            <h3>{{ product.name }}</h3>
            <p>Category: {{ product.category }}</p>
            <p>Price: {{ product.price }}</p>
        </div> -->

        <div class="card">
            <div>
              <img :src="product.image" :alt="product.title">
            </div>
            <div class="details">
            <div class="min-details">
            <h1>R{{ product.name }}<span>R{{ product.name }}</span></h1>
            <h1 class="price"> R{{ product.price }}</h1>
            </div>
        
            <div class="options">
            <div class="description">
            </div>
            </div>
            <button @click="addToCart(product.id)" class="cart-btn">Add to cart</button> 
            </div>
        </div>
    </router-link>
</template>

<script>
export default{
    props: ["product"]
}
</script>

<style scoped>
    .card {
    position: relative;
    border-radius: 5px;
    box-shadow: 0 5px 10px rgba(0,0,0,0.3);
    height: 500px;
    width: 400px;
    margin-inline: 20px;
    margin-block: 20px;
    overflow: hidden;
}

    img {
    width: 100%;
    height: 100%;
    margin: 20px auto 0 auto;
}
    .details {
    background-color: #FFF;
    border-radius: 10px;
    padding: 20px;
    position: absolute;
    top: 85%;
    width: 360px;
    transition: box-shadow .3s ease-in-out,top .3s ease-in-out;
}

    .card:hover .details {
    box-shadow: 0 -5px 10px rgba(0,0,0,0.3);
    top: 60%;
}

    .details, .min-details, .description{
    margin-bottom: 20px;
}

    .details .min-details {
    display: flex;
    justify-content: space-between;
}

    .min-details h1{
    font-size: 20px;
}

    span {
    color: #7B7B7B;
    display: block;
    font-size: 15px;
    /* font-weight: 400; */
}

    .cart-btn{
    background-color: black;
    border-radius: 5px;
    color: white;
    padding: 10px;
    text-align: center;
    text-decoration: none;
    text-transform: capitalize;
    width: 100%;
    transition: box-shadow .3s ease-in-out, transform .3s ease-in-out;
    cursor: pointer;
}

    .cart-btn:hover{
    box-shadow: 0 5px 10px rgba(0,0,0,.3);
    transform: translateY(-2px);
}
</style>