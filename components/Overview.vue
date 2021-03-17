<template>
  <section class="overview-section" style="background-image: url('/overview-bg.jpg')">
      <div class="container-fluid">
          <div class="row">
              <div class="col-12">
                  <div class="section-title">
                      <h2>overview</h2>
                      <div class="section-title-dots">
                            <span></span>
                            <span></span>
                            <span></span>
                      </div>
                  </div>
                  <p class="text-center">
                      Andalusia is one of the leading regional players in the healthcare provision space in the Middle East. With a network of general hospitals, specialized medical centers, and polyclinics across Egypt and Saudi Arabia, Andalusia has built a unique footprint both in service spectrum and geographically. Andalusia Group for Medical Services was founded in 1984 by the entrepreneur Dr. Darweesh Zagzoug as a single hospital in Jeddah, Saudi Arabia; and grown over 30 years to own and manage several healthcare facilities in both Saudi and Egypt. The second generation family owner Dr. Hazem Zagzoug, the current CEO has made it possible for a renowned financial institution like the IFC to join forces to serve more than 7 million patients in the last 10 years with amicable quality, and creating 2000 new jobs. We are proud of our origin, our progress, as well as our partners. 
                  </p>
              </div>
          </div>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style>
.overview-section {
    background-size: cover;
    background-position: center center;
}

section.overview-section:before {content: '';position: absolute;top: 0;left: 0;right: 0;bottom: 0;background: #322f2e;opacity: 0.95;}

.overview-section .section-title h2 {
    color: #fff;
}

.overview-section p {
    color: #fff;
    font-size: 24px;
    font-weight: 300;
}

.overview-section .section-title {
    margin-bottom: 60px;
}
</style>