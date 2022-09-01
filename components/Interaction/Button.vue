<template>
  <div>
    <b-button v-if="forwardFacing" class="btn-primary">
      <span class="button-content">
        {{ buttonContent }}
      </span>

      <span
        class="material-symbols material-symbols-outlined btn-primary-chevron"
      >
        chevron_right
      </span></b-button
    >
    <b-button v-else class="btn-primary">
      <span
        class="material-symbols material-symbols-outlined btn-primary-chevron chevron-left"
      >
        chevron_left
      </span>
      <span class="button-content">
        {{ buttonContent }}
      </span>
    </b-button>
  </div>
</template>

<script>
export default {
  name: "Button",
  props: ["buttonContent", "forwardFacing"],
};
</script>

<style>
.btn-primary {
  /* width: 150px; */
  border-radius: 15px;
  background-color: #ff5e98;
  border: none;
  padding: 10px 20px;
  font-weight: bold;
  font-size: 1.2rem;
  display: flex;
  align-items: center;
  justify-content: center;
}
.btn-primary:hover {
  background-color: #172d4e;
  text-decoration: none;
}
.btn-primary-chevron {
  margin-left: 15px;
}
.chevron-left {
  margin-right: 15px;
  margin-left: 0;
}
</style>
