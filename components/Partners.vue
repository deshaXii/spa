<template>
  <section class="partners-section">
    <div class="container-fluid">
      <div class="row">
        <div class="col-12">
          <div class="section-title">
            <h2>GREAT PARTNERS</h2>
            <div class="section-title-dots">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
          <ul class="partners-box">
              <li>
                  <a href="#">
                      <img src="/partner1.png" alt="">
                  </a>
              </li>
              <li>
                  <a href="#">
                      <img src="/partner2.png" alt="">
                  </a>
              </li>
              <li>
                  <a href="#">
                      <img src="/partner3.png" alt="">
                  </a>
              </li>
              <li>
                  <a href="#">
                      <img src="/partner4.png" alt="">
                  </a>
              </li>
              <li>
                  <a href="#">
                      <img src="/partner5.png" alt="">
                  </a>
              </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.partners-section {
    background: linear-gradient(to right, #e8653a, #cd3925);
}

.partners-section a img {filter: invert(100%) sepia(0%) saturate(7457%) hue-rotate(263deg) brightness(513%) contrast(99%);opacity: 0.7;transition: all 0.2s linear;}

.partners-section .partners-box {
    padding: 0;
    margin: 0;
    list-style: none;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.partners-section .partners-box img:hover {
    opacity: 1;
}

.partners-section .section-title h2 {
    color: #fff;
}

.partners-section .section-title span {
    background: #fff;
}

.partners-section .section-title {
    margin-bottom: 50px;
}
</style>