<template>
  <section class="container">
    <div>
      <h1 class="title">
        Post Item {{ id }}
      </h1>
    </div>
  </section>
</template>

<script>
export default {
  validate ({ params }) {
    // Must be a number
    return /^\d+$/.test(params.id)
  },

  asyncData ({ params }) {
    // called every time before loading the component
    return {
      id: params.id
    }
  }
}
</script>
