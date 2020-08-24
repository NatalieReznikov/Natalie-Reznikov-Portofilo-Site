<template>
  <div id="Publications">
    <div class="TextBox">
      <vuescroll>
        <template v-for="pub in pubs">
            {{pub.id+1}}. {{pub.authors}} <br :key="pub.id*7">
            <em :key="pub.id*7+1"> {{pub.title}} </em> <br :key="pub.id*7+2">
            {{pub.prelink}} <a v-if="pub.link" :href="pub.link" :key="pub.id*7+4"> {{pub.link}} </a> {{pub.postlink}} 
            <br :key="pub.id*7+5">
            <br :key="pub.id*7+6">
        </template>
      </vuescroll>
    </div>
  </div>
</template>

<script>
import vuescroll from "vuescroll/dist/vuescroll-native";

export default {
  name: "Publications",
  components: {
    vuescroll,
  },
  data: () => {
    return {
      ops: {
        vuescroll: { detectResize: false },
        scrollPanel: {},
        rail: {},
        bar: {},
      },
      pubs: [
        {
          id: 0,
          authors: "Reznikov N, Buss DJ, Provencher B, McKee MD, Piché N.",
          title: "Deep learning and 3D imaging in structural biology. Review",
          prelink:"J Struct Biol, 2020: 107598 (invited from conference selection, special issue) ",
          link:"https://doi.org/10.1016/j.jsb.2020.107598",
          postlink:"",
        },
        {
          id: 1,
          authors: "Buss DJ, Reznikov N, McKee MD.",
          title:"Crossfibrillar mineral tessellation in normal and Hyp mouse bone as revealed by 3D FIB-SEM microscopy",
          prelink:"J Struct Biol, 2020: 107603 ",
          link:"https://doi.org/10.1016/j.jsb.2020.107603",
          postlink:"",
        },
        {
          id: 2,
          authors:"Reznikov N, Hoac B, Buss DJ, Addison WN, Barros NMT, McKee MD.",
          title:"Biological stenciling of mineralization in the skeleton:  Local enzymatic removal of inhibitors in the extracellular matrix.",
          prelink:"Bone, 2020 ",
          link:"https://doi.org/10.1016/j.bone.2020.115447",
          postlink:"   (cover article)",
        },
        {
          id: 3,
          authors:"Athanasiadou D, Jiang W, Reznikov N, Rodriguez-Navarro AB, Kroeger R, Bilton M, Nelea V, Hu Y, McKee MD.",
          title: "Nanostructure of mouse otoconia",
          prelink:"J Struct Biol, 2020, 210(2):107489. ",
          link:"https://doi.org/10.1016/j.jsb.2020.107489",
          postlink:"",
        },
        {
          id: 4,
          authors: "Reznikov N, Rechav K.",
          title:"FIB-SEM dual-beam microscopy for three-dimensional ultrastructural imaging of skeletal tissues. Methodological insert in Comparative skeletal histology and paleohistology. Editors : A. de Ricqlès, L. Zylberberg, K. Padian and V. de Buffrénil",
          prelink:"CRC Press (Francis and Taylor Group) (invited book chapter, in press).",
          postlink:"",
        },
        {
          id: 5,
          authors:"Reznikov N, Alsheghri A, Piche N, Gendron M, Morozova I, Sanchez Siles JM, Gonzalez-Quevedo D, Tamimi Marino I, Song J, Tamimi Marino F.",
          title:"The topological blueprint of trabecular bone associates with skeletal pathology in humans",
          prelink:"Bone Reports, 2020 12:100264. ",
          link:"https://doi.org/10.1016/j.bonr.2020.100264",
          postlink:"",
        },
        {
          id: 6,
          authors:"Reznikov N, Dagdeviren D, Tamimi Marino F, Glorieux F, Rauch F, Retrouvey JM.",
          title:"Cone-beam computed tomography of Osteogenesis Imperfecta types III and IV: Three-dimensional evaluation of craniofacial features and upper airways",
          prelink:"J Bone Miner Res Plus, 2019, 3(6): ",
          link:"https://doi.org/10.1002/jbm4.10124",
          postlink:"",
        },
        {
          id: 7,
          authors:"Autefage H,  Allen F, Tang HM, Kallepitis C, Gentleman E, Reznikov N,  Nitiputri K, Nommeots-Nomm A, O’Donnell MD,  Lange C, Seidt BM, Kim TB, Lee PD, Pierce BF, Wagermaier W, Fratzl P, Goodship A, Jones JR, Blunn G, Stevens MM.",
          title:"Multiscale analyses reveal native-like lamellar bone repair and near perfect bone-contact with porous strontium-loaded bioactive glass.",
          prelink:"Biomaterials, 2019, 209:152-162. ",
          link:"https://doi.org/10.1016/j.biomaterials.2019.03.035",
          postlink:"",
        },
        {
          id: 8,
          authors:"Ghouse S, Reznikov N, Boughton O, Babu S, Ng G, Blunn G, Cobb J, Stevens MM, Jeffers J.",
          title:"The design and in vivo testing of a locally stiffness-matched porous scaffold",
          prelink:"Applied Materials Today, 2019, 15:377-388. ",
          link:"https://doi.org/10.1016/j.apmt.2019.02.017",
          postlink:"",
        },
        {
          id: 9,
          authors:"Reznikov N, Boughton O, Ghouse S, Blunn G, Weston A, Collinson L, Jeffers J, Cobb J, Stevens M.",
          title:"Individual response variations in scaffold-guided bone regeneration are determined by independent strain- and injury-induced mechanisms",
          prelink:"Biomaterials, 2019, 194: 183-194. ",
          link:"https://doi.org/10.1016/j.biomaterials.2018.11.026",
          postlink:"",
        },
        {
          id: 10,
          authors: "Reznikov N, Bilton M, Lari L, Stevens MM, Kroeger R.",
          title:"Fractal-like hierarchical organization of bone begins at the atomic level",
          prelink:"Science, 2018, 360: eaao2189.  ",
          link:"https://doi.org/10.1126/science.aao2189.",
          postlink:"",
        },
        {
          id: 11,
          authors:"Silvent J, Akiva A, Brumfeld V, Reznikov N, Rechav K, Yaniv K, Addadi L, Weiner S.",
          title:"Embryogenic zebrafish skeleton development: high resolution micro-CT imaging for phenotype identification",
          prelink:"PLoS ONE, 2017; 12(12): e0177731 ",
          link:"https://doi.org/10.1371/journal.pone.0177731",
          postlink:"",
        },
        {
          id: 12,
          authors: "Rowan S, Chang M-L, Reznikov N, Taylor A.",
          title:"Disassembly of the lens fiber cell nucleus to create a clear lens: The p27 descent",
          prelink:"Exper Eye Res, 2017; 156:72-78. ",
          link:"https://doi.org/10.1016/j.exer.2016.02.011",
          postlink:"",
        },
        {
          id: 13,
          authors: "Ben-Zvi Y*, Reznikov N*, Shahar R, Weiner S.",
          title:"3D architecture of trabecular bone in the pig mandible and femur: Inter-trabecular angle distributions",
          prelink:"Front Mater (Special Issue: Computed Tomography-Based Biomaterials), 2017 ",
          link:"https://doi.org/10.3389/fmats.2017.00029",
          postlink:"",
        },
        {
          id: 14,
          authors:"Reznikov N, Phillips C, Cooke M, Garbout A, Ahmed F, Stevens MM.",
          title:"Functional adaptation of the calcaneus in historical foot binding",
          prelink:"J Bone Miner Res, 2017, 32(9):1915-1925 ",
          link:"https://doi.org/10.1002/jbmr.3185",
          postlink:"(cover article, and received American Society for Bone and Mineral Research / Journal of Bone and Mineral Research Raisz-Drezner Award)",
        },
        {
          id: 15,
          authors:"Kim E, Zwi-Dantsis L, Reznikov N, Hansel CS, Agarwal S, Stevens MM.",
          title:"One-pot synthesis of multiple protein-encapsulated DNA flowers and their application in intracellular protein delivery",
          prelink:"Adv Mater, 2017, 29:1701086 ",
          link:"https://doi.org/10.1002/adma.201701086",
          postlink:"",
        },
        {
          id: 16,
          authors: "Reznikov N, Steele JAM, Fratzl P, Stevens MM.",
          title:"A materials science vision of extracellular matrix mineralization",
          prelink:"Nature Reviews Mater, 2016:16041. ",
          link:"https://doi.org/10.1038/natrevmats.2016.41",
          postlink:"",
        },
        {
          id: 17,
          authors:"Reznikov N, Chase H, Ben Zvi Y, Tarle V, Singer M, Brumfeld V, Shahar R, Weiner S.",
          title:"Intertrabecular angle: a new topological parameter of trabecular bone architecture in the human proximal femur",
          prelink:"Acta Biomater, 2016; 44:65-72. ",
          link:"https://doi.org/10.1016/j.actbio.2016.08.040",
          postlink:"",
        },
        {
          id: 18,
          authors: "Reznikov N, Chase H, Brumfeld V, Shahar R, Weiner S.",
          title:"The 3D Structure of the collagen fibril network in human trabecular bone: relation to trabecular organization",
          prelink:"Bone, 2015; 71:189-195. ",
          link:"https://doi.org/10.1016/j.bone.2014.10.017",
          postlink:"",
        },
        {
          id: 19,
          authors: "Atkins A, Reznikov N, Ofer L, Masic A, Weiner S, Shahar R.",
          title:"The three-dimensional structure of anosteocytic lamellated bone of fish",
          prelink:"Acta Biomater, 2015; 13:311-323. ",
          link:"https://doi.org/10.1016/j.actbio.2014.10.025",
          postlink:"",
        },
        {
          id: 20,
          authors: "Reznikov N, Shahar R, Weiner S.",
          title: "Bone hierarchical structure in three dimensions",
          prelink:"Acta Biomater, 2014; 10:3815-3826. ",
          link:"https://doi.org/10.1016/j.actbio.2014.05.024",
          postlink:"",
        },
        {
          id: 21,
          authors: "Almany-Magal R, Reznikov N, Shahar R, Weiner S.",
          title:"Three-dimensional structure of minipig fibrolamellar bone: adaptation to axial loading",
          prelink:"J Struct Biol, 2014; 186:253-264. ",
          link:"https://doi.org/10.1016/j.jsb.2014.03.007",
          postlink:"",
        },
        {
          id: 22,
          authors: "Reznikov N, Shahar R, Weiner S.",
          title:"Three-dimensional structure of human lamellar bone: the presence of two different materials and new insights into the hierarchical organization",
          prelink:"Bone, 2014; 59:93-104. ",
          link:"https://doi.org/10.1016/j.bone.2013.10.023",
          postlink:"",
        },
        {
          id: 23,
          authors: "Reznikov N, Almany-Magal R, Shahar R, Weiner S.",
          title:"Three-dimensional imaging of collagen fibril organization in rat circumferential lamellar bone using a dual beam electron microscope reveals ordered and disordered sub-lamellar structures",
          prelink:"Bone, 2013; 52:676–683. ",
          link:"https://doi.org/10.1016/j.bone.2012.10.034",
          postlink:"",
        },
        {
          id: 24,
          authors: "Faingold A, Cohen S, Reznikov N, Wagner DH.",
          title:"Osteonal lamellae elementary units: lamellar microstructure, curvature and mechanical properties",
          prelink:"Acta Biomater, 2013; 9:5956-5962. ",
          link:"https://doi.org/10.1016/j.actbio.2012.11.032",
          postlink:"",
        },
        {
          id: 25,
          authors: "Reznikov N, Barkana I, Abed Y, Har-Zion G, Redlich M.",
          title:"Measurement of friction forces between stainless steel wires and \"reduced-friction\" self-ligating brackets",
          prelink:"Am J Orth Dent Orthop, 2010; 138:330-338. ",
          link:"https://doi.org/10.1016/j.ajodo.2008.07.025",
          postlink:"",
        },
        {
          id: 26,
          authors: "Reznikov N, Barkana I, Abed Y, Har-Zion G, Redlich M.",
          title:"Influence of friction resistance on expression of superelastic properties of initial NiTi wires in \"reduced friction\" and conventional bracket systems",
          prelink:"J Dent Biomech, 2010; 1:613142. ",
          link:"http://dx.doi.org/10.4061/2010/613142",
          postlink:"",
        },
      ],
    };
  },
};
</script>

<style scoped>
#Publications {
  text-align: left;
  position: relative;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.63);
}
.TextBox {
  position: absolute;
  width: 80%;
  height: 80%;
  top: 10%;
  left: 10%;
}

.TextBox a {
  color: #6feb95;
}

.TextBox a:visited {
  color: #4c8c65;
}

.TextBox a:hover {
  color: #6feb95;
}
</style>
