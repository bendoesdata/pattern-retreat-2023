<template>
  <v-app>
    <v-main>
      <div class="grid">
        <div class="grid-side">
          <div style=" text-align: center; margin: 0 auto; margin-bottom: 30px; margin-right: 40px">
            <img src="@/assets/pattern-logo-RGB.svg" style="width: 300px; height: auto;" alt="">
          </div>
          <div>
            <p>
              Biomedical scientists rely on patient participation for their
              research. But the benefits of a breakthrough are not always felt
              for these patients in their lived experience.
            </p>
            <p>
              <b>
              How can we use visualization to narrow the gap between new
              biological insights and impact for patients?
            </b>
            </p>

            <p>
              Pattern is a visualization lab situated within the Broad Institute
              with a mission to create visual tools and resources that drive
              science forward. We present three projects that features the use
              of visualization techniques to provide immediate value to patients
              in the form of more personal health information, a greater
              understanding of their disease, and the role of uncertainty and
              variability in genetic risk factors.
            </p>
            <div>
              <img src="@/assets/diagram.png" style="width: 100%" alt="">
            </div>
          </div>
        </div>
        <div class="grid-main">
          <v-expansion-panels>
            <v-expansion-panel expanded="true">
              <v-expansion-panel-title color="#F36C3E"> 
                <div class="acc-header">
                <img src="@/assets/circle-icon.png" alt="">
                <h3> MINERVA: An interactive survey that predicts the likelihood of neurodevelopmental genetic variants in autistic children </h3>
              </div>
              </v-expansion-panel-title>
              <v-expansion-panel-text>
                <div class="grid">
                  <div class="grid-side">
                    <p class="subtitle">
                      An interactive survey tool for caregivers of autistic
                      children predict the likelihood of a having genetic
                      variant.
                    </p>
                    <p>
                      Genetic testing is currently recommended by the American
                      Academy of Pediatrics for all children with autism.
                      However, many clinicians and families report feeling under
                      informed about genetics and genetic testing. Insurance
                      also will not cover genetic testing in most cases.
                    </p>

                    <p>
                      Certain genetic variants have been identified as
                      especially impactful for an autistic child s development.
                      MINERVA is an interactive survey tool that uses a machine
                      learning model to identify the likelihood of an autistic
                      child having a neurodevelopmental disorder associated
                      variants (NDAVs) based on factors like age at walking,
                      verbal processing, and other physical milestones in
                      development
                    </p>
                  </div>
                  <div class="grid-main">
                    <div class="gray-box"></div>
                  </div>
                </div>
              </v-expansion-panel-text>
            </v-expansion-panel>

            <v-expansion-panel>
              <v-expansion-panel-title color="#00AFD7"> 
                <div class="acc-header">
                  <img src="@/assets/bacteria-icon.png" alt="">
                <h3>GutSee: A mobile app to help patients track and visualize their gut microbiome data</h3>  
                </div>
              </v-expansion-panel-title>
              <v-expansion-panel-text>
                <div class="grid">
                  <div class="grid-side">
                    <p class="subtitle">
                      A mobile app built for patients in a longitudinal study on how the microbiome affects Inflammatory bowel disease (IBD) and ulcerative colitis (UC) flare-ups.
                      </p>
                      <p>
                      Inflammatory bowel disease (IBD) is an unpredictable and sometimes debilitating condition with few treatment options. We developed the GutSee in collaboration with MIT’s Center for Microbiome Informatics and Therapeutics to actively engage IBD sufferers with an intuitive and friendly user interface for logging and later viewing their symptoms and diet.
                    </p>
                  </div>
                  <div class="grid-main">
                    <div class="gray-box">

                    </div>
                  </div>
                </div>
              </v-expansion-panel-text>
            </v-expansion-panel>
            <v-expansion-panel>
              <v-expansion-panel-title color="#69488E">
                <div class="acc-header">
                  <img src="@/assets/dna-icon.png" style="height: 25px; margin-left: 5px" alt="">
                  <h3 style="margin-left: 15px">Polygenic Scores Explained: A scrolling visual explainer on how to interpret polygenic risk scores</h3>
                </div>
              </v-expansion-panel-title>
              <v-expansion-panel-text>
                <div class="grid">
                  <div class="grid-side">
                    <p class="subtitle">
                      An interactive scrolly site that explains how to understand and interpret polygenic risk scores.
                    </p>
                    <p>
                      To improve genetic risk communication and support non-genetics clinicians and patients as they return and receive polygenic scores, we designed and developed a new polygenic score report and a supplemental web-based resource that utilizes scroll-based visualization techniques to provide a step-by-step explanation for understanding and interpreting polygenic scores.
                    </p>
                    <p>
                      Strong preference for colors over complex visualizations (2)
                      Annotations, risk categories, and reference-points aided in understanding (2)
                    </p>
                  </div>
                  <div class="grid-main">
                    <div class="gray-box">
                      <img src="@/assets/dna.gif" alt="">
                    </div>
                  </div>
                </div>
              </v-expansion-panel-text>
            </v-expansion-panel>
          </v-expansion-panels>
        </div>
      </div>
    </v-main>
    <v-footer>
      <span class="text-center">&copy; Pattern 2023</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    trip: {
      name: "",
      location: null,
      start: null,
      end: null,
    },
    locations: [
      "Australia",
      "Barbados",
      "Chile",
      "Denmark",
      "Ecuador",
      "France",
    ],
  }),
};
</script>

<style>
/* create grid with 12 columns, 1 row */
.grid {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: 1fr;
  grid-gap: 10px;
  margin: 10px;
}

/* create a grid item that spans 4 columns */
.grid-side {
  grid-column: span 4;
  padding: 1rem;
}

/* create a grid item that spans 8 columns */
.grid-main {
  grid-column: span 8;
  padding: 1rem;
}

.gray-box {
  background-color: #d2d2d2;
  width: 100%;
  height: 500px;
}

.subtitle {
  font-weight: 600;
}

p {
  font-size: 1rem;
  line-height: 1.5;
  margin: 0 0 1.5rem 0;
}

.acc-header * {
  display: inline
}

.acc-header {
  display: flex;
  align-items: center;
}

.acc-header h3 {
  margin-left: 10px;
  margin-top: 3px
}

.acc-header img {
  height: 25px;
  width: auto;
}

.gray-box img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
