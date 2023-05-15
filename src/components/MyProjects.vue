<template>
	<section id="projects">
		<div class="container">
			<h2>Projects</h2>
			<div class="projects-grid">
				<div
					class="projects-grid-item"
					v-for="item in projects"
					:key="item"
				>
					<div class="img-wrap">
						<img
							:src="
								require('@/assets/images/projects/' + item.img)
							"
							:alt="item.imgAlt"
						/>
					</div>
					<div class="content-overlay">
						<div class="content-overlay-links">
							<a :href="item.githubUrl" target="_blank"
								>See source code</a
							>
							<a :href="item.url">See project</a>
						</div>
						<p>{{ item.descr }}</p>
					</div>
					<a class="content-interactive-overlay" :href="item.url"></a>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
import axios from 'axios';

export default {
	name: 'MyProjects',
	data() {
		return {
			projects: [],
		};
	},
	created() {
		axios.get('data/MyProjects.json').then((resp) => {
			this.projects = resp.data;
		});
	},
};
</script>

<style lang="scss" scoped>
@import '@/assets/css/vars.scss';

#projects {
	padding: 40px 0;
	scroll-margin-top: 30px;
	h2 {
		margin-bottom: 40px;
	}
}

.projects-grid {
	width: 100%;
	height: 100%;
	display: grid;
	grid-template: repeat(auto-fit, minmax(150px, 1fr)) / repeat(
			auto-fit,
			minmax(300px, 1fr)
		);
	gap: 3rem;
}

.projects-grid-item {
	position: relative;
	border: 10px solid $secondary-clr;
	height: 100%;
	width: 100%;
	border-radius: 12px;
	box-shadow: 10px 10px 10px #d1d9e6, -10px -10px 10px #f9f9f9;
	transition: all 0.2s ease;
	overflow: hidden;
	&:hover {
		transform: scale(1.1);
	}
	&:hover .content-overlay {
		bottom: 0%;
	}
	&:hover .content-interactive-overlay {
		bottom: 0%;
	}
}

.content-overlay {
	position: absolute;
	bottom: -100%;
	left: 0;
	height: 100%;
	width: 100%;
	padding: 2rem;
	transition: all 0.2s ease;
	background-color: rgb(233, 241, 251, 1);
	display: flex;
	justify-content: center;
	align-items: center;
	flex-direction: column;
	p {
		text-align: center;
	}
}

.content-overlay-links > a {
	position: relative;
	display: block;
	text-align: center;
	padding: 5px 15px;
	margin-bottom: 1rem;
	transition: all 0.2s ease;
	border-radius: 12px;
	background: $btn-clr;
	box-shadow: 2px 2px 2px #d1d9e6, -2px -2px 2px #f9f9f9;
	z-index: 120;
	&:hover {
		color: $accent-clr;
		&:active {
			box-shadow: inset 5px 5px 5px #d1d9e6, inset -5px -5px 5px #f9f9f9;
		}
	}
}

.content-interactive-overlay {
	position: absolute;
	height: 100%;
	width: 100%;
	z-index: 100;
}

.img-wrap {
	width: 100%;
	height: 100%;
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
}

@media screen and (min-width: 700px) {
	.projects-grid {
		grid-template: repeat(auto-fit, minmax(300px, 1fr)) / repeat(
				auto-fit,
				minmax(450px, 1fr)
			);
	}
}

@media screen and (max-width: 750px) {
	#projects {
		padding: 20px 0;
	}
}

@media screen and (max-width: 500px) {
	.content-overlay {
		display: none;
	}
}
</style>
