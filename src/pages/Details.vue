<template>
  <q-page class="flex flex-center">
    <div class="details-page">
      <img src="~assets/images/logo.png" alt srcset class="logo">
      <div class="row justify-center category-buttons-wrapper">
        <q-btn-toggle
          class="category-buttons"
          glossy
          v-model="slide"
          :options="[
          { label: '메인메뉴', value: 'category11' },
          { label: '세트메뉴', value: 'category21' },
          { label: '식사메뉴', value: 'category31' },
          { label: '사이드 메뉴', value: 'wait1' },
          { label: '디저트', value: 'wait2' },
          { label: '음료', value: 'wait3' },
          { label: '어린이메뉴', value: 'wait4' },
          { label: '포장메뉴', value: 'wait5' },
        ]"
        />
      </div>
      <div class="menu-area">
        <q-carousel
          v-model="slide"
          transition-prev="slide-right"
          transition-next="slide-left"
          animated
          control-color="primary"
          class="rounded-borders"
        >
          <q-carousel-slide name="category11" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category11"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category1/category1-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category12" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category12"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category1/category1-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category21" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category21"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category2/category2-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category22" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category22"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category2/category2-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category31" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category31"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category3/category3-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category32" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category32"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category3/category3-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category41" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category21"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category2/category2-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="category42" class="column no-wrap flex-center">
            <div
              :class="item.index!=0?'menu-button':'menu-button disabled-button'"
              v-for="(item,index) in category22"
              :key="index"
              @click="addCart(index)"
              :style="item.index!=0?'background-image:url('+getURL('images/category2/category2-'+item.index+'.png')+');background-repeat: no-repeat;background-position: center center; background-size:100% 100%;':''"
            >
              <span>{{item.name}}</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="wait1" class="column no-wrap flex-center">
            <div>
              <span>준비중입니다.</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="wait2" class="column no-wrap flex-center">
            <div>
              <span>준비중입니다.</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="wait3" class="column no-wrap flex-center">
            <div>
              <span>준비중입니다.</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="wait4" class="column no-wrap flex-center">
            <div>
              <span>준비중입니다.</span>
            </div>
          </q-carousel-slide>
          <q-carousel-slide name="wait5" class="column no-wrap flex-center">
            <div>
              <span>준비중입니다.</span>
            </div>
          </q-carousel-slide>
        </q-carousel>
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      slide: "category11",
      category11: [
        { name: "모듬회", index: 1 },
        { name: "과메기", index: 2 },
        { name: "회무침", index: 3 },
        { name: "안심", index: 4 },
        { name: "등심", index: 5 },
        { name: "삼겹살", index: 6 },
        { name: "목살", index: 7 },
        { name: "살치살", index: 8 }
      ],
      category12: [
        { name: "갈비살", index: 9 },
        { name: "돼지갈비", index: 10 },
        { name: "항정살", index: 11 },
        { name: "양념갈비", index: 12 },
        { name: "모듬 곱창구이", index: 13 },
        { name: "고추장 삼겹살", index: 14 },
        { name: "", index: 0 },
        { name: "", index: 0 }
      ],
      category21: [
        { name: "뚝배기 불고기", index: 1 },
        { name: "회 덮밥", index: 2 },
        { name: "얼큰 육개장", index: 3 },
        { name: "소고기 무국", index: 4 },
        { name: "돌솥 비빔밥", index: 5 },
        { name: "돌솥 날치알밥", index: 6 },
        { name: "비빔 냉면", index: 7 },
        { name: "물 냉면", index: 8 }
      ],
      category22: [
        { name: "돼지 김치찌개", index: 9 },
        { name: "김밥", index: 10 },
        { name: "해물 된장찌개", index: 11 },
        { name: "해물 순두부찌개", index: 12 },
        { name: "제육 덮밥", index: 13 },
        { name: "김치 볶음밥", index: 14 },
        { name: "", index: 0 },
        { name: "", index: 0 }
      ],
      category31: [
        { name: "해물 파전", index: 1 },
        { name: "녹두 빈대떡", index: 2 },
        { name: "오징어 볶음", index: 3 },
        { name: "제육 볶음", index: 4 },
        { name: "두부 김치", index: 5 },
        { name: "돈까스", index: 6 },
        { name: "해물 오뎅탕", index: 7 },
        { name: "마른 안주", index: 8 }
      ],
      category32: [
        { name: "고등어 구이", index: 9 },
        { name: "계란말이", index: 10 },
        { name: "김치전", index: 11 },
        { name: "감자전", index: 12 },
        { name: "감자튀김", index: 13 },
        { name: "", index: 0 },
        { name: "", index: 0 },
        { name: "", index: 0 }
      ]
    };
  },
  methods: {
    addCart(index) {},
    getURL(url) {
      return require("assets/" + url);
    }
  }
};
</script>

<style lang="scss">
.details-page {
  background: #a81501;
  position: fixed;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: flex-end;
  // justify-content: center;
  align-items: center;
  flex-direction: column;
  flex: none;
  .category-buttons-wrapper {
    width: 100%;
  }
  .category-buttons {
    width: 100%;
    .q-btn {
      flex: 1;
      color: white;
      font-size: 16px;
      font-weight: 700;
      background: #443a39 !important;
      &.bg-primary {
        background: #ffc107 !important;
      }
    }
  }

  .menu-area {
    max-width: 1300px;
    margin-top: auto;
    display: flex;
    align-items: center;
    width: 100%;
    height: 40%;
    padding: 0;
    margin: 0;
    flex-wrap: wrap;
    flex: none;
    height: 400px;
    .menu-button {
      width: calc(25%);
      height: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      flex: none;
      background-position: center center;
      background-repeat: no-repeat;
      background: center;
      border-radius: 10px;
      &:not(.disabled-button) {
        background: #9f200f;
        border: 1px solid #ddd;
      }
      &:not(.disabled-button):hover span {
        cursor: pointer;
        transform: scale(1.2);
      }
      span {
        font-size: 28px;
        color: white;
        font-weight: 700;
        text-shadow: 1px 1px 2px black, 0 0 1px black, 0 0 0.2px black;
      }
    }
  }
  .q-carousel {
    width: 100%;
    // height: 500px;
    .q-carousel__slide {
      padding: 0;
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
    }
  }
}
</style>

