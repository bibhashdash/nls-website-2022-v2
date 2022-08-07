<template>
  <div>
    <li>
      <h2>title</h2>
      <p>body</p>
    </li>
  </div>
</template>

<script>
import stories from "~/data/data";
export default {
  name: "story",
  props: ["id"],
  data() {
    return {
      stories,
      id,
    };
  },
};
</script>

<style></style>
