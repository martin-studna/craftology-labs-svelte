<script>
	import { Landing, Services, About, Experience, CaseStudies, Contacts } from '$lib';
	import Saos from "saos";
</script>


<Landing />
<Services />
<About />
<Experience />
<CaseStudies />
<Contacts />

<style>
	@keyframes -global-slide-in-top {
    0% {
      transform: translateY(-50px);
      opacity: 0;
    }
    100% {
      transform: translateY(0);
      opacity: 1;
    }
  }
</style>
