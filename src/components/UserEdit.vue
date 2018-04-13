<template>
    <div class="component">
        <h3>You may edit the User here</h3>
        <button @click="setUserAge">Edit me!</button>
        <p>User Age {{ userAge }}</p>
    </div>
</template>

<script>
export default {
  props: ["userAge"],
  methods: {
    setUserAge() {
      this.userAge = 30;
      this.$emit("ageWasEdited", this.userAge);
    }
  }
};
</script>

<style scoped>
div {
  background-color: lightgreen;
}
</style>
