<template>
  <div class="test-body__container">
    <div class="test-body__header-section">
      <div class="">
        <div class="test-body__heading">Builder</div>
        <div class="test-body__sub-heading">
          Drag and drop your items from your cart to create your design.
        </div>
      </div>
      <div class="test-body__three-dots">
        <img src="@/assets/icons/3dots.svg" />
      </div>
    </div>
    <div class="test-body__dialog-container">
      <div class="dialog-container__box">
        <div class="dialog-box__cross">
          <img src="~/assets/icons/cross.svg" />
        </div>
        <div class="dialog-box__heading">CREATE NEW DRESS CODE</div>
        <div class="dialog-box__description">
          Your cart hold all of your items. Don’t forget to name your cart for
          easy identification.
        </div>
        <div class="dialog-box__edit-box">
          <img src="~/assets/icons/edit-pen.svg" />
          <div class="edit-text">1st Grade Girls</div>
        </div>
        <div class="button-container">
          <button class="solid-button">GO TO BUILDER</button>
        </div>
      </div>
      <div class="test-body__footer">Total $6230.00</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainBody',
}
</script>

<style>
.test-body__header-section {
  display: flex;
  justify-content: space-between;
}

.test-body__container {
  padding: 30px;
  width: 100%;
}

.test-body__heading {
  font-size: 24px;
  font-weight: 700;
}

.test-body__sub-heading {
  opacity: 0.5;
  font-weight: 400;
  font-size: 16px;
}

.test-body__three-dots {
  margin-right: 80px;
}

.test-body__dialog-container {
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.dialog-container__box {
  width: 622px;
  height: 416px;
  padding: 20px;
  background: #ffffff;
  /* Neutrals (Lightest Gray) */

  border: 1px solid #dedede;
  /* Style 1 (Desktop */

  box-shadow: 1px 9px 18px 5px rgba(45, 45, 45, 0.2);
}

.dialog-box__cross {
  display: flex;
  justify-content: flex-end;
}

.dialog-box__heading {
  font-size: 40px;
  font-weight: 700;
  display: flex;
  justify-content: center;
}

.dialog-box__description {
  font-size: 20px;
  opacity: 0.8;
  display: flex;
  justify-content: center;
  padding: 40px 70px 25px;
}

.dialog-box__edit-box {
  margin: 0 70px;
  border-bottom: 1px solid black;
  display: flex;
  flex-direction: row;
}

.edit-text {
  margin-left: 15px;
}

.solid-button {
  display: flex;
  background-color: black;
  color: white;
  font-weight: 700;
  padding: 15px 61px;
}

.button-container {
  display: flex;
  padding-top: 40px;
  justify-content: center;
}

.test-body__footer {
  font-weight: 700;
  font-size: 40px;
  padding-top: 150px;
}
</style>
