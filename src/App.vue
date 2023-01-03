<template>
  <header>
    <Nav />
  </header>
  <main>
    <p>이중 중괄호를 사용한 용법 : {{ rawHtml }}</p>
    <p>v-html 지시자(directive) 를 사용한 용법<span v-html="rawHtml"></span></p>
    <hr>
    <h4>속성 바인딩</h4>
    <div v-bind:id="dynamicId1">v-bind:속성명="변수명"</div>
    <div :id="dynamicId2">:속성명="변수명"</div>
    <hr>
    <h5>불린 속성</h5>
    <button :disabled="isButtonDisabled">버튼</button>
    <hr>
    <h5>다중 속성</h5>
    <input v-bind="multiAttribute"><br>
    <hr>
    <h4>자바 스크립트 식 사용</h4>
    <div>
      {{ 1 + 1 }}<br>
      {{ isTrue ? '참' : '거짓' }}<br>
      {{ rawHtml.split(' ') }}
    </div>
    <h4>함수 사용</h4>
    <div v-html="hello()"></div>
    <div>{{ totalNumber(10, 20) }}</div>
  </main>
  <footer>
    여기에는 풋터가 들어 갑니다.
  </footer>
</template>

<script>
import Nav from './components/NavMenu.vue'

export default {
  components: {
    Nav
  },
  methods: {
    hello: function() { return 'Hello'; },
    totalNumber: function(x, y) { return x + y; }
  },
  data() {
    return {
      rawHtml: '이것은 변수에 저장된 문자열',
      dynamicId1: 'dynamicId1',
      dynamicId2: 'dynamicId2',
      isButtonDisabled: true,
      multiAttribute: {
        id: 'id_input', name: 'name_input', type: 'number'
      },
      isTrue: false
    }
  }
}
</script>