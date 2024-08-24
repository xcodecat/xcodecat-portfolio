<script>
	import '@fortawesome/fontawesome-free/css/all.min.css';
	
	let projects = [
		{
			name: 'Memory Game',
			description: 'A two-player memory game written in Java, featuring Disney character images.',
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
			description: 'A repository featuring solutions to problems across various programming languages.',
			technologies: ['Kotlin'],
			iconClass: 'fa-solid fa-circle-xmark',
			link: 'https://github.com/xcodecat/problems'
		},
		{
			name: 'Alle Meine Entchen',
			description: "A rendition of the German children's song 'Alle Meine Entchen' played on an Arduino board using a piezo element.",
			technologies: ['C', 'C++', 'Arduino'],
			iconClass: 'fa-solid fa-music',
			link: 'https://github.com/xcodecat/alleMeineEntchen'
		}
	];
</script>

<section id="projects">
	<div class="text">
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
				<a href={project.link} target="_blank" rel="noopener noreferrer">View Project</a>
			</div>
		{/each}
	</div>
</section>

<style>
	/* General Reset */
	* {
		box-sizing: border-box;
		margin: 0;
		padding: 0;
	}

	/* Section Styling */
	#projects {
		background-color: #f5f5f5;
		padding: 60px 20px;
		display: flex;
		flex-direction: column;
		align-items: center;
		min-height: 100vh;
	}

	.text {
		margin-bottom: 40px;
		text-align: center;
	}

	h1 {
		font-size: 3rem;
		color: #333;
	}

	/* Projects Container */
	.projects-container {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 30px;
		width: 100%;
		max-width: 1200px;
	}

	/* Project Card Styling */
	.project-card {
		background-color: #ffffff;
		border-radius: 10px;
		box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
		padding: 30px;
		flex: 1 1 300px; /* Flexible basis with min width of 300px */
		max-width: 350px;
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		transition: transform 0.3s ease, box-shadow 0.3s ease;
	}

	.project-card:hover {
		transform: translateY(-10px);
		box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
	}

	.project-card i {
		font-size: 3rem;
		margin-bottom: 20px;
		/* Beibehalten der ursprünglichen Farbe */
		color: inherit;
	}

	.project-card h3 {
		font-size: 1.5rem;
		color: #333;
		margin-bottom: 15px;
	}

	.project-card p {
		font-size: 1rem;
		color: #555;
		margin-bottom: 20px;
		line-height: 1.5;
	}

	.project-card ul {
		list-style: none;
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		gap: 10px;
		margin-bottom: 20px;
	}

	.project-card li {
		background-color: #e9ecef;
		color: #333;
		border-radius: 20px;
		padding: 5px 15px;
		font-size: 0.9rem;
	}

	.project-card a {
		color: #ffffff;
		background-color: #3498DB;
		padding: 10px 20px;
		border-radius: 5px;
		text-decoration: none;
		font-weight: 500;
		transition: background-color 0.3s ease;
		margin-top: auto;
	}

	.project-card a:hover {
		background-color: #0056b3;
	}

	/* Responsive Design */
	@media (max-width: 992px) {
		.projects-container {
			gap: 20px;
		}

		.project-card {
			flex: 1 1 45%;
			max-width: 100%;
		}
	}

	@media (max-width: 768px) {
		h1 {
			font-size: 2.5rem;
		}

		.project-card {
			flex: 1 1 100%;
		}
	}

	@media (max-width: 576px) {
		h1 {
			font-size: 2rem;
		}

		.project-card {
			padding: 20px;
		}

		.project-card h3 {
			font-size: 1.3rem;
		}

		.project-card p {
			font-size: 0.9rem;
		}

		.project-card li {
			font-size: 0.8rem;
			padding: 4px 10px;
		}

		.project-card a {
			padding: 8px 16px;
			font-size: 0.9rem;
		}
	}
</style>
