<script lang="ts">
	import { colors } from '../lib/colors';

	const colorNames = Object.keys(colors);

	const list = colorNames
		.map((name) => {
			return colors[name].map((color, index) => {
				const varName = `--${name}-${index}`;
				const value = `${color}`;
				return `${varName}: ${value};`;
			});
		})
		.flat();
</script>

<ul>
	{#each list as item}
		<li>{item}</li>
	{/each}
</ul>

<style lang="scss">
	ul {
		list-style: none;
	}
</style>
