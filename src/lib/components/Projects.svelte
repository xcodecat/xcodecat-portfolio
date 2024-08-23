<script>
	import '@fortawesome/fontawesome-free/css/all.min.css';
	let projects = [
		{
			name: 'Memory Game',
			description: 'A two player Memory Game written in Java',
			technologies: ['Java', 'JavaFX'],
			iconClass: 'fas fa-gamepad',
			link: 'https://github.com/xcodecat/memory-game'
		},
		{
			name: 'Automate Download Delete',
			description: 'Script for Automating Downloads Folder Cleanup',
			technologies: ['Python'],
			iconClass: 'fa-solid fa-trash',
			link: 'https://github.com/xcodecat/automate-download-delete'
		},
		{
			name: 'bapp - Bunkerpost digital',
			description: 'The digital school newspaper of HSG Erlenbach (for students only)',
			technologies: ['VueJS', 'JavaScript', 'HTML & CSS', 'MariaDB'],
			iconClass: 'fa-solid fa-newspaper',
			link: 'https://bapp.hsgerlenbach.de'
		},
		{
			name: 'Problems',
			description: 'A repository where I solve problems in multiple languages',
			technologies: ['Kotlin'],
			iconClass: 'fa-solid fa-circle-xmark',
			link: 'https://github.com/xcodecat/problems'
		},
		{
			name: 'Alle Meine Entchen',
			description: 'The german children song "Alle Meine Entchen" on an Arduino Board using a Piezo ELement',
			technologies: ['Elements of C & C++'],
			iconClass: 'fa-solid fa-music',
			link: 'https://github.com/xcodecat/alleMeineEntchen'
		}
	];
</script>

<section id="projects">
	<div id="text">
		<h1>Projects</h1>
	</div>
	<div class="projects-container">
		{#each projects as project}
			<div class="project-card">
				<i class={project.iconClass}></i>
				<h3>{project.name}</h3>
				<p>{project.description}</p>
				<ul>
					{#each project.technologies as tech}
						<li>{tech}</li>
					{/each}
				</ul>
				<a href={project.link} target="_blank">View Project</a>
			</div>
		{/each}
	</div>
</section>

<style lang="css">
	#projects {
		background-color: #b3b3b3;
		padding: 20px;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		min-height: 100vh;
		text-align: center;
	}

	#text {
		margin-bottom: 20px;
	}

	h1 {
		font-size: 4em;
		margin: 0;
		color: #333;
	}

	.projects-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 20px;
		max-width: 1200px;
		margin: 0 auto;
	}

	.project-card {
		background-color: #ffffff;
		border-radius: 10px;
		box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
		width: 300px;
		padding: 20px;
		text-align: center;
		transition: transform 0.3s ease;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: space-between;
	}

	.project-card:hover {
		transform: translateY(-5px);
	}

	.project-card i {
		font-size: 60px;
		margin-bottom: 15px;
		color: #333;
	}

	.project-card h3 {
		font-size: 1.5em;
		margin: 10px 0;
		color: #333;
	}

	.project-card p {
		font-size: 1em;
		color: #666;
		line-height: 1.6;
		margin-bottom: 15px;
	}

	.project-card ul {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.project-card li {
		background-color: #e0e0e0;
		border-radius: 5px;
		padding: 5px 10px;
		margin: 5px 5px;
		display: inline-block;
	}

	.project-card a {
		color: #007bff;
		text-decoration: none;
		font-weight: bold;
		margin-top: auto;	
	}

	.project-card a:hover {
		text-decoration: underline;
	}

	@media (max-width: 768px) {
		.project-card {
			width: 90%;
		}

		h1 {
			font-size: 2em;
		}
	}

	@media (max-width: 480px) {
		.project-card {
			width: 100%;
		}

		h1 {
			font-size: 1.5em;
		}
	}
</style>
