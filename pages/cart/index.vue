<template>
    <div>
      <nav>
        <div class="navBox-1">
          <div>
            <img
              id="Dark-logo"
              src="https://images.moneycontrol.com/static-mcnews/2023/06/Meesho-682x435.jpg?impolicy=website&width=1600&height=900"
              alt="Dark-logo"
            />
          </div>
          <div class="I-2-box">
          <i class="ri-search-line"></i>
          <input placeholder="Try these accessories" />
        
        </div>
          <div class="cart-box">
            <div>
              <span>Download App</span>
            </div>
            <div>
              <span>Become a Supplier</span>
            </div>
            <div>
              <span>Newsroom</span>
            </div>
            <div>
              <span>Profile</span>
            </div>
            <span><button @click="handleSingIn">cart</button></span>
          </div>
        </div>
        <hr />
        <div class="product-box">
          <div>
            <span>Phone</span>
          </div>
          <div>
            <span>Watch</span>
          </div>
          <div>
            <span>Wallet</span>
          </div>
          <div>
            <span>Sunglasses</span>
          </div>
          <div>
            <span>Belt</span>
          </div>
          <div>
            <span>Jewellery & Accessories</span>
          </div>
          <div>
            <span>Casual-Footwear</span>
          </div>
          <div>
            <span>formal-shoes</span>
          </div>
        </div>
        <hr />
      </nav>
      <section>
        <div>
          <h1>Your cart item </h1>
          <h3 v-if="cartItem.value == null" >Your cart is empty please add item </h3>
        </div>
      </section>
  
      <div class="card-container" v-if="cartItem.value != null">
        <div class="cards" v-for="(item, index) in cartItem" :key="index">
          <div class="image" >
            <img :src="item.image" />
            <div class="title">
              <h3>Name : {{ item.name }}</h3>
              <h3>Material : Synthetic</h3>
            </div>
            <div class="des">
              <p>price : {{ item.price }}</p>
              <button @click="handleRemoveItem(item, index)">remove-from-cart</button>
            </div>
          </div>
        </div>
      </div>
  
      <footer>
        <div class="box-1">
          <div>
            <a
              href="https://www.meesho.io/jobs?utm_medium=footer&utm_source=meesho_website&utm_campaign=careerspagepromotion"
              target="_blank"
              >Careers</a
            >
          </div>
          <div>
            <a
              href="https://supplier.meesho.com/?utm_source=meesho&utm_medium=mweb&utm_campaign=footer"
              target="_blank"
              >Become a supplier</a
            >
          </div>
          <div>
            <a href="https://www.meesho.com/legal/hall-of-fame?embed=true"
              >Hall of Fame</a
            >
          </div>
          <div>
            <a href="https://www.meesho.com/sitemap">Sitemap</a>
          </div>
        </div>
        <div class="box-2">
          <div>
            <a href="https://www.meesho.com/legal?embed=true"
              >Legal and Policies</a
            >
          </div>
          <div>
            <a
              href="https://www.meesho.io/blog?utm_medium=footer&utm_source=meesho_website&utm_campaign=blogpagepromotion"
              >Meesho Tech Blog</a
            >
          </div>
          <div>
            <a href="https://www.meesho.com/notices_and_returns?embed=true"
              >Notices and Returns</a
            >
          </div>
        </div>
        <div class="box-3">
          <div>
            <h6>Reach out to us</h6>
          </div>
          <div>
            <a href="https://www.facebook.com/meeshosupply"
              ><i class="ri-facebook-box-fill"></i
            ></a>
            <a href="https://www.instagram.com/meeshoapp/"
              ><i class="ri-instagram-fill"></i
            ></a>
            <a href="https://www.youtube.com/channel/UCaGHIRKYUYlaI_ZAt2hxpjw"
              ><i class="ri-youtube-fill"></i
            ></a>
            <a
              href="https://www.linkedin.com/authwall?trk=bf&trkInfo=AQFa6qVeNdEp2wAAAYxY7s_YZg5fM7Ld3gOhmCkwppoboTFCS_1lveChTzHCvojo4zt3ay51g9dkLx3uOdQ-qr7gFFkxJ1_uap-8gnYPYry59BGvqqJFeshQIVBM2kpY1OXI6w4=&original_referer=&sessionRedirect=https%3A%2F%2Fwww.linkedin.com%2Fcompany%2Fmeesho"
              ><i class="ri-linkedin-box-fill"></i
            ></a>
            <a href="https://twitter.com/Meesho_Official/"
              ><i class="ri-twitter-fill"></i
            ></a>
          </div>
        </div>
        <div class="box-4">
          <h3>Contact Us</h3>
          Fashnear Technologies Private Limited,
          <br />
          CIN: U74900KA2015PTC082263
          <br />
          06-105-B, 06-102, (138 Wu) Vaishnavi Signature, No. 78/9,
          <br />
          Outer Ring Road, Bellandur, Varthur Hobli,
          <br />
          Bengaluru-560103, Karnataka, India
          <br />
          E-mail address:
          <a href="mailto:query@meesho.com">query@meesho.com</a>
          <br />
          © 2015- 2023 Meesho.com
        </div>
      </footer>
    </div>
  </template>
  
  
  <script setup>
  import { onMounted } from "vue";

  let cartItem = reactive({});
  
  function handleRemoveItem(item, index) {
      console.log("item", item)
      console.log("index", index)
      localStorage.removeItem("cartItem");
      getLocalstorageData()
  }
  
  function getLocalstorageData() {
      let localStorageData = JSON.parse(localStorage.getItem("cartItem"));
      console.log("localStorageData", localStorageData)
      cartItem.value = localStorageData ? localStorageData : null
  }
  
  onMounted(() => {
  //   cartItem.value = JSON.parse(localStorage.getItem("cartItem"));
      getLocalstorageData()
  });
  </script>