<script>
	import '@fortawesome/fontawesome-free/css/all.min.css';
	let languages = [
		{
			name: 'Python',
			description:
				'Developed a Discord bot and a script for organizing the download folder.',
			iconClass: 'fab fa-python'
		},
		{
			name: 'Java',
			description:
				'School projects in object-oriented programming, including a memory game.',
			iconClass: 'fab fa-java'
		},
		{
			name: 'JavaScript',
			description:
				'Experience in web development and school projects, including a school newspaper.',
			iconClass: 'fab fa-js'
		},
		{
			name: 'Kotlin/Flutter',
			description:
				'Basic knowledge of Android development, with an interest in mobile applications.',
			iconClass: 'fa-brands fa-android'
		},
		{
			name: 'Go',
			description:
				'Exploratory learning, with an interest in systems programming and new technologies.',
			iconClass: 'fa-brands fa-golang'
		}
	];
</script>

<section id="skills">
	<div id="text">
		<h1>Skills</h1>
	</div>
	<div class="cards-container">
		{#each languages as language}
			<div class="card">
				<i class={language.iconClass}></i>
				<h3>{language.name}</h3>
				<p>{language.description}</p>
			</div>
		{/each}
	</div>
</section>

<style>
	#skills {
		background-color: #d0d0d0;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 20px;
		min-height: 100vh;
	}

	#text {
		text-align: center;
		margin-bottom: 20px;
	}

	h1 {
		font-size: 4em;
		margin: 0;
	}

	.cards-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 20px;
		max-width: 1200px;
	}

	.card {
		background-color: #ffffff;
		border-radius: 10px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
		width: 250px;
		padding: 20px;
		text-align: center;
		transition: transform 0.3s ease;
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.card:hover {
		transform: translateY(-5px);
	}

	.card i {
		font-size: 60px;
		margin-bottom: 15px;
		color: #333;
	}

	.card h3 {
		font-size: 1.5em;
		margin: 10px 0;
		color: #333333;
	}

	.card p {
		font-size: 1em;
		color: #666666;
		line-height: 1.6;
	}
</style>
