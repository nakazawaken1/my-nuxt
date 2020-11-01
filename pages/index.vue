<template>
  <div>
    <h1>Todo リスト</h1>
    <table>
      <tr><th>連番</th><th>内容</th><th>完了</th><th>追加日時</th></tr>
      <tr v-for="(todo, i) in todos" :key="i">
        <td>{{i + 1}}</td>
        <td>{{todo.title}}</td>
        <td><input type="checkbox" :checked="todo.done"/></td>
        <td>{{format(todo.created_at)}}</td>
      </tr>
      <tr>
        <td>新規</td>
        <td><input type="text" v-model="title"/></td>
        <td></td>
        <td><button>追加</button></td>
      </tr>
    </table>
    {{title}}
  </div>
</template>

<script>
export default {
  data() {
    return {
      todos: [
        { title: '歯磨き', done: true, created_at: new Date() },
        { title: '宿題', done: false, created_at: new Date() },
      ],
      title: null,
    }
  },
  methods: {
    format(date) {
      return date.getFullYear()
        + '/' + (date.getMonth() + 1)
        + '/' + date.getDate()
        + ' ' + date.getHours()
        + ':' + date.getMinutes();
    }
  }
}
</script>

<style>
th, td {
  border: 1px solid silver;
}
</style>
