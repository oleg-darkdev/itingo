<script>
    import { Button } from 'flowbite-svelte';
	import WorkList from '../../../components/landing/ngo/WorkList.svelte';

	export let typeWork, btnLink;
</script>

<section id={typeWork.anchor} style="background-position: {typeWork.align == 'start' ? 'right': 'left'};" class="{typeWork.bgImage} work-wrap justify-{typeWork.align} content-center " >
	<div data-aos="fade-down"
		data-aos-delay="80"
		data-aos-duration="800" 
		data-aos-once="false"
		data-aos-mirror="true"  style="" class="lg:w-7/12 md:w-12/12 bg-white flex justify-end items-center">
		<div 
		style="min-width: 320px;" class="pt-8 pb-8 pr-2 pl-2 flex flex-col items-center ">
			<h3 class=" m-8 text-5xl lg:text-6xl md:text-6xl   text-lightYellow font-bold">{typeWork.title}</h3>
			  <p class="font-normal lg:w-8/12 md:w-8/12 w-11/12 text-start leading-tight mb-2 text-viol">
  				{typeWork.description}
			</p>
			<WorkList dataAboutService={typeWork.dataAboutService}/>
			<Button href={btnLink} size="xl" class="lg:w-4/12" color="purple">Zgłosić projekt</Button>
		</div>
	</div>
</section>


<style>
	
	.work-wrap {
		
		height: auto;
		background-repeat: no-repeat;		
		background-size: auto;
		background-attachment: fixed;
	}
	@media (min-width: 1024px) {
		.work-wrap {
			min-height: 100vh;
		}
		.computers-bg {
		 background-image: url(/images/ngo/type_works_bg/computers-bg.svg);
	}
	/* benefits */
	.technology-bg {
		background-image: url(/images/volunteer/benefits/technology-bg.svg);
	}
	.progress-bg {
		background-image: url(/images/volunteer/benefits/progress-bg.svg);
	}
	.begginers_help-bg {
		background-image: url(/images/volunteer/benefits/begginers_help-bg.svg);
	}
	.flexible_schedule-bg {
		background-image: url(/images/volunteer/benefits/flexible_schedule-bg.svg);
	}
	.mentoring-bg {
		background-image: url(/images/volunteer/benefits/mentoring-bg.svg);
	}
	.technology-bg {
		background-image: url(/images/volunteer/benefits/technology-bg.svg);
	}
	.reccomandation_letter-bg {
		background-image: url(/images/volunteer/benefits/reccomandation_letter-bg.svg);
	}





	/* types works */
	.design-bg {
		background-image: url(/images/ngo/type_works_bg/design-bg.svg);
	}
	.projecting-bg {
		background-image: url(/images/ngo/type_works_bg/projecting-bg.svg);
	}
	.security-bg {
		background-image: url(/images/ngo/type_works_bg/security-bg.svg);
	}
	.seo-bg {
		background-image: url(/images/ngo/type_works_bg/seo-bg.svg);
	}
	.server-bg {
		background-image: url(/images/ngo/type_works_bg/server-bg.svg);
	}
	.site-bg {
		background-image: url(/images/ngo/type_works_bg/site-bg.svg);
	}
	.social-bg {
		background-image: url(/images/ngo/type_works_bg/social-bg.svg);
	}
	.video-bg {
		background-image: url(/images/ngo/type_works_bg/video-bg.svg);
	}
	}
	@media (min-device-width: 320px) and (max-device-width: 1024px) {
		.work-wrap {
			min-height: 60vh;
			height: auto;
		}
		.computers-bg, .design-bg, .projecting-bg, .security-bg, .seo-bg, .server-bg, .site-bg, .social-bg, .video-bg {
			background-color: #4A148C;
		}

	}
</style>