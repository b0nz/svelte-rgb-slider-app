<script>
	let red = 50;
	let green = 50;
	let blue = 50;

	function fontColor(r, g, b) {
		if (r < 50 || g < 50 || b < 50) {
			return 'color: #ffffff';
		}
		return 'color: #000000';
	}
</script>

<main>
	<div class="card">
		<div class="box" style="background-color: rgb({red}, {green}, {blue}); {fontColor(red, green, blue)}">
			rgb({red}, {green}, {blue})
		</div>
		<div class="slider-container">
			<div>
				<label for="slider-red">Red</label>
				<input type="range" min="0" max="255" bind:value={red} id="slider-red" />
			</div>
			<div>
				<label for="slider-green">Green</label>
				<input type="range" min="0" max="255" bind:value={green} id="slider-green" />
			</div>
			<div>
				<label for="slider-blue">Blue</label>
				<input type="range" min="0" max="255" bind:value={blue} id="slider-blue" />
			</div>
		</div>
	</div>
</main>

<style>
	main {		
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		min-height: 100vh;
	}

	input[type="range"] {
		width: 100%;
	}

	.slider-container {
		margin-top: 20px;
	}

	.box {
		height: 8rem;
		border-radius: 10px;
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 2em;
	}

	.card {
		margin: 0 15px;
		background-color: #ffffff;
		border-radius: 10px;
		width: 40vw;
		padding: 15px;
		box-shadow: 0 20px 50px rgba(0, 0, 0, 0.12);
	}

	label {
		font-size: 14px;
	}

	@media only screen and (max-width: 600px) {
		.card {
			width: 90vw
		}
	}
</style>