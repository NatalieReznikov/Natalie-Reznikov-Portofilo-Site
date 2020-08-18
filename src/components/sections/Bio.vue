<template>
  <div id="Bio">
    <vue-custom-scrollbar class="scroll-area"  :swipeEasing="true" :settings="settings">
      <VueTimeline 
        :timeline-items="timelineItems" 
        :individualClasses="true"
      />
    </vue-custom-scrollbar>
  </div>
</template>

<script>
import VueTimeline from 'bs-vue-timeline'
import vueCustomScrollbar from 'vue-custom-scrollbar'


export default {
  name : "Bio",
  components : {
    VueTimeline,
    vueCustomScrollbar
  },
  data : () => (
    {
      settings: {
        maxScrollbarLength: 60
      },
      timelineItems: [
      {
        from: new Date(2018, 0),
        to: new Date(2020, 0),
        title: 'Object Research Systems Inc., Montreal, QC, Canada',
        subtitle: 'Applications Specialist',
        content: '<em> I designed, assessed and validated novel modules for 3D image analysis for Dragonfly software. I also produced tutorials and educational videos, provided hands-on and online training, troubleshooting and technical support for academic users. </em>',
        image : 'df logo.png'

      },
      {
        from: new Date(2017, 0),
        to: new Date(2018, 0),
        title: 'McGill University, Montreal, QC, Canada',
        subtitle: 'Postdoctoral Research Fellow, Faculty of Dentistry',
        content: '<em> My project aimed at detecting topological differences of the trabecular bone network in pathological bone samples and comparison of the findings with those of normal trabecular bone to assess skeletal adaptation. This work was based on my original algorithm called Inter-Trabecular Angle analysis. My secondary project was 3D analysis of craniofacial deformations in the rare inherited disease Osteogenesis Imperfecta. </em>',
        image : 'mcgill_modified.png'
      },
      {
        from: new Date(2014, 0),
        to: new Date(2017, 0),
        title: 'Imperial College London, London, UK',
        subtitle: 'Postdoctoral Research Fellow, <br> Dept. of Materials, Faculty of Engineering',
        content: '<em> I developed a biomimetic 3D-printed prosthetic material for repair of large defects of trabecular bone. That novel material mimics bone’s natural shock-absorbing properties as normally found in our joints and vertebrae. Other projects included: Functional adaptation of the human foot bones; Multiscale characterization of heterotopic bone; 3D imaging and analysis of the collagen-mineral interface in bone; 3D characterization of bioglass-bone interface; 3D imaging and quantification of DNA-origami drug carriers.</em>',
        image : 'icl.png'
      },
      {
        from: new Date(2010, 0),
        to: new Date(2014, 0),
        title: 'Weizmann Institute of Science, Rehovot, Israel.',
        subtitle: 'PhD, Dept. of Structural Biology',
        content: 'Thesis title: The adaptation of mechanical properties of lamellar bone tissue <br> <em> I studied the 3D organization of bone collagen – the framework principally responsible for toughness – using volumetric imaging obtained from dual-beam microscopy (FIB-SEM), and the topology of trabecular bone tissue imaged by µCT.</em>',
        image : 'Weizmann-Institute-of-Science_logo_modified.png'
      },
      {
        from: new Date(2006, 0),
        to: new Date(2008, 0),
        title: 'Hebrew University of Jerusalem, Jerusalem, Israel.',
        subtitle: 'MSc, Dept. of Orthodontics, Faculty of Dentistry',
        content: 'Thesis title:  Frictional properties of various types of orthodontic brackets <br> <em> This work focused on the mechanics of fixed orthodontic appliances and their surface characterization in simulated pseudo-clinical situations. </em>',
        image : 'hebrew u.png'
      },
    ]
    }
  ),
}
</script>

<style>

:root {
  --bvt-primary-color: #6FEB95;
  --bvt-bg-secondary: #4C8C65;
  --bvt-timeline-color: #ffffff;
  --bvt-timeline-text-color: rgb(255, 255, 255);
  --bvt-border-color: #16191d;
  --bvt-duration-color: var(--bvt-primary-color);
  --bvt-box-shadow1: 0 1px 6px rgba(0, 0, 0, 0.12), 0 1px 4px rgba(0, 0, 0, 0.24);
}

.timeline-content{
  background-color: #282C34 !important;
}

.scroll-area {
  position: relative;
  width: calc(100% - 0px);
  height: calc(100% - 0px);
}
.timeline-nodes:nth-child(odd) h3, .timeline-nodes:nth-child(odd) h2, .timeline-nodes:nth-child(odd) p{
  text-align: center !important;
}
h3.text-light {
    color: #000000 !important;
}

.timeline-image img{
  width: 120px !important;
  height: 120px !important;
  max-height: 120px !important; 
}
.timeline-image::before{
  width: 150px !important;
  height: 150px !important;
}

.timeline-content::after{
  top: 51.818px !important
}

</style>

<style scoped>
#Bio{
  width: 100%;
  height: 100%;
  padding: 50px;
}
</style>