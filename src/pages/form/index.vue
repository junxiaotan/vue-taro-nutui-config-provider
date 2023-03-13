<template>
    <nut-form :model-value='formModel'>
      <nut-form-item label="姓名">
        <nut-input v-model='formModel.name'></nut-input>
      </nut-form-item>
    </nut-form>
   <nut-button type="primary" @click="handleClick">点我</nut-button>
</template>

<script>
import { reactive, toRefs, ref } from 'vue';
export default {
  name: 'Index',
  components: {
  },
  setup() {
    const themeVars = reactive({
      primaryColor:'#008000',
      primaryColorEnd:'#008000',
    });
    const formModel = reactive({
      name: ''
    });
    const handleClick = () => {
      formModel.name = 'test';
    };

    return {
      formModel,
      themeVars,
      handleClick
    }
  }
}
</script>

<style lang="scss">
.index {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
