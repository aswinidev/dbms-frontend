<template>
  <div>
    <table class="table1">
      <caption> HOTEL BILL</caption>
      <tr>
        <th colspan="3">
          Invoice #{{ genBill.billID }}
        </th>
        <th>{{ genBill.bDate }}</th>
      </tr>
      <tr id="whiteBG">
        <td colspan="2">
          <h3>Pay To:</h3>
          Le Lotus Grand Hotel<br>
          Varanasi,<br>
          Uttar Pradesh, India- 221001
        </td>
        <td colspan="2">
          <h3>Customer:</h3>
          {{ genBill.fname + genBill.lname }}<br>
        </td>
      </tr>
      <tr>
        <th>
          Name-Description
        </th>
        <th>
          Qty.
        </th>
        <th>
          MRP
        </th>
        <th>
          Amount
        </th>
      </tr>
      <tr id="whiteBG">
        <td>
          Single Rooms
        </td>
        <td>
          {{ genBill.singleRoom }}
        </td>
        <td>
          {{ genBill.singlePrice }}
        </td>
        <td>
          {{ genBill.singlePrice * genBill.singleRoom }}
        </td>
      </tr>
      <tr id="whiteBG">
        <td>
          Double Rooms
        </td>
        <td>
          {{ genBill.doubleRoom }}
        </td>
        <td>
          {{ genBill.doublePrice }}
        </td>
        <td>
          {{ genBill.doubleRoom * genBill.doublePrice }}
        </td>
      </tr>
      <tr>
        <td colspan="3">
          GRANDTOTAL
        </td>
        <td id="whiteBG">
          Rs + {{ genBill.amount }}
        </td>
      </tr>
    </table>
    <center>
      <button class="custom-btn btn-1" @click="Pay">
        <span>{{ "Pay " + genBill.amount }}</span>
      </button>
    </center>
  </div>
</template>

<script>
export default {
  data () {
    return {
      genBill: {}
    }
  },
  mounted () {
    this.genBill = this.$route.params.genBill
    console.log(this.genBill)
  }
}
</script>

<style scoped>
@import '@/assets/bill/bill.css'
</style>
