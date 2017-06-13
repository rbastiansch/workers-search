<template>
	<form class="form-inline my-2 my-lg-0">
	<button class="btn btn-outline-success my-2 my-sm-0" type="submit" @click.prevent="loadFuncionarios">Buscar Funcionários</button>
	</form>
</template>

<script>

export default{
  name: 'search',
  methods: {
    loadFuncionarios() {
      this.$http.get('https://slimapp-rbastiansch.c9users.io/public/index.php/api/funcionarios').then((response) => {
        this.$emit('loadFunc', response.body);
      }, (response) => {
        console.error(response);
      });
    },
  },
};
</script>
