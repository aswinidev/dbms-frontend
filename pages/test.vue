<template>
  <div>
    <NavBar />
    <div class="row justify-content-between" style="text-align:center; margin-top: 40px">
      <div class="col-4">
        <h1>Customer Queries</h1>
      </div>
    </div>
    <div class="card" style="margin: 100px 300px 50px; width: ;">
      <div class="card-body">
        <h5 class="card-title" style="font-size: 30px; font-weight: 600;">
          Name | Email
        </h5>
        <p class="card-text" style="font-size: 24px;">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. At ex esse, doloribus iusto est similique ea mollitia dicta magnam cum nulla, sapiente adipisci quibusdam tempore in nostrum aut vel. Cupiditate.
        </p>
        <a
          href="#"
          class="btn btn-primary"
          style="font-size: 20px;"
        >Reply</a>
      </div>
    </div>
    <Footer />
  </div>
</template>

<style scoped>
.card:hover{
  transition: all 0.3s ease-in-out;
scale: 1.1;
}
.card-text{
  display: block;
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;

}
</style>
