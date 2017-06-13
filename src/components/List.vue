<template>
	<div class="table-responsive mt-2">
		<table class="table">
			<thead class="thead">
				<tr>
					<th>Código</th>
					<th>Nome</th>
					<th>Função</th>
					<th>Telefone</th>
					<th>Cidade</th>
				</tr>
			</thead>
			<tbody>
				<tr v-for="funcionarios in funcionarios">
					<th scope="row">{{funcionarios.id}}</th>
					<td>{{funcionarios.name}}</td>
					<td>{{funcionarios.job}}</td>
					<td>{{funcionarios.phone}}</td>
					<td>{{funcionarios.city}}</td>
				</tr>
			</tbody>
		</table>
	</div>
</template>

<script>
export default{
  name: 'list',
  props: ['funcionarios'],
};
</script>
