<template>
  <div id="app">
    <Navbar />
    <b-container>
      <b-row class="justify-content-center">
        <AddItem />
        <ListItem />
      </b-row>
    </b-container>
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import AddItem from "./components/AddItem.vue";
import ListItem from "./components/ListItem.vue";
import axios from "axios";

export default {
  name: "app",
  components: {
    Navbar,
    AddItem,
    ListItem
  },
  data() {
    return {
      productList: []
    };
  },
  methods: {
    async getProductList() {
      try {
        let result = await axios.get("http://localhost:3000/products");
        console.log("result", result.data);
        this.productList = result.data;
      } catch (error) {
        console.log("Error", error);
      }
    }
  },
  mounted() {
    this.getProductList();
  }
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
body {
  font-family: Helvetica, Arial, sans-serif;
}
</style>
