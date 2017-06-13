<template>
	<div class="col mt-2">
		<CSearch @loadFunc="loadFunc"></CSearch>
		<CList v-if="seen" :funcionarios="funcionarios"></CList>
	</div>
</template>

<script>
import CSearch from './Search';
import CList from './List';

export default{
  name: 'principal',
  components: {
    CSearch,
    CList,
  },
  data() {
    return {
      seen: false,
      funcionarios: [],
    };
  },
  methods: {
    loadFunc(result) {
      this.funcionarios = result;
      this.seen = true;
    },
  },
};
</script>
