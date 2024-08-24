<script>
	import '@fortawesome/fontawesome-free/css/all.min.css';
	let languages = [
		{
			name: 'Python',
			description: 'Developed a Discord bot and a script for organizing the download folder.',
			iconClass: 'fab fa-python'
		},
		{
			name: 'Java',
			description: 'School projects in object-oriented programming, including a memory game.',
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
	<div class="text">
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
	* {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}
	#skills {
		background-color: #d0d0d0;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 20px;
		min-height: 100vh;
		width: 100%;
	}

	.text {
		text-align: center;
		margin-bottom: 20px;
		width: 100%;
	}

	h1 {
		font-size: 4em;
		margin: 0;
	}

	.cards-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 30px;
		width: 100%;
		max-width: 1200px;
		margin: 0 auto;
		padding: 0 20px;
		overflow: hidden;
	}

	.card {
		background-color: #ffffff;
		border-radius: 10px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
		width: 100%;
		max-width: 350px;
		padding: 30px;
		text-align: center;
		transition: transform 0.3s ease;
		display: flex;
		flex-direction: column;
		align-items: center;
		flex-shrink: 0;
		margin: 0;
	}

	.card:hover {
		transform: translateY(-5px);
	}

	.card i {
		font-size: 70px;
		margin-bottom: 20px;
		color: #333;
	}

	.card h3 {
		font-size: 1.8em;
		margin: 15px 0;
		color: #333333;
	}

	.card p {
		font-size: 1.1em;
		color: #666666;
		line-height: 1.8;
	}

	@media (max-width: 992px) {
		.cards-container {
			justify-content: center;
			gap: 20px;
		}

		.card {
			flex: 1 1 45%;
			max-width: 100%;
		}
	}

	@media (max-width: 768px) {
		h1 {
			font-size: 2.5rem;
		}

		.card {
			flex: 1 1 80%;
			max-width: 100%;
			margin: 0 auto;
		}
	}

	@media (max-width: 576px) {
		h1 {
			font-size: 2rem;
		}

		.card {
			padding: 20px;
			max-width: 250px;
			margin: 0 auto;
		}

		.card h3 {
			font-size: 1.3rem;
		}

		.card p {
			font-size: 0.9rem;
		}
	}
</style>
