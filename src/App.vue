
<template>
  <div class="container-fluid">
      <div class="row">
          <div class="col-1"></div>
          <div class="col-4">
            <div class="row">
                <div class="col-2">
                  <h2 class="text-nowrap">The First Degree Equation</h2>
                </div>
              </div>
              <div class="row">
                <div class="col-4">
                  <label for="" class="text-nowrap">Enter first number</label>
                

                  <input type="number" class="form-control" v-model="a">
                </div>
              </div>

              <div class="row">
                <div class="col-4">
                  <label for="" class="text-nowrap">Enter second number</label>
                

                  <input type="number" class="form-control" v-model="b">
                </div>
              </div>

              <div class="row">
                <div class="col-3">
                  <button v-on:click="calculate" class="btn btn-success mt-4">Answer</button>
                </div>
              </div>

              <div class="row">
                <div class="col-3">
                  <p v-if:="answer" class="btn btn-success mt-4">
                    {{ answer }}
                  </p>
                </div>
              </div>

          </div>
          
          <div class="col-4">
            <div class="row">
              <div class="col-2">
                <h2 class="text-nowrap">Second Degree Equation</h2>
              </div>
            </div>

            <div class="row">
                <div class="col-4">
                    <label for="">Enter first number</label>

                    <input type="number" class="form-control" v-model="aa">
                </div>
            </div>

            <div class="row">
                <div class="col-4">
                    <label for="">Enter second number</label>

                    <input type="number" class="form-control" v-model="bb">
                </div>
            </div>

            <div class="row">
                <div class="col-4">
                    <label for="">Enter third number</label>

                    <input type="number" class="form-control" v-model="cc">
                </div>
            </div>

            <div class="row">
                <div class="col-4">
                    <button class="btn btn-success mt-4" v-on:click="calculer">Answer</button>  
                </div>
            </div>

            <div class="row">
                <div class="col-4">
                    <button class="btn btn-success" v-if="reponse">Answer</button>  
                </div>
            </div>
          </div>
      </div>
  </div>
</template>

<script setup>
  import {ref} from 'vue';
    const a = ref(null)
    const b = ref(null)
    const answer = ref('')

    const calculate = () =>{
      if (a== 0 && b== 0) {
        "real set"
      }else if
        (b!=0 && a==0){
          "empty set"
        }else if
          (a!=0){
            const x = -b.value/a.value;
            answer.value = `x = ${x}`
          }         
    }

    const aa = ref(null)
    const bb = ref(null)
    const cc = ref(null)
    const reponse = ref('')

    const calculer = () =>{
      if (aa==0 && bb==0 && cc==0) {
        "real set"  
      }else if(aa==0 && bb==0 && cc!=0){
        "empty set"
      }else if(aa==0 && bb!=0){
        const x = -cc.value/bb.value;
        reponse.value = `x=${x}`
      }
      if (aa!=0) {
        
      }
    }
</script>

<style scoped></style>
