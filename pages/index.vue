<template>
  <div>
    <h1>Todo リスト</h1>
    <table>
      <tr><th>内容</th><th>完了</th><th>追加日</th></tr>
    </table>
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
th, td {
  border: 1px solid silver;
}
</style>
