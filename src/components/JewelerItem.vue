<template>
  <div class="container-jeweler" 
    @mouseup="
      (e) => {
        handleMouseUp(e);
      }
    "
  >
    <div
      @mousemove="
        (e) => {
          handleMouseMove(e);
        }
      "
      @mousedown="
        (e) => {
          handleMouseDown(e);
        }
      "
      :style="classObject"
      class="jeweler container transform-component"
      id="handle_mobile"
    >
      <!-- Manager -->
      <div class="info-manage">
        <button class="btn-info-manage cursor-btn">
          <div class="btn-content">Manager</div>
          <img
            src="https://game.defikingdoms.com/static/media/bubble-arrow.905173b2.png"
            alt=""
          />
        </button>
      </div>
      <div class="info-jeweler">
        <button class="btn-info-manage cursor-btn">
          <div class="btn-content">Jeweler</div>
          <img
            src="https://game.defikingdoms.com/static/media/bubble-arrow.905173b2.png"
            alt=""
          />
        </button>
      </div>
      <div class="info-info">
        <button class="btn-info-info cursor-btn">
          <!-- <div class="btn-content">Manager</div> -->
          <img
            src="https://game.defikingdoms.com/static/media/text_bubble_excl_mark.4ef4a151.png"
            alt=""
          />
        </button>
      </div>
      <div class="hero-manage">
        <img
          src="https://game.defikingdoms.com/static/media/bank-npc.8f28ffae.png"
          alt="hero_manager"
        />
      </div>
      <div class="table-manager">
        <img
          src="https://game.defikingdoms.com/static/media/bank-desk3.ead9fc47.png"
          alt=""
        />
      </div>
      <div class="table-jeweler">
        <img
          src="https://game.defikingdoms.com/static/media/bank-desk2.02d89879.png"
          alt=""
        />
      </div>
      <div class="table-info">
        <img
          src="https://game.defikingdoms.com/static/media/bank-desk3.ead9fc47.png"
          alt=""
        />
      </div>
      <button class="layout-btn btn-manage cursor-btn">
        <label for="input__id__manage"></label>
      </button>
      <div>
        <input type="checkbox" class="input__modal" id="input__id__manage" />

        <div class="modal">
          <label for="input__id__manage" class="modal__overlay"></label>
        </div>
        <div class="modal__body manage">
          <div class="modal__body__container">
            <div class="modal_body_head">
              <div class="title">Locked JEWEL Management</div>
            </div>
            <div class="modal_body_content">
              <div class="border_content">
                <div class="head">Manager Greg</div>
                <div class="body">
                  Thank you for being a valued client! If you have locked JEWEL,
                  I can assist you with transferring it to another wallet. I can
                  only transfer the full balance, so make sure you want to move
                  everything!
                </div>
              </div>
              <div class="introduce">
                <div>
                  This function will transfer all of your wallet and locked
                  JEWEL from one wallet to another. You can use this function if
                  your wallet has been compromised or if you are moving to a
                  hardware wallet.
                </div>
                <div>
                  You can only transfer the full balance of your locked JEWEL.
                  Only wallets with active DeFi Kingdoms accounts may receive
                  locked JEWEL.
                </div>
                <div>
                  All unclaimed rewards should be claimed prior to transfer.
                  Additionally, all JEWEL in the transferring wallet will be
                  moved to the new wallet when using this feature. If you do not
                  wish to move your unlocked JEWEL, deposit it with the Jeweler
                  before using this transfer option. xJEWEL will not be
                  transferred and will need to be sent manually.
                </div>
                <div>
                  The recipient wallet address must be different from the
                  current wallet. If you try to transfer locked JEWEL to the
                  same wallet that it is already in, it will be lost forever.
                </div>
              </div>
              <div class="total-locked">
                <p>Total Locked JEWEL</p>
                <p>
                  <img
                    src="https://game.defikingdoms.com/static/media/cute-jewel.4849f9a3.png"
                    alt=""
                  />
                  0.00
                </p>
              </div>
              <div class="total-wallet">
                <p>Total Locked JEWEL</p>
                <p>
                  <img
                    src="https://game.defikingdoms.com/static/media/cute-jewel.4849f9a3.png"
                    alt=""
                  />
                  0.00
                </p>
              </div>
              <div style="padding: 10px 15px">
                <label for="address" class="cursor-btn"
                  >Recipient Address</label
                >
                <input type="text" id="address" />
              </div>
              <div style="padding: 0 15px">
                <div class="warning">
                  <img
                    src="https://game.defikingdoms.com/static/media/warning.e34a399d.svg"
                    alt=""
                  />
                  <p>
                    Warning: This process is irreversible. There is no way to
                    cancel or undo this transfer, so be sure that you entered
                    the correct wallet address and that it is not the same
                    wallet that contains the locked JEWEL that you are
                    attempting to move.
                  </p>
                  <input type="text" placeholder="Type 'SEND'" />
                </div>
                <button
                  disabled="disabled"
                  class="btn-transfer-locked cursor-btn"
                >
                  TRANSFER LOCKED JEWEL
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <button class="layout-btn cursor-btn btn-jeweler">
        <label for="input__id__jeweler"></label>
      </button>
      <div>
        <input type="checkbox" class="input__modal" id="input__id__jeweler" />

        <div class="modal">
          <label for="input__id__jeweler" class="modal__overlay"></label>
        </div>
        <div class="modal__body info">
          <div class="modal__body__container">
            <div class="modal_body_head">
              <div class="title">Info</div>
            </div>
            <div class="modal_body_content">
              <div class="border_content">
                <div class="head">Jeweler Micah</div>
                <div class="body">
                  Welcome to Adelyn, the greatest city in Serendale! You can
                  deposit your JEWEL here at the Jeweler, and visit the
                  Marketplace to trade tokens. Lazarus the Druid is also there;
                  he can help you acquire seeds which you can plant in the
                  Gardens to participate in liquidity pools and earn rewards!
                </div>
                <div class="footer">
                  You can find Heroes for sale in the Tavern, or visit the
                  Portal to Summon new ones. Again, welcome, and enjoy your
                  stay! If you need more information about anything you find
                  here, visit docs.defikingdoms.com to learn more.
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <button class="layout-btn cursor-btn btn-info">
        <label for="input__id__info"></label>
      </button>
      <div>
        <input type="checkbox" class="input__modal" id="input__id__info" />

        <div class="modal">
          <label for="input__id__info" class="modal__overlay"></label>
        </div>
        <div class="modal__body info">
          <div class="modal__body__container">
            <div class="modal_body_head">
              <div class="title">Info</div>
            </div>
            <div class="modal_body_content">
              <div class="border_content">
                <div class="head">Jeweler Micah</div>
                <div class="body">
                  Welcome to Adelyn, the greatest city in Serendale! You can
                  deposit your JEWEL here at the Jeweler, and visit the
                  Marketplace to trade tokens. Lazarus the Druid is also there;
                  he can help you acquire seeds which you can plant in the
                  Gardens to participate in liquidity pools and earn rewards!
                </div>
                <div class="footer">
                  You can find Heroes for sale in the Tavern, or visit the
                  Portal to Summon new ones. Again, welcome, and enjoy your
                  stay! If you need more information about anything you find
                  here, visit docs.defikingdoms.com to learn more.
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <button class="layout-btn cursor-btn btn-lila">
        <label for="input__id__lila"></label>
      </button>
      <div>
        <input type="checkbox" class="input__modal" id="input__id__lila" />

        <div class="modal">
          <label for="input__id__lila" class="modal__overlay"></label>
        </div>
        <div class="modal__body">
          <div class="modal__body__container">
            <div class="modal_body_head">
              <div class="title">Lila</div>
            </div>
            <div class="modal_body_content">
              <i class="title">* mumble mumble *</i>
              <div>So many bills... not enough JEWEL...</div>
            </div>
          </div>
        </div>
      </div>
      <div class="hero-jeweler">
        <img
          src="https://game.defikingdoms.com/static/media/teller-idle.053534ac.png"
          alt="hero_jeweler"
        />
      </div>
      <div class="hero-info">
        <img
          src="https://game.defikingdoms.com/static/media/banker-idle.ff6a4d3f.png"
          alt="hero_info"
        />
      </div>
      <div class="hero-lila">
        <img
          src="https://game.defikingdoms.com/static/media/lila-animation.a9794464.png"
          alt="hero_lila"
        />
      </div>
      <div class="bank-eyes">
        <img
          src="https://game.defikingdoms.com/static/media/bank-eyes.049bd9ec.png"
          alt="bank_eyes"
        />
      </div>
      <div class="bank-lights">
        <div style="width: 1712px; height: 1392.97px; z-index: 1000; position: absolute"></div>
        <img
          src="https://game.defikingdoms.com/static/media/bank-lights.e8e3bf99.png"
          alt="bank_lights"
        />
      </div>
      <div class="bankShine">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-statue.783a90a5.png"
          alt="bankShine"
        />
      </div>
      <div class="bankShine-chestTL">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-chestTL.fb167560.png"
          alt="bankShine-chestTL"
        />
      </div>
      <div class="bankShine-chestTC">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-chestTC.25ffd514.png"
          alt="bankShine-chestTC"
        />
      </div>
      <div class="bankShine-pig">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-pig.b50be6a6.png"
          alt="bankShine-pig"
        />
      </div>
      <div class="bankShine-chestTR">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-chestTR.f063b7b8.png"
          alt="bankShine-chestTR"
        />
      </div>
      <div class="bankShine-vaseL">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-vaseL.0195a7db.png"
          alt="bankShine-vaseL"
        />
      </div>
      <div class="bankShine-vaseR">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-vaseL.0195a7db.png"
          alt="bankShine-vaseR"
        />
      </div>
      <div class="bankShine-chestBL">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-chestBL.648c7ab8.png"
          alt="bankShine-chestBL"
        />
      </div>
      <div class="bankShine-chestBR">
        <img
          src="https://game.defikingdoms.com/static/media/bankShine-chestBR.0e721d9a.png"
          alt="bankShine-chestBR"
        />
      </div>
      <div class="pumpkin">
        <img
          src="https://game.defikingdoms.com/static/media/Pumpkin01.4f7e453e.png"
          alt="pumpkin"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default({
  name: 'JewelerItem',
  data() {
    return {
      scaleNumber: {
        x: 1,
        y: 1,
        locationInitialX: 0,
        locationInitialY: 0,
        isMouseDown: false,
      },
      classObject: {},
      isModal: false,
      a: 0,
      b: 0,
      c: 0,
      d: 0,
      e: 0,
      f: 0,
      };
  },

  mounted(){ 
    console.log(this.c)
    var el = document.getElementById("handle_mobile");
    el.addEventListener("touchstart", handleStart, false);
    el.addEventListener("touchmove", handleMove, false);
    function handleStart(e){
      this.isMouseDown = true;
      this.c = e.touches[0].clientX - e.touches[0].target.getBoundingClientRect().left;
      this.d = e.touches[0].clientY - e.touches[0].target.getBoundingClientRect().top;
    }

    function handleMove(e){
      console.log(e.touches[0].pageY - this.d)
      if (this.isMouseDown) {
        if(e.touches[0].pageX - this.c < 300 && e.touches[0].pageX - this.c > -1500 && e.touches[0].pageY - this.d > -1200 && e.touches[0].pageY - this.d < 700){
          handle_mobile.style.left = `${e.touches[0].pageX - this.c}px`
          handle_mobile.style.top = `${e.touches[0].pageY - this.d}px`
        }
      } 
    }
  },

  methods: {
  handleMouseMove(e) {
    let finalX = 0
    let finalY = 0
    if (this.isMouseDown) {
      if(window.innerWidth > 1700){
        finalX = e.pageX - this.a - this.scaleNumber.locationInitialX
        finalY = e.pageY - this.b - this.scaleNumber.locationInitialY;
        this.classObject = {
          transform: `scale(${this.scaleNumber.x}, ${this.scaleNumber.y}) translate(${finalX}px, ${finalY}px)`,
        };
      }
      else{
        if(e.pageX - this.c < 500 && e.pageX - this.c > -500 && e.pageY - this.d > -500 && e.pageY - this.d < 500){
          this.classObject = {
          left: `${e.pageX - this.c}px`,
          top: `${e.pageY - this.d}px`
        }
        }
      }
    } 
    else {
      if(window.innerWidth > 1700){
        this.classObject = {
        transform: `scale(${this.scaleNumber.x}, ${this.scaleNumber.y}) translate(${0}px, ${0}px)`,
        transition: "transform 1.5s",
        };
      }
      }
  },

  handleMouseDown(e) { 
    this.isMouseDown = true;
    if(window.innerWidth > 1700){
      this.a = e.target.getBoundingClientRect().left;
      this.b = e.target.getBoundingClientRect().top;
      this.scaleNumber.locationInitialX = e.offsetX;
      this.scaleNumber.locationInitialY = e.offsetY;
    }
    else{
      this.c = e.clientX - e.target.getBoundingClientRect().left;
      this.d = e.clientY - e.target.getBoundingClientRect().top;
    }
  },
  handleMouseUp() {
    this.isMouseDown = false;
  },
  },
})
</script>


<style scoped>
.btn-lila label,
.btn-manage label,
.btn-info label,
.btn-jeweler label {
  width: 100%;
  height: 100%;
  cursor: url(https://game.defikingdoms.com/static/media/click-cursor-2x.113d2d1d.png),
    auto;
}

.modal__body {
  position: fixed;
  /* transition: all linear 10s; */
  transition: opacity 10s ease-in-out;
  -webkit-transition: opacity 10s ease-in-out;
  -moz-transition: opacity 10s ease-in-out;
  opacity: 0;
  overflow: auto;
  z-index: 7000;
  display: none;
  margin: auto;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  max-width: 420px;
  height: fit-content;
  border: 1px solid rgb(76, 62, 35);
  background-color: rgba(0, 0, 0, 0.85);
}

.modal__body div{
  color: #fff;
}

/* .modal__body__container {
  width: 100%;
  border: 1px solid rgb(76, 62, 35);
  background-color: rgba(0, 0, 0, 0.85);
  transition: all linear 0.9s;
} */

.modal_body_head {
  text-align: center;
  width: 100%;
}

.modal_body_head .title {
  font-size: 2rem;
  font-family: Lora;
  padding: 0.6rem 3.5rem;
  background: rgba(0, 0, 0, 0.9);
}

.modal_body_content {
  padding: 1.8rem 1.8rem;
}

.modal_body_content div {
  margin-top: 10px;
}

.modal__body.info {
  max-width: 650px;
}

.modal__body.info .modal_body_content {
  font-family: Lora;
  font-size: 1.2rem;
}

.modal__body.info .modal_body_content .head {
  margin: 0;
}

.modal__body.manage {
  max-width: 650px;
}

.modal__body.manage .modal_body_content {
  overflow: scroll;
  max-height: 60vh;
}

.modal__body.manage .modal_body_content::-webkit-scrollbar {
    display: none;
}


.modal__body.manage .warning p {
  width: 290px;
  font-size: 0.8rem;
}

.modal__body.manage .warning {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  background-color: rgba(255, 61, 0, 0.65);
  padding: 10px;
}

.modal__body.manage .warning input {
  height: 35px;
  width: 150px;
  border: 1px solid rgb(250, 192, 93);
  border-radius: 8px;
  font-size: 0.7rem;
  background: transparent;
  text-shadow: rgb(0 0 0 / 85%) 1px 1px 0px;
  background-color: black;
  color: white;
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  flex-wrap: nowrap;
  -webkit-box-align: center;
  align-items: center;
  font-weight: 400;
  font-size: 12px;
  text-align: center;
}

.btn-transfer-locked {
  position: relative;
  color: #fff;
  background: #009c44;
  font-size: 13px;
  letter-spacing: 1px;
  padding: 10px 30px;
  display: block;
  width: 100%;
  margin-top: 10px;
  border: none;
  border-radius: 4px;
  opacity: 0.4;
}

.modal__body.manage .introduce {
  padding: 15px;
}

.modal__body.manage .total-locked p,
.modal__body.manage .total-wallet p {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 1.2rem;
  margin: 0;
}

.modal__body.manage .total-locked p img,
.modal__body.manage .total-wallet p img {
  width: 14px;
  height: 14px; 
  margin-right: 5px;
}

.modal__body.manage .total-wallet {
  margin-top: 25px;
}

.modal__body.manage #address {
  display: block;
  width: 100%;
  padding: 10px 15px;
  background-color: transparent;
  outline: none;
  border: 1px solid #fff;
  color: #fff;
}

.border_content {
  border: 1px solid rgb(76, 62, 35);
  padding: 1rem;
  background-image: linear-gradient(
    to right,
    rgba(0, 0, 0, 0.8),
    rgba(0, 0, 0, 0.5)
  );
}

.modal {
  position: fixed;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  display: none;
  animation: fadein linear 0.3s;
  z-index: 6000;
  width: 100%;
  height: 100%;
}
.modal__overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  /* background-color: rgba(0, 0, 0, 0.4); */
  background-color: rgba(30, 30, 30, 0.5);
  cursor: url(https://game.defikingdoms.com/static/media/default-cursor-2x.946e7535.png),
    auto;
}

@keyframes fadein {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.input__modal {
  display: none;
}
.input__modal:checked ~ .modal {
  display: flex;
}
.input__modal:checked ~ .modal__body {
  display: block;
  opacity: 1;
}

.jeweler {
  position: absolute;
  background-image: url(https://game.defikingdoms.com/static/media/bank-bg.6b091ffd.png);
  min-width: 1718px;
  height: 1392.97px;
  z-index: 1;
  background-size: 100%;
  image-rendering: pixelated;
  background-repeat: no-repeat;
  margin: 0 auto;
}

.cursor-btn {
  cursor: url(https://game.defikingdoms.com/static/media/click-cursor-2x.113d2d1d.png),
    auto;
}

.layout-btn {
  overflow: hidden;
  background-color: transparent;
  border: 0px;
  outline: 0px;
  z-index: 5000;
  width: 136.081px;
  height: 156.101px;
  position: absolute;
}

.btn-manage {
  left: 810.176px;
  top: 253.672px;
}

.btn-jeweler {
  left: 801.176px;
  top: 700px; 
}

.btn-info {
  left: 361.176px;
  top: 711px;
  width: 102.081px;
  height: 156.101px;
}

.btn-lila {
  left: 650.176px;
  top: 665px;
}

.btn-info.focus,
.btn-info:focus,
.btn-info:hover {
  color: unset;
  background-color: unset;
  border-color: unset;
}

.btn-info:not(:disabled):not(.disabled).active,
.btn-info:not(:disabled):not(.disabled):active,
.show > .btn-info.dropdown-toggle {
  color: unset;
  background-color: unset;
  border-color: unset;
}
.btn-info:not(:disabled):not(.disabled).active[data-v-fd8b9234],
.btn-info[data-v-fd8b9234]:not(:disabled):not(.disabled):active,
.show > .btn-info.dropdown-toggle[data-v-fd8b9234] {
  color: unset;
  background-color: unset;
  border-color: unset;
}

.btn-info:not(:disabled):not(.disabled).active:focus,
.btn-info:not(:disabled):not(.disabled):active:focus,
.show > .btn-info.dropdown-toggle:focus {
  -webkit-box-shadow: none;
  box-shadow: none;
}

.btn-info.focus,
.btn-info:focus {
  /* -webkit-box-shadow: 0 0 0 0.2rem rgb(58 176 195 / 50%); */
  box-shadow: none;
}

.hero-manage img {
  width: 81.081px;
  height: 116.101px;
  position: absolute;
  left: 841.176px;
  top: 292.672px;
}

.hero-jeweler,
.hero-info,
.hero-lila,
.bank-eyes,
.bank-lights,
.bankShine,
.bankShine-chestTL,
.bankShine-chestTC,
.bankShine-pig,
.bankShine-chestTR,
.bankShine-vaseL,
.bankShine-vaseR,
.bankShine-chestBL,
.bankShine-chestBR,
.pumpkin {
  position: absolute;
  left: 838.176px;
  top: 764px;
  width: 65.081px;
  height: 116.101px;
  z-index: 188;
  overflow: hidden;
}

.hero-info {
    left: 380.176px;
    top: 766.672px;
}
.hero-lila {
  left: 619.176px;
  top: 690.672px;
  width: 112.081px;
}
.bank-eyes {
  left: 1407.176px;
  top: 138.672px;
  width: 101.081px;
  height: 84.101px;
}
/* .bank-lights {
  width: 1400px;
  height: 1392.97px;
  top: 0px;
  left: 0px;
  z-index: 400;
} */

.bank-lights {
  width: 1712px;
  height: 1392.97px;
  top: 0px;
  left: 0;
  z-index: 400;
}

.bankShine {
  width: 132.162px;
  height: 159.162px;
  top: 170.297px;
  left: 220.73px;
}

.bankShine-chestTL {
  width: 139.297px;
  height: 139.297px;
  top: 274.595px;
  left: 369.459px;
}

.bankShine-chestTC {
  width: 97.297px;
  height: 87.297px;
  top: 254.162px;
  left: 706.486px;
}

.bankShine-pig {
  width: 92.8649px;
  height: 46.4324px;
  top: 235.162px;
  left: 1023.51px;
}

.bankShine-chestTR {
  width: 139.297px;
  height: 92.8649px;
  top: 227.162px;
  left: 1341.54px;
}

.bankShine-vaseL {
  width: 92.8649px;
  height: 46.4324px;
  top: 645.054px;
  left: 604.622px;
}

.bankShine-vaseR {
  width: 92.8649px;
  height: 46.4324px;
  top: 649.054px;
  left: 1048.622px;
}

.bankShine-chestBL {
  width: 92.8649px;
  height: 139.297px;
  top: 1020.081px;
  left: 1532px;
}

.bankShine-chestBR {
  width: 92.8649px;
  height: 139.297px;
  top: 825.081px;
  left: 1235px;
}

.pumpkin {
  width: 92.8649px;
  height: 139.297px;
  top: 777.081px;
  left: 1569px;
}

.hero-jeweler img,
.hero-info img {
  position: absolute;
  min-width: 670.368px;
  height: 101.571px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 11s steps(11, end) 0s infinite normal none running dKpWqB;
}

@keyframes dKpWqB {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -670px;
    top: 0;
  }
}

.bank-eyes img {
  position: absolute;
  min-width: 6686.27px;
  min-width: 2414.49px;
  height: 92.8649px;

  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 13s steps(26, end) 0s infinite normal none running
    animate-bank-eyes;
}

@keyframes animate-bank-eyes {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -2414.49px;
    top: 0;
  }
}

.hero-lila img {
  position: absolute;
  min-width: 6686.27px;
  height: 101.571px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 14s steps(48, end) 0s infinite normal none running
    animate-hero-lila;
}

@keyframes animate-hero-lila {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -6686.27px;
    top: 0;
  }
}

.bank-lights img {
  position: absolute;
  min-width: 6880px;
  height: 1391.97px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 1.2s steps(4) 0s infinite normal none running animate-bank-lights;
}

@keyframes animate-bank-lights {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -6880px;
    /* top: 0; */
  }
}

.bankShine img {
  position: absolute;
  min-width: 20894.6px;
  height: 232.162px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 9s steps(90, end) 0s infinite normal none running animate-bankShine;
}

@keyframes animate-bankShine {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -20894.6px;
    top: 0;
  }
}

.bankShine-chestTL img {
  position: absolute;
  min-width: 10168.7px;
  height: 139.297px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 7.3s steps(73, end) 0s infinite normal none running
    animate-bankShine-chestTL;
}

@keyframes animate-bankShine-chestTL {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -10168.7px;
    top: 0;
  }
}

.bankShine-chestTC img {
  position: absolute;
  width: 12815.4px;
  height: 139.297px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 9.2s steps(92, end) 0s infinite normal none running
    animate-bankShine-chestTC;
}

@keyframes animate-bankShine-chestTC {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -12815.4px;
    top: 0;
  }
}

.bankShine-pig img {
  position: absolute;
  min-width: 6686.27px;
  height: 46.4324px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 7.2s steps(72, end) 0s infinite normal none running
    animate-bankShine-pig;
}

@keyframes animate-bankShine-pig {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -6686.27px;
    top: 0;
  }
}

.bankShine-chestTR img {
  position: absolute;
  min-width: 11979.6px;
  height: 92.8649px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 8.6s steps(86, end) 0s infinite normal none running
    animate-bankShine-chestTR;
}

@keyframes animate-bankShine-chestTR {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -11979.6px;
    top: 0;
  }
}

.bankShine-vaseL img {
  position: absolute;
  min-width: 7429.19px;
  height: 46.4324px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 8s steps(80, end) 0s infinite normal none running
    animate-bankShine-vaseL;
}

@keyframes animate-bankShine-vaseL {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -7429.19px;
    top: 0;
  }
}

.bankShine-vaseR img {
  position: absolute;
  min-width: 7429.19px;
  height: 46.4324px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 8.1s steps(81, end) 0s infinite normal none running
    animate-bankShine-vaseR;
}

@keyframes animate-bankShine-vaseR {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -7429.19px;
    top: 0;
  }
}

.bankShine-chestBL img {
  position: absolute;
  min-width: 8079.24px;
  height: 139.297px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 8.7s steps(87, end) 0s infinite normal none running
    animate-bankShine-chestBL;
}

@keyframes animate-bankShine-chestBL {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -8079.24px;
    top: 0;
  }
}

.bankShine-chestBR img {
  position: absolute;
  min-width: 8079.24px;
  height: 139.297px;
  image-rendering: pixelated;
  transform: scale(1, 1);
  animation: 8.8s steps(88, end) 0s infinite normal none running
    animate-bankShine-chestBR;
}

@keyframes animate-bankShine-chestBR {
  0% {
    left: 0;
    top: 0;
  }
  100% {
    left: -8079.24px;
    top: 0;
  }
}

.pumpkin img {
  position: absolute;
  width: 63.8649px;
  height: 79.8649px;
  image-rendering: pixelated;
  transform: scale(1, 1);
}

.table-manager img {
  position: absolute;
  width: 279px;
  height: 183px;
  top: 327.027px;
  left: 742.919px;
  overflow: hidden;
  display: flex;
  padding: 0px;
  border: 0px;
  background-color: transparent;
  z-index: 370;
}

.table-jeweler img {
  position: absolute;
  width: 232px;
  height: 139px;
  top: 790px;
  left: 742.919px;
  overflow: hidden;
  display: flex;
  padding: 0px;
  border: 0px;
  background-color: transparent;
  z-index: 370;
}

.table-info {
  position: absolute;
min-width: 276px;
    height: 186px;
    top: 784px;
    left: 275.919px;
  overflow: hidden;
  display: flex;
  padding: 0px;
  border: 0px;
  background-color: transparent;
  z-index: 370;
}

.container-jeweler {
  background-color: #131313;
  height: 100vh;
  width: 100vw;
  padding: 0 !important;
  position: absolute;
  left: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: url(https://game.defikingdoms.com/static/media/default-cursor-2x.946e7535.png),
    auto;
  overflow: hidden;
}

.transform-component {
  /* display: flex; */
  /* flex-wrap: wrap; */
  /* width: -moz-fit-content; */
  /* width: fit-content; */
  /* height: -moz-fit-content; */
  /* height: fit-content; */
  /* margin: 0; */
  /* padding: 0; */
  /* transform-origin: 0% 0%; */
}

.info-manage {
  position: absolute;
  top: 258.868px;
  left: 879.216px;
}

.info-jeweler {
  position: absolute;
  top: 703.868px;
  left: 867.216px;
}

.info-info {
  position: absolute;
  top: 696.868px;
  left: 414px;
}

.btn-info-manage {
  animation: 4.5s ease-in-out 0s infinite normal none running animate-btn;
  pointer-events: revert !important;
  position: relative;
  background-image: url(https://game.defikingdoms.com/static/media/text-bubble-left.c3f30af7.png),
    url(https://game.defikingdoms.com/static/media/text-bubble-right.2fb52ccb.pngg);
  background-position: left top, right top;
  background-repeat: repeat-y;
  background-color: rgb(255, 224, 183);
  background-size: 11.6081px 8.70608px;
  image-rendering: initial;
  left: -50%;
  z-index: 2000;
  border: 0;
}

@keyframes animate-btn {
  0% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0);
  }
}

.btn-info-manage::before {
  content: '';
  display: block;
  position: absolute;
  top: -11.6081px;
  left: 11.6081px;
  width: calc(100% - 23.2162px);
  height: calc(100% + 23.2162px);
  background-image: url(https://game.defikingdoms.com/static/media/text-bubble-top.d04e86af.png),
    url(https://game.defikingdoms.com/static/media/text-bubble-btm.6e7dfc5b.png);
  background-position: center top, center bottom;
  background-repeat: repeat-x;
  background-size: 46.4324px 11.6081px;
}

.btn-info-manage::after {
  content: '';
  display: block;
  position: absolute;
  top: -11.6081px;
  left: 0px;
  width: 100%;
  height: calc(100% + 23.2162px);
  background-image: url(https://game.defikingdoms.com/static/media/text-bubble-topLeft.4ef18153.png),
    url(https://game.defikingdoms.com/static/media/text-bubble-topRight.ef4ff233.png),
    url(https://game.defikingdoms.com/static/media/text-bubble-btmLeft.67ba4cac.png),
    url(https://game.defikingdoms.com/static/media/text-bubble-btmRight.52e8daad.png);
  background-position: left top, right top, left bottom, right bottom;
  background-repeat: no-repeat;
  background-size: 26.1182px 27.1182px;
}

.btn-content {
  position: relative;
  text-align: center;
  color: rgb(0, 0, 0);
  padding: 0px 31.9223px;
  font-family: Lora, serif;
  font-weight: bold;
  z-index: 2003;
  font-size: calc(18.1182px);
}

.btn-info-info {
  animation: 4.5s ease-in-out 0s infinite normal none running animate-btn;
  pointer-events: revert !important;
  position: relative;
  background-position: left top, right top;
  background-repeat: repeat-y;
  background-color: rgb(255, 224, 183);
  background-size: 11.6081px 8.70608px;
  image-rendering: initial;
  left: -50%;
  z-index: 2000;
  border: 0;
}

.btn-info-manage img {
  position: absolute;
  width: 23.2162px;
  height: 20.3142px;
  image-rendering: pixelated;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2002;
}

.btn-info-info img {
  position: absolute;
  min-width: 80.2162px;
  height: 40.3142px;
  image-rendering: pixelated;
  left: 50%;
  transform: translateX(-50%);
  z-index: 2002;
}

.layout-btn {
}

/* .animate-glass {
  background-color: red;
  position: absolute;
  width: 232.162px;
  height: 232.162px;
  top: 114.297px;
  left: 134.73px;
  overflow: hidden;
  z-index: 184;
}

.animate-glass::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 50px;
  height: 100%;
  background: rgba(255, 255, 255, 0.5);
  transform: skewX(45deg) translateX(150px);
  transition: 0.5s;
} */

.info-manage label{
  width: 180px;
  height: 52px;
  position: absolute;
  left: -87px;
  top: -10px;
}
</style>