<template>
  <h2 :id="headingId">Heading</h2>
  <button :disabled="isDisabled">Disabled</button>
  <h2 class="underline">Underline Text</h2>
  <h2 :class="status">Status</h2>
  <h2 :class="isPromoted && 'promoted'">Promoted Movie</h2>
  <h2 :class="isSoldOut ? 'sold-out' : 'new'">New / Sold Out</h2>
  <h2 :class="['new', 'promoted']">Newly promoted movie</h2>
  <h2 :class="[isPromoted && 'promoted', isSoldOut ? 'sold-out' : 'new']">
    Array conditional movie
  </h2>
  <h2 :class="{ promoted: isPromoted, new: !isSoldOut, 'sold-out': isSoldOut }">
    Object Conditional Movie
  </h2>

  <h2 :style="{ color: highlighColor, fontSize: headerSize + 'px' }">Highlighted Text</h2>
  <h2 :style="[baseStyle, successStyle]">Array Highlighted Text</h2>
  <h2 :style="[baseStyle, dangerStyle]">Array Highlighted Text</h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      headingId: "heading-id",
      isDisabled: true,
      status: "danger",
      isPromoted: false,
      isSoldOut: true,
      highlighColor: "orange",
      headerSize: "50",
      baseStyle: {
        fontSize: "20px",
      },
      successStyle: {
        backgroundColor: "green",
      },
      dangerStyle: {
        backgroundColor: "red",
      },
    }
  },
}
</script>

<style scoped>
.underline {
  text-decoration: underline;
}

.promoted {
  font-style: italic;
}

.new {
  color: #00ff00;
}

.sold-out {
  color: #ff0000;
}
</style>
