<script>
export default {
  data() {
    return {
      navItems: [
        {
          title: '平泽唯',
          showDropdown: false,
          submenus: ['Submenu 1', 'Submenu 2', 'Submenu 3']
        },
        {
          title: '相生祐子',
          showDropdown: false,
          submenus: ['Submenu A', 'Submenu B']
        },
        {
          title: '英梨梨',
          showDropdown: false,
          submenus: ['Submenu X', 'Submenu Y', 'Submenu Z']
        }
      ]
    };
  },
  methods: {
    showDropdown(index) {
      this.navItems.forEach((item, i) => {
        if (i === index) {
          item.showDropdown = true;
        } else {
          item.showDropdown = false;
        }
      });
    },
    hideDropdown() {
      this.navItems.forEach(item => {
        item.showDropdown = false;
      });
    }
  }
};
</script>
<template>
<div class="outterBar">
    <ul class="innerBar">
      <li class="col"><img class="col" src="https://cdn-image2.fengrin.me/xiandehuang%2F2018new_doge02_org.png" width="14px"></li>

      <li
        v-for="(item, index) in navItems" 
        :key="index"
        @mouseover="showDropdown(index)"
        @mouseleave="hideDropdown"
        class="col"
      >
        {{ item.title }}
        <div v-if="item.showDropdown" class="dropdown">
          <ul>
            <li v-for="(submenu, subIndex) in item.submenus" :key="subIndex">{{ submenu }}</li>
          </ul>
        </div>
      </li>
      <li class="col"><img src="https://cdn-image2.fengrin.me/xiandehuang%2Ffangdajing.png" width="14px"></li>
      <li class="col"><img src="https://cdn-image2.fengrin.me/xiandehuang%2Fbag.png" width="14px"></li>
    </ul>
</div>

</template>
<style>
    .innerBar {
      display: grid;
      grid-template-columns: repeat(13, 1fr);
      grid-gap: 10px;
      background-color: rgb(20, 19, 19);
      width: 75%;
    }

    .col {
      padding: 10px;
      display: flex;
      align-items: center;
      position: relative;
    }
    .outterBar {
        display: grid;
        place-items: center; /* 水平和垂直居中 */
        background-color: rgb(20, 19, 19);
        color: gray;
        font-size: 9pt;
        position: relative;
    }



    .navbar {
  position: relative;
}

ul {
  list-style-type: none;
}

.dropdown {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #fff;
  border: 1px solid #ccc;
  padding: 10px;
  display: none;
}

li:hover .dropdown {
  display: block;
}
</style>