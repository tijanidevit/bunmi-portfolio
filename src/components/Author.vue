<template>
  <div class="author content has-text-centered">
    <g-image
      alt="Author image"
      class="image"
      src="~/assets/images/bunmi.jpg"
    />

    <h1 v-if="showTitle">
      {{ $static.metadata.siteName }}
    </h1>

    <p>{{ $static.metadata.siteDescription }}</p>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: {
    showTitle: {
      type: Boolean,
      default: true,
    },
  },
};
</script>
