<script lang="ts">
	import { colors } from '../lib/colors';

	const colorNames = Object.keys(colors);

	async function copy(color: string) {
		await navigator.clipboard.writeText(color);
	}
</script>

<a class="home" href="/">&lt;- Home</a>
{#each colorNames as name}
	<a href={`/color-${name}`}>
		<span style={`background-color: ${colors[name][4]}`} class="strip">
			<ul>
				{#each colors[name] as color, i}
					<li>
						<p>
							{name}
							{i}
						</p>
						<p>
							{color}
						</p>
					</li>
				{/each}
			</ul>
		</span>
	</a>
	<ul>
		{#each colors[name] as color}
			<li on:click={() => copy(color)} style={`background-color: ${color};`} />
		{/each}
	</ul>
	<span
		style={`background-image: linear-gradient(
      to right,
      ${colors[name][0]},
      ${colors[name][1]},
      ${colors[name][2]},
      ${colors[name][3]},
      ${colors[name][4]},
      ${colors[name][5]},
      ${colors[name][6]},
      ${colors[name][7]},
      ${colors[name][8]},
      ${colors[name][9]},
      ${colors[name][10]}
    )`}
		class="strip"
	/>
{/each}

<style lang="scss">
	a {
		text-decoration: none;
	}
	.strip {
		display: block;
		width: 100vw;
		height: 2rem;

		&:first-child {
			height: 7rem;

			ul {
				height: 100%;
				align-items: center;
				li {
					color: #fff;
				}
			}
		}
	}
	ul {
		list-style-type: none;
		display: flex;
		justify-content: space-between;
		padding: 0;
		margin: 0;

		li {
			height: 5rem;
			flex: 1 0;
			cursor: pointer;
		}
	}

	.home {
		position: absolute;
		top: 0.5rem;
		left: 2rem;
		color: #fff;
	}
</style>
