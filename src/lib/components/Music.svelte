<script lang="ts">
	import '@fortawesome/fontawesome-free/css/all.min.css';

	let music = [
		{
			name: 'Study',
			link: `<iframe style="border-radius:12px"
				src="https://open.spotify.com/embed/playlist/7hUx85faD36UvhULacNEJd?utm_source=generator&theme=0"
				width="100%" height="352" frameBorder="0" allowfullscreen=""
				allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
				loading="lazy"></iframe>`,
			iconClass: 'fa-solid fa-graduation-cap'
		},
		{
			name: 'Daily',
			link: `<iframe style="border-radius:12px" src="https://open.spotify.com/embed/playlist/1d9gre8DSEYEjHeWcAslOq?utm_source=generator&theme=0" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>`,
			iconClass: 'fa-solid fa-music'
		},
		{
			name: 'Code',
			link: `<iframe style="border-radius:12px"
				src="https://open.spotify.com/embed/playlist/2NGqBaEid5GuCwD0XdEhOh?utm_source=generator&theme=0"
				width="100%" height="352" frameBorder="0" allowfullscreen=""
				allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
				loading="lazy"></iframe>`,
			iconClass: 'fa-solid fa-code'
		}
	];
</script>

<section id="music">
	<div class="section-header">
		<h1>My Playlists</h1>
		<p>Hand-picked soundtracks for every mood and focus.</p>
	</div>

	<div class="music-grid">
		{#each music as music}
			<div class="music-card">
				<div class="icon-label">
					<i class={music.iconClass}></i>
					<h3>{music.name}</h3>
				</div>
				<div class="iframe-wrapper">
					{@html music.link}
				</div>
			</div>
		{/each}
	</div>
</section>

<style>
	* {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}

	#music {
		background-color: #f4f4f5;
		padding: 60px 20px;
		width: 100%;
	}

	.section-header {
		text-align: left;
		max-width: 1200px;
		margin: 0 auto 40px auto;
		padding: 0 20px;
	}

	.section-header h1 {
		font-size: 3rem;
		margin-bottom: 10px;
		color: #111827;
	}

	.section-header p {
		color: #4b5563;
		font-size: 1.2rem;
	}

	.music-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 30px;
		max-width: 1200px;
		margin: 0 auto;
		padding: 0 20px;
	}

	.music-card {
		background-color: white;
		border: 1px solid #e5e7eb;
		border-radius: 16px;
		box-shadow: 0 8px 16px rgba(0, 0, 0, 0.05);
		padding: 20px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		transition:
			transform 0.3s ease,
			box-shadow 0.3s ease;
	}

	.music-card:hover {
		transform: translateY(-5px);
		box-shadow: 0 12px 20px rgba(0, 0, 0, 0.08);
	}

	.icon-label {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin-bottom: 16px;
	}

	.icon-label i {
		font-size: 48px;
		color: #4b5563;
		margin-bottom: 10px;
	}

	.icon-label h3 {
		font-size: 1.5rem;
		color: #111827;
		margin: 0;
	}
</style>
