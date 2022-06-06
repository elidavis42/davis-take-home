<template>
  <div class="card" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">Did you know?</h5>
    <p class="card-text">{{fact}}</p>
    <a class="btn btn-primary" @click="$emit('newFact')">Get Another Fact </a>
  </div>
</div>
</template>

<script>
export default {
  name: 'FactDisplay',
  props: {
    fact: String
  }
}
</script>
