<script lang="ts">
	import '@fortawesome/fontawesome-free/css/all.min.css';
</script>

<center class="hero">
	<div class="container">
		<h1 class="name">Laura Thiel</h1>
		<p class="comment">Aspiring Developer</p>
	</div>
	<div class="scroll-indicator">
		<div class="mouse">
			<div class="wheel"></div>
		</div>
		<div class="arrow"></div>
	</div>
	<div class="icons">
		<button class="icon-button">
			<a href="https://www.reddit.com/user/xcodecat/" target="_blank">
				<i class="fab fa-reddit"></i>
			</a>
		</button>
		<button class="icon-button">
			<a href="https://www.github.com/xcodecat" target="_blank">
				<i class="fa-brands fa-github"></i>
			</a>
		</button>
	</div>
</center>

<style lang="css">
	@import url('https://fonts.googleapis.com/css2?family=Mate:ital@0;1&display=swap');
	
    /* Hero */
    .hero {
		width: 100vw;
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		background-color: (31, 42, 48, 0.5);
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
		backdrop-filter: blur(6.5px);
		-webkit-backdrop-filter: blur(6.5px);
		font-family: 'Mate', serif;
		font-weight: 400;
		font-size: larger;
		text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.7);
		color: #e0e0e0;
		position: relative;
	}

    /* Text */
	.name {
		margin: 0;
	}
	.comment {
		margin: 0;
	}
	.container {
		color: #e0e0e0;
		position: relative;
		height: 100vh;
		width: 100vw;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		/* From https://css.glass */
		background: rgba(31, 42, 48, 0.5);
		box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
		backdrop-filter: blur(6.5px);
		-webkit-backdrop-filter: blur(6.5px);
		font-family: 'Mate', serif;
		font-weight: 400;
		font-style: normal;
		font-size: larger;
		text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.7);
        margin: 0;
	}

    /* Icons */
	.icons {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		position: absolute;
		bottom: 0;
		right: 1vw;
		padding: 5px;
	}
	.icons > * {
		font-size: 24px;
		margin: 0 5px;
	}
	.icon-button {
		color: #e0e0e0;
		background-color: transparent;
		border: none;
		cursor: pointer;
		padding: 10px;
		font-size: 24px;
		margin: 0 0px;
		transition: transform 0.2s;
	}
	.icon-button i.fab.fa-reddit, i.fa-brands.fa-github {
		color: #e0e0e0;
	}
	.icon-button:hover {
		transform: scale(1.1);
	}
	.icon-button:focus {
		outline: none;
	}

    /* Mouse */
	.scroll-indicator {
		position: absolute;
		bottom: 30px;
		left: 50%;
		transform: translateX(-50%);
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.mouse {
		width: 30px;
		height: 50px;
		border: 2px solid #e0e0e0;
		border-radius: 20px;
		position: relative;
	}
	.wheel {
		width: 4px;
		height: 8px;
		background-color: #e0e0e0;
		position: absolute;
		top: 8px;
		left: 50%;
		transform: translateX(-50%);
		border-radius: 2px;
		animation: scroll 1.5s infinite;
	}
	.arrow {
		width: 10px;
		height: 10px;
		border-right: 2px solid #e0e0e0;
		border-bottom: 2px solid #e0e0e0;
		transform: rotate(45deg);
		margin-top: 5px;
		animation: arrow-bounce 1.5s infinite;
	}
	@keyframes scroll {
		0% {
			transform: translate(-50%, 0);
			opacity: 0;
		}
		50% {
			transform: translate(-50%, 10px);
			opacity: 1;
		}
		100% {
			transform: translate(-50%, 20px);
			opacity: 0;
		}
	}
	@keyframes arrow-bounce {
		0%,
		100% {
			transform: translateY(0) rotate(45deg);
		}
		50% {
			transform: translateY(5px) rotate(45deg);
		}
	}

	@media only screen and (max-width: 600px) {
		.scroll-indicator {
			display: none;
		}
	}
</style>
