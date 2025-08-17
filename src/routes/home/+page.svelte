<script lang="ts">
	import type { LanEvent } from '$lib/types/lanEvent';

	const currentEvents: LanEvent[] = [];
	const pastEvents: LanEvent[] = [];

	currentEvents.push({
		title: 'Nintendo Lan',
		time: new Date('2025-09-01'),
		location: 'koeln',
		players: 2
	});

	currentEvents.push({
		title: 'Mariokart Lan',
		time: new Date('2025-10-01'),
		location: 'berlin',
		players: 3
	});

	pastEvents.push({
		title: 'Retro Lan',
		time: new Date('2025-06-01'),
		location: 'london',
		players: 323
	});

	pastEvents.push({
		title: 'Minecraft Lan',
		time: new Date('2025-03-01'),
		location: 'paris',
		players: 12
	});

	pastEvents.push({
		title: 'Grosse Lan',
		time: new Date('2024-09-01'),
		location: 'amsterdam',
		players: 43
	});
</script>

<main>
	<div class="upcoming list">
		<h1>Upcoming Events</h1>

		<div class="event-list">
			{#each currentEvents as event}
				<div class="curronet-event event">
					<h2>{event.title}</h2>
					<div class="event-content">
						<p>When?</p>
						<p>{event.time}</p>
						<p>Where?</p>
						<p>{event.location}</p>
						<p>Player Count?</p>
						<p>{event.players}</p>
					</div>
				</div>
			{/each}
		</div>
	</div>
	<div class="past list">
		<h1>Past Events</h1>

		<div class="event-list">
			{#each pastEvents as event}
				<div class="past-event event">
					<h2>{event.title}</h2>
				</div>
			{/each}
		</div>
	</div>
</main>

<style>
	h1 {
		font-size: 2rem;
		margin: 0;
		padding: 0;
	}

	h2 {
		font-size: 1.5rem;
		margin: 0;
		padding: 0;
	}

	main {
		display: flex;
		flex-direction: column;
		gap: 3rem;

		width: 100%;

		align-items: center;
	}

	.list {
		width: 50%;
	}

	.event-list {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.event {
		background-color: whitesmoke;
		padding: 1rem;
		border-style: solid;
		border-color: black;
		border-width: 1px;
		border-radius: 1rem;

		width: 100%;
	}

	.event-content {
		border-top-style: solid;
		border-top-color: black;
		border-top-width: 1px;

		margin-top: 0.5rem;
		padding-top: 0.5rem;
	}
</style>
