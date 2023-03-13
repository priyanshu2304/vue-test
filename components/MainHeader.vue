<template>
  <div class="test-header_container">
    <img class="test-header__image" src="@/assets/icons/logo.svg" />
    <div class="test-header__user-info">
      <div class="test-header__choose-language">
        Choose Language
        <img
          class="test-header__down-arrow"
          src="@/assets/icons/DownArrow.svg"
        />
      </div>
      <div class="test-header__user-name">
        <img
          class="test-header__user-profile"
          src="@/assets/icons/UserProfile.svg"
        />
        Chloe Johnson
        <img
          class="test-header__down-arrow"
          src="@/assets/icons/DownArrow.svg"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderSection',
}
</script>

<style >
.test-header_container {
  padding: 15px 32px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.test-header__user-info {
  display: flex;
  font-size: 12px;
}

.test-header__down-arrow {
  margin-left: 20px;
}

.test-header__user-name {
  display: flex;
  margin-left: 80px;
  align-items: center;
}

.test-header__user-profile {
  display: flex;
  margin-right: 5px;
}

.test-header__choose-language {
  display: flex;
  align-items: center;
}

@media only screen and (max-width: 1100px) {
  .test-header_container {
    padding: 10px ;
  }

  .test-header__user-name {
    display: flex;
    margin-left: 10px;
    align-items: center;
  }

  .test-header__user-info {
   margin-left: 10px;
  }
}
</style>
