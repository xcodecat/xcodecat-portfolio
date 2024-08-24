<section id="about">
	<div class="text">
		<h1>About Me</h1>
		<p>
			I'm a <b>17-year-old student and beginner</b> in <b>web development</b>, passionate about
			turning ideas into reality through <b>code</b>.<br />
			Although I'm still learning, I've already gained the skills to create <b>engaging</b>,
			<b>functional <b>websites</b></b> and I’m eager to keep improving.<br />
			I'm also exploring the world of <b>IoT</b>, where <b>technology</b> enhances everyday life.<br
			/><br />
			Beyond coding, I express my <b>creativity</b> through <b>guitar playing</b>.<br />
			In my free time, I enjoy the <b>outdoors</b>, finding inspiration in <b>nature</b>.<br /><br
			/>
			I'm excited to continue growing, blending <b>technology</b> and <b>creativity</b> as I learn more
			every day.
		</p>
	</div>
</section>

<style>
	#about {
		background-color: #eaeded;
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	.text {
		width: 50vw;
	}

	h1 {
		font-size: 4em;
		margin: 0;
	}

	p {
		font-size: 1.5em;
		margin: 0;
	}

	b {
		position: relative;
		font-weight: bold;
	}

	b::after {
		content: '';
		position: absolute;
		left: 0;
		bottom: -2px;
		width: 100%;
		height: 2px;
		background-color: #bdc3c7;
		transform: scaleX(0);
		transform-origin: bottom right;
		transition: transform 0.3s ease;
	}

	b:hover::after {
		transform: scaleX(1);
		transform-origin: bottom left;
	}

	b:hover {
		color: #bdc3c7;
	}

	@media only screen and (max-width: 600px) {
		.text {
			width: 75vw;
		}
	}
</style>
