<template>
	<div class="createform">
		<input type="text" placeholder="Название">
		<input type="text" placeholder="Описание">
		<button>создать</button>
	</div>
</template>

<script setup>

</script>
<style lang="scss">
	.createform
	{
		display: flex;
		flex-direction: column;
		gap: 10px;
		max-width: 400px;
		padding: 10px;
		margin-bottom: 100px;
		input
		{
			border: none;
			border-radius: 10px;
			padding: 10px;
			:active
			{
				border: none;
			}
		}
		button
		{
			border: none;
			border-radius: 10px;
			background-color: yellowgreen;
			padding: 10px;
			cursor: pointer;
		}
	}
</style>