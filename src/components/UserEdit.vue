<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <button @click="setUserAge">Edit me!</button>
        <p>User Age {{ userAge }}</p>
    </div>
</template>

<script>
import { eventBus } from "../main.js";

export default {
  props: ["userAge"],
  methods: {
    setUserAge() {
      this.userAge = 30;
      //   this.$emit("ageWasEdited", this.userAge);
      //   eventBus.$emit("ageWasEdited", this.userAge);
      eventBus.changeAge(this.userAge);
    }
  }
};
</script>

<style scoped>
div {
  background-color: lightgreen;
}
</style>
