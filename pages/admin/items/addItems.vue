<template>
  <div>
    <div class="container" style="height:100vh">
      <form class="form-container">
        <div class="headline">
          <span>Add Item</span>
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey;">Item Name</label><br><br>
          <input
            v-model="itemName"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Number of Items</label><br><br>
          <input
            v-model="noOfItems"
            type="text"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Price</label><br><br>
          <input
            v-model="price"
            type="Email"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Contact Number</label><br><br>
          <input
            v-model="contactNo"
            type="Email"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>
        <div class="form-line">
          <label style="font-size: 18px; color: darkgrey">Supplier Name</label><br><br>
          <input
            v-model="SupplierName"
            type="form-input"
            class="form-input"
            autocomplete="off"
            style="cursor: auto;"
            required
          >
        </div>

        <input type="button" class="form-button" value="Submit" style="font-size: 18px;" @click="addItem">
      </form>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
const myaxios = axios.create({ baseURL: 'http://localhost:8080' })
export default {
  data () {
    return {
      itemName: '',
      noOfItems: 0,
      price: 0,
      contactNo: '',
      SupplierName: ''
    }
  },
  methods: {
    addItem () {
      myaxios
        .post('/admin/addItem', {
          itemName: this.itemName,
          noOfItems: this.noOfItems,
          price: this.price,
          contactNo: this.contactNo,
          supplierName: this.SupplierName
        },
        {
          headers: {
            Authorization: `Bearer ${localStorage.getItem('token')}`
          }
        }
        )
        .then(function (response) {
          console.log(response.data)
        }
        )
        .catch((error) => {
          this.errorMessage = error.message
          console.error('There was an error!', error)
        })
    }
  }
}
</script>

<style scoped>
  @import '@/assets/employee/addEmp.css'
</style>
