<script>
export default {
  data() {
    return {
      navItems: [
        {
          title: '平泽唯',
          showDropdown: false,
          submenus: ['下意识吉他手', '平地摔拿手', '团队吐槽役2号']
        },
        {
          title: '相生祐子',
          showDropdown: false,
          submenus: ['狗头人', '运动万能', '数学无能']
        },
        {
          title: '英梨梨',
          showDropdown: false,
          submenus: ['败犬', '最强插话家', '黄毛长直也算长直']
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
<div class="nav-container">
    <div class="nav-bar">
      <div class="nav-logo">
        <img src="https://cdn-image2.ruifeng.me/xiandehuang%2F2018new_doge02_org.png" width="14px">
      </div>

      <div 
        v-for="(item, index) in navItems" 
        :key="index"
        @mouseenter="showDropdown(index)"
        @mouseleave="hideDropdown"
        class="nav-item"
      >
        <span>{{ item.title }}</span>
        <div v-if="item.showDropdown" class="dropdown-container">
          <div class="dropdown-content">
            <div v-for="(submenu, subIndex) in item.submenus" :key="subIndex" class="dropdown-item">{{ submenu }}</div>
          </div>
        </div>
      </div>

      <div class="nav-icons">
        <img src="/magnifying-glass-solid-full.svg" width="14px">
        <img src="/bag-shopping-solid-full.svg" width="14px">
      </div>
    </div>
</div>
</template>
<style>
.nav-container {
  width: 100%;
  color: black;
  font-family: -apple-system, BlinkMacSystemFont, sans-serif;
  font-size: 12px;
  position: relative;
  z-index: 9999;
}

.nav-bar {
  max-width: 980px;
  margin: 0 auto;
  padding: 0 22px;
  display: flex;
  align-items: center;
  height: 44px;
}

.nav-item {
  position: relative;
  margin: 0 15px;
  height: 100%;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.nav-item span {
  opacity: 0.8;
  transition: opacity 0.3s;
}

.nav-item:hover span {
  opacity: 1;
}

.dropdown-container {
  position: fixed;
  top: 44px;
  left: 0;
  right: 0;
  width: 100%;
  color: #000;
  background-color: white;
  overflow: hidden;
  max-height: 0;
  transform: translateY(-20px);
  opacity: 0;
  transition: all 2s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

.nav-item:hover .dropdown-container {
  max-height: 500px;
  transform: translateY(0);
  opacity: 1;
}

.dropdown-content {
  max-width: 980px;
  margin: 0 auto;
  padding: 20px 22px;
  display: flex;
  flex-direction: column;
}

.dropdown-item {
  padding: 8px 0;
  opacity: 0.8;
}

.dropdown-item:hover {
  opacity: 1;
}

.nav-logo, .nav-icons {
  display: flex;
  align-items: center;
}

.nav-icons {
  margin-left: auto;
}

.nav-icons img {
  margin-left: 20px;
}
</style>