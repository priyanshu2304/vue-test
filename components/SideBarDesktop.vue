<template>
  <div class="test-sidebar__section">
    <div class="test-sidebar__container">
      <div v-for="item in options" :key="item.id" class="test-sidebar-items">
        <div class="test-sidebar-item-logo">
          <img :src="item.image" />
        </div>
        <div class="test-sidebar-item-name">{{ item.name }}</div>
      </div>
      <div class="margin-230">
        <div
          v-for="item in bottomOptions"
          :key="item.id"
          class="test-sidebar-items mt-50"
        >
          <div class="test-sidebar-item-logo">
            <img :src="item.image" />
          </div>
          <div class="test-sidebar-item-name">{{ item.name }}</div>
        </div>
      </div>
    </div>
    <div class="test-sidebar__search-container">
      <div class="test-sidebar__search-box">
        <img class="test-sidebar__img" src="~/assets/icons/Search-bar.svg" />
        <div class="test-sidebar__text">Search your cart</div>
        <img class="test-sidebar__img-filter" src="~/assets/icons/Filter.svg" />
      </div>
      <div class="test-sidebar__cart">Your Carts</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SideBarDesktop',
  computed: {
    options() {
      return [
        {
          id: 1,
          name: 'Create class',
          image: require('~/assets/icons/Cart.svg'),
        },
        {
          id: 2,
          name: 'Search Items',
          image: require('~/assets/icons/Search.svg'),
        },
        {
          id: 3,
          name: 'Your Cart',
          image: require('~/assets/icons/Shopping.svg'),
        },
        {
          id: 4,
          name: 'Checkout',
          image: require('~/assets/icons/Dollar-sign.svg'),
        },
      ]
    },

    bottomOptions() {
      return [
        {
          id: 10,
          name: 'Account',
          image: require('~/assets/icons/Account.svg'),
        },
        {
          id: 11,
          name: 'Log out',
          image: require('~/assets/icons/Logout.svg'),
        },
      ]
    },
  },
}
</script>

<style>
.test-sidebar__section {
  display: flex;
  flex-direction: row;
}
.test-sidebar__container {
  width: 115px;
  background-color: #000;
  color: white;
  padding-top: 80px;
  padding-bottom: 25px;
  gap: 50px;
  display: flex;
  flex-direction: column;
}

.test-sidebar-item-name {
  display: flex;
  justify-content: center;
  font-size: 12px;
}

.test-sidebar-item-logo {
  display: flex;
  justify-content: center;
  padding-bottom: 10px;
}

.test-sidebar__search-container {
  padding-top: 40px;
}

.test-sidebar__search-box {
  border: 1px solid #dedede;
  height: 48px;
  width: 283px;
  margin-left: 20px;
  background-color: #f5f0ed;
  border-radius: 20px;
  display: flex;
  margin-right: 50px;
}

.test-sidebar__text {
  font-size: 16px;
  display: flex;
  align-items: center;
  color: #9b9aa2;
}
.test-sidebar__img {
  display: flex;
  padding: 12px;
}
.test-sidebar__img-filter {
  display: flex;
  padding-top: 12px;
  padding-bottom: 12px;
  padding-left: 90px;
}
.test-sidebar__cart {
  margin-left: 20px;
  margin-top: 20px;
  font-size: 16px;
  font-weight: 600;
}

.margin-230 {
  margin-top: 230px;
  padding-left: 20px;
}

.mt-50 {
  margin-top: 50px;
}
</style>
