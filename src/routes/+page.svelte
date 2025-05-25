<main>
	<h1>Hello, World!</h1>

	<div class="color-palette">
		<div class="col x-col-1"></div>
		<div class="col x-col-2"></div>
		<div class="col x-col-3"></div>
		<div class="col x-col-4"></div>
		<div class="col x-col-5"></div>
		<div class="col x-col-6"></div>
		<div class="col x-col-7"></div>
		<div class="col x-col-8"></div>
		<div class="col x-col-9"></div>
	</div>
</main>

<style>
	.color-palette {
		display: inline-grid;
		grid-template-columns: repeat(3, 100px);
		grid-template-rows: repeat(3, 100px);

		gap: 10px;
	}

	.col {
		display: inline-block;

		width: 100%;
		height: 100%;
	}

	.x-col-1 {
		background-color: var(--col-primary);
	}

	.x-col-2 {
		background-color: var(--col-secondary);
	}

	.x-col-3 {
		background-color: var(--col-light-accent);
	}

	.x-col-4 {
		background-color: var(--col-accent-2);
	}

	.x-col-5 {
		background-color: var(--col-soft-contrast);
	}

	.x-col-6 {
		background-color: var(--col-alt-purple);
	}

	.x-col-7 {
		background-color: var(--col-deep-violet);
	}

	.x-col-8 {
		background-color: var(--col-cool-blue);
	}

	.x-col-9 {
		background-color: var(--col-core-blue);
	}
</style>
