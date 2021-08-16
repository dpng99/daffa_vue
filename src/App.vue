<template>
  <div class="wrapper">
    <nav class="navbar">
      <div class="navbar-brand">
          <router-link to="/" class="navbar-item"><strong>KOZII</strong></router-link>
          <a class="navbarr-burger" aria-label="menu" aria-expanded="false" data-target="navbar-meu" @click="showMobileMenu = !showMobileMenu">
          </a>
      </div> 

      <div class="navbar-menu" id="navbar-menu" v-bind:class="{'is-active':showMobileMenu}">
        <div class="navbar-start">
            <div class="navbar-item">
              <form method="get" action="/search">
                <div class="filed has-addons">
                  <div class="control">
                    <input type="text" class="input">
                  </div>

                  <div class="control">
                    <button class="button is-success">
                      <span class="icon">
                        <i class="fas fa-search"></i>
                      </span>
                    </button>
                  </div>
                </div>
              </form>
            </div>
        </div>
        <div class="navbar-end">
          <router-link to="/login" class="navbar-item">LOGIN</router-link>
          <router-link to="/register" class="navbar-item">Register</router-link>
          <div class="navbar-item">
            <div class="buttons">
              <router-link to="/login" class="button is-light">Login </router-link>
              <router-link to="/cart" class="button is-success">
              <span class="icon"><i class="fas fa-shopping-cart"></i></span>
              <span>Cart</span>
              </router-link> 
            </div>
          </div>
        </div>
        </div>  
        </nav>
        <div class="container">
          <div class="content-wrapper">
            <div class="content-gambar">
              <img src="./gambar/sepeda.png" alt="image/png">
            </div>
            <div class="text-content">
              <h1 class="title">Macbook Air 2020 MWTJ2 13" inch i3 256GB Touch ID Space Grey Japan</h1>
              <h2 class="price">Rp999.999</h2>
              <div class="Kirim">
              <p>Pengiriman</p>
              <label for="kota-pengiriman">
                <select name="kota-pengiriman" id="kota-pengiriman">
                    <option value="KotaJakartaTimur">Kota Jakarta Timur</option>
                    <option value="KotaJakartaBarat">Kota Jakarta Barat</option>
                    <option value="KotaJakartaSelatan">Kota Jakarta Selatan</option>
                    <option value="KotaJakartaUtara">Kota Jakarta Utara</option>
                </select>
              </label>
              <br>
              <br>
              <label for="Pilihan Pengiriman">
                <select name="Pilihan Pengiriman" id="Pilihan Pengiriman">
                    <option value="0">Gratis Ongkir</option>
                    <option value="JNE">Rp.7000</option>
                    <option value="SI Cepat">Rp.9000</option>
                </select>
              </label>
              <p>Varian</p>
              <div class="seletcor-variant">
          
                 
                <button class="btn-pilih first">Hitam</button>
           
                
                <button class="btn-pilih first">Hitam</button>
                
                <button class="btn-pilih first">Hitam</button>
              
                <button class="btn-pilih first">Hitam</button>
               
                <button class="btn-pilih first">Hitam</button>
              
                <button class="btn-pilih first">Hitam</button>
            
                
                <button class="btn-pilih first">Hitam</button>
          
         
                <button class="btn-pilih first">Hitam</button>
               
                 </div>
              </div>
              </div>
            

          </div>

        </div>

      <section class="section">
      <router-view/>
      </section>
      <footer class="footer">
        <p class="has-text-centered"> Copyright 2021</p>
      </footer>
      </div>
</template>
<script>
export default {
  data(){
    return {
      showMobileMenu: false
    }
  }
}
</script>
<style lang="scss">
@import "../node_modules/bulma";
.navbar{
  background:#fd5d31; 
}
.icon{
  position: relative;
}
.container{
   box-shadow: 2px 2px 2px 2px #D4D4D4;
  background: white;
  justify-content: center;
  align-items: center;
  margin-top: 50px;
  height: 500px;
  width: 900px;
}
.wrapper{
 background: #FEFEF3;
}
.content-wrapper{
padding: 3rem calc((100vw-1300px)/2);
margin-top: 50px;
display: grid;
grid-template-columns: 1fr 1fr;
grid-template-rows: 800px;
}
.text-content {
  margin-left: 20px;
  
}
.btn-pilih{
box-sizing: border-box;
  -webkit-appearance: none;
     -moz-appearance: none;
          appearance: none;
  background-color: transparent;
  border: 2px solid #e74c3c;
  border-radius: 0.6em;
  color: #e74c3c;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  align-self: center;
  font-size: 1rem;
  font-weight: 400;
  line-height: 1;
  margin: 10px;
  padding: 1.2em 2.8em;
  text-decoration: none;
  text-align: center;
  text-transform: uppercase;
  position: relative;
}
.btn-pilih:hover, btn-pilih:focus{
  color: #fff;
  outline: 0;
}
.selector-variant-btn{

justify-content: center;
position: absolute;

}
.selector-variant{
display: grid;
grid-template-columns: 1fr 1fr;
grid-template-rows: 10px;
justify-content: center;
}

.first {
  transition: box-shadow 300ms ease-in-out, color 300ms ease-in-out;
}
.first:hover {
  box-shadow: 0 0 40px 40px #e74c3c inset;
}
</style>
