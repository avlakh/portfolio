<template>
	<section id="about">
		<div class="container">
			<h2>About Me</h2>
			<div class="about-me-flex">
				<Tilt :options="options">
					<div class="about-me-img">
						<img
							src="@/assets/images/secondary-photo.png"
							alt="main photo"
						/>
					</div>
				</Tilt>
				<div class="about-me-text">
					<div class="about-me-descr">
						<h3>Artem Vlakh</h3>
						<h5>
							<span class="bolder-span">Residence:</span>Poland
						</h5>
						<h5><span class="bolder-span">City:</span>Warsaw</h5>
						<h5><span class="bolder-span">Age:</span>26</h5>
						<p>
							Hey &#128075; My name is Artem and I'm a front-end developer passionate. Coming from marketing industry and looking to leverage my web development skills. 
						</p>
						<p>
							An open-minded, result-oriented specialist with
							great time-management skills that strives to learn
							more.
						</p>
						<div class="about-me-skills">
							<span>React</span><span>Redux Toolkit</span><span>Vue</span
							><span>HTML5</span><span>Semantic HTML</span
							><span>CSS3 / SCSS</span><span>Flex / Grid</span
							><span>RWD / AWD</span><span>CSS animation</span
							><span>Cross-browser development</span
							><span>JavaScript ES6+</span><span>Bootstrap5</span><span>Web Storage</span
							><span>jQuery</span><span>Git/Github</span
							><span>APIs</span><span>AJAX</span
							><span>Figma</span><span>npm</span
							><span>Leaflet</span><span>JSON</span
							><span>Vite</span>
						</div>
						<a href="https://drive.google.com/file/d/1qBismOQr37hB9Sfu73YY9QJA9hrzvXXR/view" target="_blank" class="cv-btn"
							><span>Open CV</span
							><i class="icon icon-file_download"></i
						></a>
					</div>
					<h3 class="heading-languages">Languages</h3>
					<div class="about-me-languages">
						<div class="lan">
							<img
								src="@/assets/images/ua-flag.svg"
								alt="UA flag"
							/>
							<h6 class="lan-level">Native</h6>
						</div>
						<div class="lan">
							<img
								src="@/assets/images/pl-flag.svg"
								alt="PL flag"
							/>
							<h6 class="lan-level">Advanced</h6>
						</div>
						<div class="lan">
							<img
								src="@/assets/images/us-flag.svg"
								alt="US flag"
							/>
							<h6 class="lan-level">Advanced</h6>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import Tilt from 'vanilla-tilt-vue';

export default {
	name: 'AboutMe',
	components: {
		Tilt,
	},
	data() {
		return {
			options: {
				max: 10,
				speed: 5000,
				glare: true,
				'max-glare': 0.2,
			},
		};
	},
};
</script>

<style lang="scss">
@import '@/assets/css/vars.scss';

#about {
	scroll-margin-top: 30px;
	padding: 40px 0;
	.container {
		padding: 25px 0;
		h2 {
			margin-bottom: 20px;
		}
	}
}

.about-me-flex {
	display: flex;
	gap: 40px;
}

.about-me-img {
	border-radius: 12px;
	overflow: hidden;
	box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		/* object-position: 43% 0%; */
	}
}
.about-me-text {
	width: 60%;
	h4 {
		margin-bottom: 16px;
		position: relative;
		color: #1a76d2;
		&:before {
			content: '';
			position: absolute;
			bottom: -5px;
			left: 0;
			width: 27%;
			border: 1px solid $secondary-clr;
		}
	}
	p {
		padding-right: 20%;
		margin-bottom: 10px;
		&:last-of-type {
			margin-bottom: 30px;
		}
	}
	h5 {
		font-size: 18px;
		line-height: 22px;
		margin-bottom: 8px;
		font-weight: 400;
		&:last-of-type {
			margin-bottom: 30px;
		}
	}
}

.bolder-span {
	font-weight: 700;
	margin-right: 8px;
}

.about-me-skills {
	display: flex;
	flex-wrap: wrap;
	gap: 20px;
	margin-bottom: 20px;
	pointer-events: none;
	span {
		padding: 5px 20px;
		border-radius: 12px;
		background-color: #e8ebf0;
		box-shadow: 5px 5px 5px #d1d9e6, -5px -5px 5px #f9f9f9;
		color: $accent-clr;
		transition: all 0.2s ease;
	}
}

.cv-btn {
	display: block;
	padding: 10px 50px;
	background-color: #e8ebf0;
	border-radius: 12px;
	width: 40%;
	box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
	text-align: center;
	color: inherit;
	margin-bottom: 30px;
	&:hover {
		color: $accent-clr;
	}
	&:active {
		box-shadow: inset 5px 5px 5px #d1d9e6, inset -5px -5px 5px #f9f9f9;
	}
	span:first-of-type {
		margin-right: 10px;
	}
	i {
		font-size: 20px;
		position: relative;
		&:before {
			position: absolute;
			top: 3px;
		}
	}
}

.heading-languages {
	margin-bottom: 20px;
}

.about-me-languages {
	display: flex;
	gap: 40px;
	justify-content: flex-start;
	.lan {
		width: 33%;
		border-radius: 12px;
		box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 30px;
		transition: all 0.2s ease;
		padding: 20px 10px;
		will-change: transform;
		.lan-level {
			font-weight: 500;
			font-size: 20px;
			cursor: default;
		}
		img {
			height: 30px;
			width: 65px;
			object-fit: cover;
		}
		&:hover {
			transform: scale(1.1);
			border-radius: 12px;
		}
	}
}

@media screen and (max-width: 1200px) {
	.about-me-flex {
		align-items: flex-start;
		#tiltMe {
			width: 60%;
			height: 60%;
		}
	}
	.about-me-text {
		width: 100%;
	}
}

@media screen and (max-width: 1100px) {
	.about-me-flex {
		flex-direction: column;
		align-items: center;
		#tiltMe {
			width: 60%;
		}
	}
	.about-me-text p {
		padding-right: 0;
	}
	.about-me-languages {
		flex-wrap: wrap;
		.lan {
			width: 30%;
		}
	}
}

@media screen and (max-width: 900px) {
	.about-me-languages .lan {
		width: 45%;
	}
}

@media screen and (max-width: 750px) {
	#about {
		padding: 20px 0;
	}
}

@media screen and (max-width: 700px) {
	.about-me-flex #tiltMe {
		width: 100%;
	}
}

@media screen and (max-width: 600px) {
	.about-me-skills {
		align-items: center;
		justify-content: center;
		margin-bottom: 30px;
	}
	.cv-btn {
		width: 100%;
		padding: 25px 25px;
	}
	.about-me-languages {
		gap: 20px;
		.lan {
			width: 100%;
		}
	}
}
</style>
