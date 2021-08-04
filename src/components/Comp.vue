<template>
	<button @click="$emit('custom:click', 'clicked')">CLICK ME</button>
</template>

<script>
	export default {
		name : 'Comp',
		emits: [ 'custom:click' ]
	}
</script>
