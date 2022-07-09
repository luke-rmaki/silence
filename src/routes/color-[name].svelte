<script lang="ts">
	import { page } from '$app/stores';
	import { colors as allColors } from '../lib/colors';

	const name = $page.params.name;
	const colors = allColors[name];
	console.log(colors);
</script>

<div
	style={`
	--color0: ${colors[0]};
	--color1: ${colors[1]};
	--color2: ${colors[2]};
	--color3: ${colors[3]};
	--color4: ${colors[4]};
	--color5: ${colors[5]};
	--color6: ${colors[6]};
	--color7: ${colors[7]};
	--color8: ${colors[8]};
	--color9: ${colors[9]};
	--color10: ${colors[10]};
`}
>
	<a href="/colors">&lt;- Colors</a>
	<h1>{name.toUpperCase()}</h1>
	<ul>
		<li style={`color: var(--color0);`}>0</li>
		<li style={`color: var(--color1);`}>1</li>
		<li style={`color: var(--color2);`}>2</li>
		<li style={`color: var(--color3);`}>3</li>
		<li style={`color: var(--color4);`}>4</li>
		<li style={`color: var(--color5);`}>5</li>
		<li style={`color: var(--color6);`}>6</li>
		<li style={`color: var(--color7);`}>7</li>
		<li style={`color: var(--color8);`}>8</li>
		<li style={`color: var(--color9);`}>9</li>
		<li style={`color: var(--color10);`}>10</li>
	</ul>
	<ul class="bold">
		<li style={`color: var(--color0);`}>0</li>
		<li style={`color: var(--color1);`}>1</li>
		<li style={`color: var(--color2);`}>2</li>
		<li style={`color: var(--color3);`}>3</li>
		<li style={`color: var(--color4);`}>4</li>
		<li style={`color: var(--color5);`}>5</li>
		<li style={`color: var(--color6);`}>6</li>
		<li style={`color: var(--color7);`}>7</li>
		<li style={`color: var(--color8);`}>8</li>
		<li style={`color: var(--color9);`}>9</li>
		<li style={`color: var(--color10);`}>10</li>
	</ul>

	<div class="lighter">
		<ul>
			<li style={`color: var(--color0);`}>0</li>
			<li style={`color: var(--color1);`}>1</li>
			<li style={`color: var(--color2);`}>2</li>
			<li style={`color: var(--color3);`}>3</li>
			<li style={`color: var(--color4);`}>4</li>
			<li style={`color: var(--color5);`}>5</li>
			<li style={`color: var(--color6);`}>6</li>
			<li style={`color: var(--color7);`}>7</li>
			<li style={`color: var(--color8);`}>8</li>
			<li style={`color: var(--color9);`}>9</li>
			<li style={`color: var(--color10);`}>10</li>
		</ul>
		<ul class="bold">
			<li style={`color: var(--color0);`}>0</li>
			<li style={`color: var(--color1);`}>1</li>
			<li style={`color: var(--color2);`}>2</li>
			<li style={`color: var(--color3);`}>3</li>
			<li style={`color: var(--color4);`}>4</li>
			<li style={`color: var(--color5);`}>5</li>
			<li style={`color: var(--color6);`}>6</li>
			<li style={`color: var(--color7);`}>7</li>
			<li style={`color: var(--color8);`}>8</li>
			<li style={`color: var(--color9);`}>9</li>
			<li style={`color: var(--color10);`}>10</li>
		</ul>
	</div>
	<div class="darker">
		<ul>
			<li style={`color: var(--color0);`}>0</li>
			<li style={`color: var(--color1);`}>1</li>
			<li style={`color: var(--color2);`}>2</li>
			<li style={`color: var(--color3);`}>3</li>
			<li style={`color: var(--color4);`}>4</li>
			<li style={`color: var(--color5);`}>5</li>
			<li style={`color: var(--color6);`}>6</li>
			<li style={`color: var(--color7);`}>7</li>
			<li style={`color: var(--color8);`}>8</li>
			<li style={`color: var(--color9);`}>9</li>
			<li style={`color: var(--color10);`}>10</li>
		</ul>
		<ul class="bold">
			<li style={`color: var(--color0);`}>0</li>
			<li style={`color: var(--color1);`}>1</li>
			<li style={`color: var(--color2);`}>2</li>
			<li style={`color: var(--color3);`}>3</li>
			<li style={`color: var(--color4);`}>4</li>
			<li style={`color: var(--color5);`}>5</li>
			<li style={`color: var(--color6);`}>6</li>
			<li style={`color: var(--color7);`}>7</li>
			<li style={`color: var(--color8);`}>8</li>
			<li style={`color: var(--color9);`}>9</li>
			<li style={`color: var(--color10);`}>10</li>
		</ul>
	</div>
</div>

<style lang="scss">
	div {
		height: 100vh;
		width: 100vw;
		background-color: var(--color9);
		padding: 5rem;
		box-sizing: border-box;

		a {
			color: var(--color0);
			font-family: var(--font);
		}

		h1 {
			margin: 0;
			color: var(--color0);
			font-family: var(--font);
		}

		ul {
			list-style-type: none;
			display: flex;
			width: 100%;
			justify-content: space-around;

			li {
				font-family: var(--font);
			}
		}
		.bold {
			li {
				font-weight: bold;
			}
		}
	}

	.lighter,
	.darker {
		background-color: var(--color8);
		padding: 0;
		height: 20rem;
		width: 100%;
		display: flex;
		justify-content: center;
		flex-direction: column;
		align-items: center;
	}

	.darker {
		background-color: var(--color10);
	}
</style>
