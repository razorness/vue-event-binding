<template>
	<div class="hello">
		<h1>{{ msg }}</h1>
		<p>
			<button @click="foo.trigger">CLICK</button>
		</p>
		<p>
			<comp @custom:click="foo.trigger"/>
		</p>
	</div>
</template>

<script>
	import Comp from '@/components/Comp';

	class Foo {

		bar = 'foobar';

		trigger() {
			console.log(this, arguments);
		}

	}

	export default {
		name      : 'HelloWorld',
		components: {Comp},
		props     : {
			msg: String
		},
		data() {
			return {foo: new Foo()}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	h3 {
		margin: 40px 0 0;
	}

	ul {
		list-style-type: none;
		padding: 0;
	}

	li {
		display: inline-block;
		margin: 0 10px;
	}

	a {
		color: #42b983;
	}
</style>
