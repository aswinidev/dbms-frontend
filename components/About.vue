<template>
  <div>
    <!-- <NavBar /> -->
    <section id="about">
      <div class="container">
        <header class="section-header aos-init">
          <h3>About Us</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
            labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
            laboris nisi ut aliquip ex ea commodo consequat.
          </p>
        </header>
        <div class="row about-cols">
          <div class="col-md-4">
            <div class="about-col">
              <div class="img">
                <img
                  src="https://res.cloudinary.com/munnapatel003/image/upload/v1631986010/demo3.jpg"
                  alt=""
                  class="img-fluid"
                >
                <div class="icon">
                  <i class="fas fa-tachometer-alt" />
                </div>
              </div>
              <h2 class="title">
                Our Mission
              </h2>
              <p>
                Lorem ipsum dolor sit amet, consectetur elit, sed do eiusmod tempor ut labore et dolore
                magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
                aliquip ex ea commodo consequat.
              </p>
            </div>
          </div>
          <div class="col-md-4">
            <div class="about-col">
              <div class="img">
                <img
                  src="https://res.cloudinary.com/munnapatel003/image/upload/v1631986010/demo2.jpg"
                  alt=""
                  class="img-fluid"
                >
                <div class="icon">
                  <i class="far fa-list-alt" />
                </div>
              </div>
              <h2 class="title">
                Our Plan
              </h2>
              <p>
                Sed ut perspiciatis unde omnis iste natus error sit voluptatem doloremque laudantium,
                totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto
                beatae vitae dicta sunt explicabo.
              </p>
            </div>
          </div>
          <div class="col-md-4">
            <div class="about-col">
              <div class="img">
                <img
                  src="https://res.cloudinary.com/munnapatel003/image/upload/v1631986010/demo1.jpg"
                  alt=""
                  class="img-fluid"
                >
                <div class="icon">
                  <i class="far fa-eye" />
                </div>
              </div>
              <h2 class="title">
                Our Vision
              </h2>
              <p>
                Nemo enim ipsam voluptatem quia voluptas sit aut odit aut fugit, sed quia magni dolores
                eos qui ratione voluptatem sequi nesciunt Neque porro quisquam est, qui dolorem ipsum
                quia dolor sit amet.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- <Footer /> -->
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
* {
    font-family: "Poppins", sans-serif;
}

a:hover {
    text-decoration: none;
}

#about {
    background: url("https://cf.bstatic.com/images/hotel/840x460/201/201684636.jpg") center top no-repeat fixed;
    background-size: cover;
    padding: 29px 0 40px 0;
    position: relative;
}

.section-header h3 {
    font-size: 32px;
    color: #111;
    text-transform: uppercase;
    text-align: center;
    font-weight: 700;
    position: relative;
    padding-bottom: 15px;
}

.section-header h3::before {
    content: '';
    position: absolute;
    display: block;
    width: 120px;
    height: 1px;
    background: #ddd;
    bottom: 1px;
    left: calc(50% - 60px);
}

.section-header h3::after {
    content: '';
    position: absolute;
    display: block;
    width: 40px;
    height: 3px;
    background: #575a7b;
    bottom: 0;
    left: calc(50% - 20px);
}

.section-header p {
    text-align: center;
    padding-bottom: 30px;
    color: #333;
}

#about::before {
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    background: rgb(255 255 255 / 48%);
    z-index: 9;
}

#about .container {
    position: relative;
    z-index: 10;
}

#about .about-col {
    background: #fff;
    border-radius: 0 0 4px 4px;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.08);
    margin-bottom: 20px;
}

#about .about-col .img {
    position: relative;
}

#about .about-col .img img {
    border-radius: 4px 4px 0 0;
}

#about .about-col .icon {
    width: 64px;
    height: 64px;
    padding-top: 8px;
    text-align: center;
    position: absolute;
    background-color: #575a7b;
    border-radius: 50%;
    text-align: center;
    border: 4px solid #fff;
    left: calc(50% - 32px);
    bottom: -30px;
    transition: 0.3s;
}

#about .about-col i {
    font-size: 24px;
    line-height: 1.5;
    color: #fff;
    transition: 0.3s;
}

#about .about-col:hover .icon {
    background-color: #fff;
}

#about .about-col:hover i {
    color: #575a7b;
}

#about .about-col h2 {
    color: #000;
    text-align: center;
    font-weight: 700;
    font-size: 20px;
    padding: 0;
    margin: 40px 0 12px 0;
}

#about .about-col h2 a {
    color: #000;
}

#about .about-col p {
    font-size: 14px;
    line-height: 24px;
    color: #333;
    margin-bottom: 0;
    padding: 0 20px 20px 20px;
}

.btn-sm-default-web {
    background: #0c2b4b;
    display: inline-block;
    text-transform: uppercase;
    padding: 5px 30px;
    color: #ffffff;
    letter-spacing: 1px;
}
</style>
