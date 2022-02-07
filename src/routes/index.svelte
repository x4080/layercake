<script>
	import { LayerCake, Svg } from 'layercake';

	import Line from './layercake/Line.svelte';
	import Area from './layercake/Area.svelte';
	import AxisX from './layercake/AxisX.svelte';
	import AxisY from './layercake/AxisY.svelte';

	const xKey = 'myX';
	const yKey = 'myY';

	let points = [
		{
			myX: 1979,
			myY: 7.19
		},
		{
			myX: 1980,
			myY: 7.73
		},
		{
			myX: 1981,
			myY: 2.73
		},
		{
			myX: 1982,
			myY: 12.73
		}
	];
</script>
<div class="chart-container">
	<LayerCake
		padding={{ right: 10, bottom: 20, left: 25 }}
		x={xKey}
		y={yKey}
		yDomain={[0, null]}
		data={points}
	>
		<Svg>
			<AxisX/>
			<AxisY/>
			<Line/>
			<Area/>
		</Svg>
	</LayerCake>
</div>

<style>
	.chart-container {
		width: 100%;
		height: 100%;
	}
</style>
