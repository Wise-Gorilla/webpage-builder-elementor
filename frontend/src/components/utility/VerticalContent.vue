<template>
  <div class="text-left">
    <label for="radio" class="font-weight-bold">Vertical :</label>
    <b-form-group>
      <b-form-radio-group
        v-model="selected"
        :options="options"
        name="vertical"
      ></b-form-radio-group>
    </b-form-group>
  </div>
</template>

<script>
export default {
  props: {
    vertical: String
  },
  data() {
    return {
      selected: this.vertical,
      options: [
        { text: "Start", value: "start" },
        { text: "Center", value: "center" },
        { text: "End", value: "end" }
      ]
    };
  },
  watch: {
    selected: function(val) {
      this.$emit("changeVertical", val);
    }
  }
};
</script>
