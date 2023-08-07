<template>
	<div class="container">
		<!-- <CreateForm /> -->
		<ListTodo />
	</div>
</template>

<script>
import CreateForm from "@/components/CreateForm.vue";
import ListTodo from "@/components/ListTodo.vue";
</script>

<style>
*
{
	margin: 0;
}
.container
{
	max-width: 1440px;
	width: 100%;
	height: 100%;
	margin: 0 auto;
	padding: 150px 150px;
	background-color: #DBD7D2;
}
</style>