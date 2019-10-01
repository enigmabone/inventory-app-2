<template>
  <b-col md="4" class="m-4">
    <b-card header="Add Inventory Item">
      <b-card-body>
        <b-form autocomplete="off">
          <b-form-group label="Item Name">
            <b-form-input v-model="form.name" id="name" name="name" trim></b-form-input>
          </b-form-group>
          <b-form-group label="Item Price ($)">
            <b-form-input v-model="form.price" id="price" name="price" trim></b-form-input>
          </b-form-group>
          <b-form-group label="Item Brand">
            <b-form-input v-model="form.brand" id="brand" name="brand" trim></b-form-input>
          </b-form-group>
          <b-form-group label="Inventory Status">
            <b-form-radio
              v-model="form.inventoryStatus"
              name="inventoryStatus"
              value="true"
            >In Stock</b-form-radio>
            <b-form-radio
              v-model="form.inventoryStatus"
              name="inventoryStatus"
              value="false"
            >Out of Stock</b-form-radio>
          </b-form-group>
          <b-button block variant="success" @click="addProduct">Add Item</b-button>
        </b-form>
      </b-card-body>
    </b-card>
  </b-col>
</template>
<script>
export default {
  name: "AddItem",
  data() {
    return {
      form: {
        name: "",
        price: "",
        brand: "",
        inventoryStatus: ""
      }
    };
  },
  methods: {
    addProduct() {
      console.log(this.form);
      //this.$emit("")
    }
  }
};
</script>
<style scoped lang="scss">
.card-header {
  font-weight: bold;
}
.card {
  box-shadow: 0px 0px 5px #cacaca;
}
</style>