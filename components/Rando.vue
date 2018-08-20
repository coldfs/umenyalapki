<template>
  <el-form ref="form" label-width="120px">
    <el-input class="decidetext" type="textarea" v-model="choises" placeholder="Варианты, каждый вариант на новой строке"></el-input>
    <br/><br/>
    <el-button type="primary" @click="decide">Реши за меня</el-button>
    <br/><br/>
    <div> Рандомайзер считает что лучше: {{ answer }} </div>
  </el-form>
</template>

<script>
export default {
  data() {
    return {
      choises: '',
      answer: 'фар фыр фыр'
    }
  },
  methods: {
    decide: function () {
      this.answer = this.allChoises[Math.floor(Math.random() * this.allChoises.length)];
    }
  },
  computed: {
    allChoises: function() {
      return this.choises.split("\n").concat(['Пойти поспать']);
    }
  }
}
</script>

<style>
.decidetext{
  width: 56%
}
</style>

