<template>
	<button @click="$emit('custom:click', 'clicked')">CLICK (this === undefined)</button>
</template>

<script>
	export default {
		name : 'Comp',
		emits: [ 'custom:click' ]
	}
</script>
