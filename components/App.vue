<template>
  <div>
  <el-form ref="form" label-width="120px">
    <el-input class="decidetext" type="textarea" v-model="choises" placeholder="Варианты, каждый вариант на новой строке"></el-input>
    <br/><br/>
    <el-button type="primary" @click="decide">Реши за меня</el-button>
    <br/><br/>
  <div> Рандомайзер считает что лучше: {{ answer }} </div>
  </el-form>
    
    
  </div>
</template>

<script>
    function random_item(items)
    {
      return items[Math.floor(Math.random()*items.length)];
    }

    export default {
    data() {
      return {
        choises: '',
        answer: 'фар фыр фыр'
      }
    },
    methods: {
      decide: function () {
        this.answer = random_item(this.allChoises)
      }
    },
    computed: {
      allChoises: function() {
        var a = this.choises.split("\n")
        a.push('Пойти поспать');
        return a;
      }
    }
  }
</script>

<style>

.decidetext{
  width: 56%
}
</style>

