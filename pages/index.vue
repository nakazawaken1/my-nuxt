<template>
  <div>
    <h1>Todo リスト</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        { title: '歯磨き', done: false, created_at: new Date() },
        { title: '宿題', done: false, created_at: new Date() },
      ]
    }
  }
}
</script>

<style>
</style>
