<script>
	import FeaturesIcon from '$lib/icons/features.svelte';
	import BlogIcon from '$lib/icons/blog.svelte';
	import ExperienceIcon from '$lib/icons/experience.svelte';
	import ProjectsIcon from '$lib/icons/projects.svelte';
	import GitHubIcon from '$lib/icons/socials/github.svelte';
	import Button from '$lib/components/atoms/Button.svelte';
	import Sparkles from '../atoms/Sparkles.svelte';
</script>

<section id="hero">
	<h1 class="hello">Hey, I'm Brian</h1>
	<p class="intro">
		<span class="left">I learn and write about exponentials</span>
		<span class="right">Let's ride 🌊</span>
	</p>
	<div class="ctas">
		<Sparkles>
			<Button href="#">
				<ProjectsIcon slot="icon" />
				Projects (W.I.P.)
			</Button>
		</Sparkles>
		<!-- <Button color="primary" href="https://histoire-sveltekit-static-blog-template.vercel.app/">
			<FeaturesIcon slot="icon" />
			Components
		</Button> -->
		<Button color="secondary" href="/blog">
			<BlogIcon slot="icon" />
			Blog
		</Button>
		<Button color="primary" href="">
			<ExperienceIcon slot="icon" />
			Experience
		</Button>
	</div>
</section>

<style lang="scss">
	@import '$lib/scss/breakpoints.scss';

	#hero {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 15px;
		position: relative;
		padding: 80px 0;

		@include for-phone-only {
			padding: 40px 0 50px;
		}

		.hello {
			text-align: center;
		}

		.intro {
			font-weight: 500;
			font-size: 1.4rem;
			width: min(100%, 440px);
			display: flex;
			flex-direction: column;

			.left {
				text-align: left;
			}
			.right {
				text-align: right;
			}

			@include for-phone-only {
				display: none;
			}
		}

		.ctas {
			display: flex;
			flex-wrap: wrap;
			align-items: center;
			justify-content: center;
			gap: 10px;
			width: 100%;
		}
	}
</style>
