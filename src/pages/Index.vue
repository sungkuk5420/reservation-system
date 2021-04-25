<template>
  <q-page class="flex flex-center">
    <div class="menu-page">
      <img src="~assets/images/logo.png" alt srcset class="logo" />
      <div class="menu-area">
        <div
          class="menu-button"
          v-for="(item, index) in menu"
          :key="index"
          @click="moveDetail()"
          :style="
            'background-image:url(' +
            getURL('images/main/' + item.index + '.png') +
            ');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;'
          "
        >
          <span>{{ item.name }}</span>
        </div>
      </div>

      <div class="footer-menu">
        <q-btn class="bg-white" text-color="black" label="주문 이력" />
        <q-btn class="bg-yellow" text-color="black" label="점원 호출" />
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      menu: [
        { name: "메인메뉴", index: 1 },
        { name: "세트메뉴", index: 2 },
        { name: "식사메뉴", index: 3 },
        { name: "사이드 메뉴", index: 4 },
        { name: "디저트", index: 5 },
        { name: "음료", index: 6 },
        { name: "어린이메뉴", index: 7 },
        { name: "포장메뉴", index: 8 },
      ],
    };
  },
  methods: {
    moveDetail() {
      console.log("details");
      this.$router.push("/details");
    },
    getURL(url) {
      return require("assets/" + url);
    },
  },
};
</script>

<style lang="scss">
.menu-page {
  background: #a81501;
  position: fixed;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  flex: none;
  .logo {
    margin-top: auto;
    margin-bottom: auto;
    width: auto;
    height: 150px;
  }
  .menu-area {
    max-width: 1300px;
    margin-bottom: auto;
    margin-bottom: auto;
    display: flex;
    align-items: center;
    width: 100%;
    height: 40%;
    padding: 20px;
    flex-wrap: wrap;
    .menu-button {
      width: calc(25% - 15px);
      height: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex: none;
      background-position: center center;
      background-repeat: no-repeat;
      background: center;
      border-radius: 10px;
      border: 1px solid #ddd;
      &:hover {
        cursor: pointer;
        transform: scale(1.1);
      }
      &:nth-child(1),
      &:nth-child(2),
      &:nth-child(3),
      &:nth-child(5),
      &:nth-child(6),
      &:nth-child(7) {
        margin-right: 20px;
      }
      &:nth-child(1),
      &:nth-child(2),
      &:nth-child(3),
      &:nth-child(4) {
        margin-bottom: 20px;
      }
      span {
        font-size: 28px;
        color: white;
        font-weight: 700;
        text-shadow: 1px 1px 2px black, 0 0 1px black, 0 0 0.2px black;
      }
    }
  }
  .footer-menu {
    margin-top: auto;
    margin-left: auto;
    margin-right: 20px;
    margin-bottom: 20px;
    .q-btn {
      padding: 15px 20px;
      font-size: 24px;
      font-weight: 700;
      &:not(:last-child) {
        margin-right: 20px;
      }
    }
  }
}
</style>

