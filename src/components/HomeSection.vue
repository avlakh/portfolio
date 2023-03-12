<template>
	<section id="home-section">
		<div class="frame-container">
			<div class="container">
				<div class="home-section-text">
					<h1>Artem Vlakh</h1>
					<h2>Front-end Developer</h2>
					<a href="#about" class="btn">About me</a>
				</div>
				<div class="home-section-img">
					<img
						src="@/assets/images/main-photo.png"
						alt="main photo"
					/>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'HomeSection',
};
</script>

<style lang="scss">
@import '@/assets/css/vars.scss';

#home-section {
	height: 100vh;
	padding: 80px 0 40px;
	.frame-container {
		height: 100%;
		box-shadow: inset 10px 10px 10px #d1d9e6, inset -10px -10px 10px #f9f9f9;
		border-radius: 12px;
		overflow: hidden;
		.container {
			height: 100%;
			display: flex;
			align-items: center;
			justify-content: space-between;
			padding: 25px 0 0;
		}
	}
}

.home-section-text {
	flex-basis: auto;
	h1 {
		background: linear-gradient(to bottom, #2280e4 30%, #0e69c9 70%);
		color: transparent;
		-webkit-background-clip: text;
		margin-bottom: 15px;
	}
	h2 {
		margin-bottom: 32px;
	}
	.btn {
		display: inline-block;
		text-transform: capitalize;
		width: 60%;
		padding: 10px 20px;
		transition: all 0.2s ease;
		border-radius: 12px;
		background: $btn-clr;
		text-align: center;
		font-size: 20px;
		box-shadow: 5px 5px 5px #d1d9e6, -5px -5px 5px #f9f9f9;
		&:hover {
			color: $accent-clr;
		}
		&:active {
			box-shadow: inset 5px 5px 5px #d1d9e6, inset -5px -5px 5px #f9f9f9;
		}
	}
}

.home-section-img {
	flex-basis: 60%;
	border-radius: 12px;
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
}

@media screen and (max-width: 1200px) {
	.home-section-text .btn {
		width: 50%;
	}
}

@media screen and (max-width: 1000px) {
	#home-section {
		height: 100%;
		.frame-container .container {
			justify-content: start;
			flex-direction: column;
			gap: 40px;
		}
	}
	.home-section-text {
		width: 100%;
		text-align: center;
		flex: none;
		h1 {
			font-size: 58px;
			line-height: 62px;
		}
		h2 {
			font-size: 28px;
			line-height: 36px;
		}
	}
}

@media screen and (max-width: 750px) {
	#home-section {
		padding: 80px 0 20px;
	}
}

@media screen and (max-width: 500px) {
	.home-section-text {
		h1 {
			font-size: 42px;
			line-height: 50px;
		}
		h2 {
			font-size: 22px;
			line-height: 30px;
		}
	}
}
</style>
