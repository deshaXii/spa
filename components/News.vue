<template>
  <section class="news-section">
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="section-title">
            <h2>RECENT NEWS</h2>
            <div class="section-title-dots">
              <span></span>
              <span></span>
              <span></span>
            </div>
          </div>
        </div>
        <div class="col-md-4">
            <div class="news-box">
                <div class="news-img-box">
                    <img src="/news1.jpg" alt="">
                </div>
                <div class="news-info-box">
                    <a href="#"><h4>How to Improve Your Sales Volume</h4></a>
                    <span class="news-date">23 AUG, 2018</span>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod teminc ididunt ut labore et dolore.</p>
                    <a href="#" class="more-btn">read more</a>
                </div>
            </div>
        </div>
        <div class="col-md-4">
            <div class="news-box">
                <div class="news-img-box">
                    <img src="/news2.jpg" alt="">
                </div>
                <div class="news-info-box">
                    <a href="#"><h4>How to Improve Your Sales Volume</h4></a>
                    <span class="news-date">23 AUG, 2018</span>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod teminc ididunt ut labore et dolore.</p>
                    <a href="#" class="more-btn">read more</a>
                </div>
            </div>
        </div>
        <div class="col-md-4">
            <div class="news-box">
                <div class="news-img-box">
                    <img src="/news3.jpg" alt="">
                </div>
                <div class="news-info-box">
                    <a href="#"><h4>How to Improve Your Sales Volume</h4></a>
                    <span class="news-date">23 AUG, 2018</span>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod teminc ididunt ut labore et dolore.</p>
                    <a href="#" class="more-btn">read more</a>
                </div>
            </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style>
.news-box {
    box-shadow: 0px 2px 5px rgb(174 174 174 / 45%);
}

.news-box .news-info-box {
    padding: 20px 32px;
}

.news-box .news-info-box h4 {
    color: #101010;
    font-size: 20px;
    margin-bottom: 5px;
    text-transform: capitalize;
    transition: all .2s linear;
    font-weight: bold;
    line-height: 24px;
}
.news-box .news-info-box a:hover h4 {
    opacity: 0.9;
    color: #777;
}

.news-box .news-info-box .news-date {
    color: #101010;
    opacity: 0.6;
    font-size: 14px;
    margin-bottom: 15px;
    display: block;
    text-transform: uppercase;
}

.news-box .news-info-box p {
    color: #101010;
    opacity: 0.9;
    font-size: 14px;
}

.news-box .news-img-box img {
    width: 100%;
    object-fit: cover;
    max-height: 200px;
    height: 200px;
}

.news-box .news-info-box .more-btn {
    background: linear-gradient(to right, #eb6b3d, #e7643a);
    border: none;
    border-radius: 0;
    min-width: 145px;
    min-height: 43px;
    text-transform: capitalize;
    font-size: 22px;
    font-family: "Corbel";
    display: inline-block;
    color: #fff;
    text-align: center;
    line-height: 43px;
    height: 43px;
}
</style>