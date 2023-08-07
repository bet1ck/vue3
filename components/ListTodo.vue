<template>
	<div class="createform">
		<input
			:value="title"
			@input="titleValue"
			type="text"
			placeholder="Название"
		/>
		<input
			:value="text"
			@input="textValue"
			type="text"
			placeholder="Описание"
		/>
		<button @click="createList">создать</button>
	</div>
	<div>
		<div class="list" :key="list.id" v-for="list in lists">
			<div>{{ list.title }}</div>
			<div>{{ list.text }}</div>
			<button @click="deleteList(list.id)">удалить</button>
		</div>
	</div>
</template>

<script setup>
	const lists = reactive([
	{
		id: 1,
		title: "vue",
		text: "описание"
	},
	{
		id: 2,
		title: "vue",
		text: "описание"
	},
	{
		id: 3,
		title: "vue",
		text: "описание"
	}
	])

	const title = ref('');
	const titleValue = (event) => {
		title.value = event.target.value;
	};
	const text = ref('');
	const textValue = (event) => {
		text.value = event.target.value;
	};

	const createList = () => {

	const id = new Date().getTime();
	lists.push({
		id,
		title: title.value,
		text: text.value
	});
	title.value = '';
	text.value = '';
	};
	const deleteList = (id) => {
	const index = lists.findIndex((item) => item.id === id);
	if (index !== -1) {
		lists.splice(index, 1);
	}
	};

</script>

<style>
	.list
	{
		display: flex;
		justify-content: space-between;
		align-items: center;
		border: 1px solid black;
		margin-bottom: 10px;
		padding: 10px;
		width: 400px;
	}
</style>
