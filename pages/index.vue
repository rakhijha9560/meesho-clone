
<template>
    <div>
      <!-- start nav -->
      <nav>
        <div class="navBox-1">
          <div>
            <img
              id="Dark-logo"
              src="https://images.moneycontrol.com/static-mcnews/2023/06/Meesho-682x435.jpg?impolicy=website&width=1600&height=900"
              alt="Dark-logo"
            />
          </div>
          <div>
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
            <span>phone</span>
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
          <h1>Products For You</h1>
        </div>
      </section>
  
      <div class="projects-container">
        <div class="cards" v-for="(product, index) in products" :key="index">
          <div class="image">
            <img :src="product.image" />
          </div>
          <div class="title">
            <h3>Name: {{ product.name }}</h3>
            <h3>Material: {{ product.material }}</h3>
          </div>
          <div class="des">
            <p>Price: {{ product.price }}$</p>
            <button @click="handleBuyNow">Buy Now</button>
            <span>
              <button @click="handleAddToCart(product)">Add to Cart</button>
            </span>
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
    </div>
  </template>
    
  
  <script setup>
  import { useRouter } from "vue-router";
  const router = useRouter();
  
  const handleSingIn = () => {
    router.push("/cart");
    return;
  };

  const handleBuyNow = () => {
    router.push("/address");
    return;
  };
  
  const products = [
    {
      image: "https://images.meesho.com/images/products/340497338/j6lgm_512.webp",
      name: "02_  i-phnoe12",
      material: "000",
      price: "50,000$",
    },
    {
      image: "https://images.meesho.com/images/products/27060117/6rkci_512.webp",
      name: "Mesh Strap All Black",
      material: "AnalogueSize-Free",
      price: "5,000$",
    },
    {
      image: "https://images.meesho.com/images/products/201822547/g5vfw_512.webp",
      name: "02_Leather Wallet",
      material: "PU",
      price: "1500$",
    },
    {
      image: "https://images.meesho.com/images/products/23048258/48047_512.webp",
      name: "Men Sunglasses, Goggles",
      material: "size/free-size",
      price: "2000$",
    },
    {
      image: "https://images.meesho.com/images/products/317140742/ykatn_512.webp",
      name: "02_Leather-belt",
      material: "PU",
      price: "1300$",
    },
    {
      image: "https://images.meesho.com/images/products/310291894/1yz96_512.webp",
      name: "necklace",
      material: "gold",
      price: "85000$",
    },
    {
      image: "https://images.meesho.com/images/products/54151475/t6f06_512.webp",
      name: "_casual-shoes",
      material: "Synthetic",
      price: "2500$",
    },
    {
      image: "https://images.meesho.com/images/products/193054110/yp9pd_512.webp",
      name: "02_Black Boots",
      material: "Leather",
      price: "5000$",
    },
  ];
  
  function handleAddToCart(data) {
    localStorage.setItem("cartItem", JSON.stringify(data));
  }
  </script>

