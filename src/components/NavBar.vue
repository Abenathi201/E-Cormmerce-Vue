<template>
    <!-- <nav class="topNav">
        <routerlink class="active" to="/">Home</routerlink>
        <routerlink to="/tutorials">Tutorial</routerlink>
        <routerlink to="/about">About</routerlink>
        <routerlink to="/Form">Form</routerlink>
    </nav> -->

    <nav>
      <routerlink to="/" id="logo">My Logo</routerlink>
      <!-- <input type="checkbox" id="hamburger" />
      <label for="hamburger">
        <i class="fa-solid fa-bars"></i>
      </label> -->
      <ul>
        <li>
          <router-link to="/">Home</router-link>
        </li>
        <li>
            <router-link to="/about">About</router-link>
        </li>
        <li>
            <router-link to="/products">Products</router-link>
        </li>
        <li>
            <router-link to="/form">Contact Us</router-link>
        </li>
      </ul>
    </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
nav {
  font-family: "Poppins", sans-serif;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #d9d9d9;
  padding: 20px;
}
nav a {
  text-decoration: none;
  text-transform: capitalize;
  color: #ffffff;
}
#logo {
  font-size: 1.2em;
  font-weight: 600;
}
/* input[type="checkbox"] {
  appearance: none;
}
label {
  display: none;
  cursor: pointer;
} */
ul {
  list-style: none;
  display: flex;
  gap: 1em;
}
ul a {
  padding: 0.5em;
}
ul a:hover {
  background-color: #333333;
  border-radius: 0.5em;
}
.active {
  border-bottom: 2px solid #ffffff;
}

</style>