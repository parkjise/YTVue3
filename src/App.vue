<template>
  <h1>영화정보</h1>
  <div v-for="(movies,index) in data" :key="index">
    <h3 class="bg-yellow" :style="textRed">{{movies.title}}</h3>
    <p>개봉 {{movies.year}}</p>
    <p>장르 : {{movies.category}}</p>
    <button @:click="increseLike(index)">좋아요</button><span>{{movies.like}}</span>
  </div>
  <p>{{foods[0]}}</p>
  <p>{{foods[1]}}</p>
  <p>{{foods[2]}}</p>
  <!-- 반복문 -->
  <div v-for="(item,i) in foods" :key="i">{{item}}</div>
</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        foods:["김밥","순대","만두","떡볶이"],

        data : [
          {
            title:"노랑",
            year:2023,
            category:"액션,드라마",
            textRed:"color:red",
            like:0,
          },
          {
            title:"노랑",
            year:2023,
            category:"액션,드라마",
            textRed:"color:red",
            like:0,
          },
          {
            title:"아쿠아맨",
            year:2024,
            category:"액션,판타지",
            textRed:"color:red",
            like:0,
          },
        ]
      }
    },
    methods: {
      increseLike(index){
        this.data[index].like++
      }
    },
  }
</script>

<style>
.bg-yellow{
  background:yellow;
}
</style>
