# Vue

#### 指令

1. ##### v-bind(:)

   1. 用于绑定HTML的Attribute
   2. 可用v-bind:[attributename]="value"的方式动态参数绑定

2. ##### v-on(@)

   1. 用于监听Dom事件
   2. 可用v-bind:[methodname]="value"的方式动态参数绑定

3. ##### v-for

   1. 用于循环数据

      ```
      <div id="app-4">
        <ol>
          <li v-for="todo in todos">
            {{ todo.text }}
          </li>
        </ol>
      </div>
      ```

      ```Html
      var app4 = new Vue({
        el: '#app-4',
        data: {
          todos: [
            { text: '学习 JavaScript' },
            { text: '学习 Vue' },
            { text: '整个牛项目' }
          ]
        }
      })
      ```

4. ##### v-if

   1. 控制显示和隐藏

      ```
      <div id="app-3">
        <p v-if="seen">现在你看到我了</p>
      </div>
      ```

      ```
      var app3 = new Vue({
        el: '#app-3',
        data: {
          seen: true
        }
      })
      ```

5. ##### v-model

   1. 实现表单输入和应用状态之间的双向绑定

      ```
      <div id="app-6">
        <p>{{ message }}</p>
        <input v-model="message">
      </div>
      ```

      ```
      var app6 = new Vue({
        el: '#app-6',
        data: {
          message: 'Hello Vue!'
        }
      })
      ```

6. ##### v-once

   1. 一次性地插值，当数据改变时，插值处的内容不会更新

      ```
      <span v-once>这个将不会改变: {{ msg }}</span>
      ```

7. ##### v-html

   1. 输出真正的 HTML

      ```
      //rawHtml=<span>This is word</span>
      <p>Using mustaches: {{ rawHtml }}</p>
      <p>Using v-html directive: <span v-html="rawHtml"></span></p>
      ```

#### Vue属性

1. ##### el

   1. 绑定Dom元素

2. ##### data

   1. Vue对象内数据

3. ##### methods

   1. Vue对象内方法

4. ##### created

   1. Vue对象生命周期--Vue创建结束

5. ##### mounted

   1. Vue对象生命周期--el绑定结束

6. ##### updated

   1. Vue对象生命周期--data修改结束

7. ##### destroyed

   1. Vue对象生命周期--Vue销毁结束

8. ##### computed

   1. 计算属性

9. ##### watch

   1. 侦听属性
   
10. ##### components

   1. 局部组件注册

#### Vue名词

1. 组件化应用构建
2. Object.freeze()
3. 前缀 $
4. 生命周期
5. 参数与动态参数
6. 修饰符

