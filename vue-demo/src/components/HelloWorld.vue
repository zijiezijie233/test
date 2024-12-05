<template>
  <div class="hello">
    <h3>学习vue3.0</h3>
    <h1 v-if="flag">Vue is awesome!</h1>
    <h1 v-else>Vue is not awesome!</h1>
    <h1 v-show="flag">I like Vue!</h1>
    <ul>
      <li v-for="(item, index) in newList" :key="item.id">
        {{ index}} + {{ item.name }}
      </li>
    </ul>
    <button @click="counter += 1">
      点击:counter {{ counter }}
    </button>
    <button @click="clickHandle">按钮</button>
    <h1>{{ message }}</h1>
    <button @click="say('hi')">say hi</button>
    <button @click="say('watch')">say what</button>
    <ul>
      <li @click="clickItemHandle(item)" v-for="(item, index) in names" :key="index">{{ item }}</li>
    </ul>
    <input type="text" v-model.lazy.trim="username">
     <input type="text" v-model.trim ="password">
    <h1>{{ username }},{{ password }}</h1>
    <button @click="clickGetUsername">获取用户名</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      flag: true,
      newList: [
        { id: 1, name: 'vue3.0' },
        { id: 2, name: 'react' },
        { id: 3, name: 'angular' }
      ],
      counter: 1,
      message: 'Hello Vue3.0',
      names: ['tom', 'jerry', 'kitty'],
      username: '',
      password: '',
      
    }
  },
  methods: {
    clickHandle(event) {
      //读取data中的数据，通过this
      this.message = 'Hello Hello Vue3.0'
      console.log(event)  //event是原生的事件对象
      event.target.innerHTML = '按钮被点击了'
    },
    say(data) {
      console.log(data)
    },
    clickItemHandle(item) {
      console.log(item)
    },
    clickGetUsername() {
      console.log(this.username + this.password)
    }
  }
}
</script>


