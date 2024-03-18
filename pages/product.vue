<template>
  <div>
    <Nav />
    <section class="page-header">
      <div class="container">
        <div class="page-wrapper">
          <article>
            <h1 class="site-title">Products</h1>
          </article>
        </div>
      </div>
    </section>
    <section class="product-list1 row-max-grid">
      <div class="container">
        <div class="new-product">
          <div class="text-desc">
            <h2>New Products</h2>
            <p>
              The Company is producing quality plastic product by using modern
              production techniques through the creation of employment and
              saving the foreign currency reserve of the country .The factory is
              managed by qualified engineers and administrative workers
              specialized in all aspects of manufacturing work.
            </p>
          </div>
          <img src="../assets/img/proplast2.jpg" alt="" />
        </div>
        <div class="all-product">
          <div class="single-product"></div>
        </div>
      </div>
    </section>
    <div class="wrapper">
      <section class="module product-list">
        <h3 class="section-title"><b>List of</b><span>Products</span></h3>
      </section>
      <section class="product-all-list">
        <div class="list">
          <div class="container">
            <div class="single-list">
              <img class="img-tab" src="../assets/img/HDPEPIPES.png" alt="" />
              <h3>HDPE PIPES</h3>
              <p>
                HDPI pipes which PPI produced is manufactured from high degree
                of impact resistance and are robust and ductile. HDPE pipes have
                the ability to absorb pressure surges which make the superior to
                other plastic materials.PPI mainly using PE100 with highest
                specific weight. PPI HDPE pipes are produced in accordance to
                ESISO4427 to meet the required standard.
              </p>
            </div>
            <div class="single-list">
              <img src="../assets/img/HDptable.png" alt="" />
            </div>
            <!-- <div class="single-list">
              <img src="../assets/img/HDPEPIPES.png" alt="" />

              <button class="btn btn-secondary row-max-grid">
                <a href="./order"> Order Now</a>
              </button>
            </div> -->
            <div class="single-list">
              <img class="img-tab" src="../assets/img/upvc.webp" alt="" />
              <h3>UPVC PIPES</h3>
              <p>
                Fully compliant to the ISO 1452 standards.PVC is one of the
                oldest plastic resins and it’s globally the second most used
                resin below ethylene. Unlike HDPE PVC cannot be processed in its
                pure form and additives need to be added and then blended to
                increase its heat stability and other characteristics.  
              </p>
            </div>
            <div class="single-list">
              <img src="../assets/img/u-pvsTable.png" alt="" />
            </div>
            <div class="single-list">
              <img class="img-dsc" src="../assets/img/PPRFITTINGS.jpg" alt="" />
              <h3>PPR FITTINGS</h3>
              <p>
                We Produces a complete range of polypropylene (PPR) pipes for
                cold and hot water distribution system for household ,portable
                water and buildings.PPI PPR pipes are made from PP random
                copolymer (PP-R or R 200P) granules which have excellent heat
                resistance ,physical and chemical properties to suit application
                of portable water distribution and heating system.
              </p>
            </div>
            <div class="single-list">
              <img src="../assets/img/pprpipe.png" alt="" />
            </div>
            <div class="single-list">
              <img src="../assets/img/upvc.jpg" alt="" />
              <h4>UPVC FITTINGS</h4>
              <p>
                are an engineered plastic known as Unplasticized Polyvinyl
                Chloride. In the lack of plasticizers, which increase plastic's
                flexibility and reduce its brittleness, something is said to be
                "unplasticized."
              </p>
            </div>
            <div class="single-list"></div>
            <div class="single-list">
              <button class="btn btn-secondary row-max-grid">
                <a href="./order"> Order Now</a>
              </button>
            </div>
            <div class="single-list">
              <img src="../assets/img/ppr.jpg" alt="" />
              <h4>PPR PIPES</h4>
              <p>
                (A polypropylene random co-polymer)is a type of plastic pipe
                constructed from this substance.
              </p>
            </div>
            <div class="single-list">
              <h3>OD 20</h3>
              <h3>OD 25</h3>
              <h3>OD 32</h3>
            </div>
            <div class="single-list">
              <h3>OD 40</h3>
              <h3>OD 50</h3>
              <h3>OD 63</h3>
              <button class="btn btn-secondary row-max-grid">
                <a href="./order"> Order Now</a>
              </button>
            </div>
            <div class="single-list">
              <img src="../assets/img/condi.jpg" alt="" />
              <h4>Conduits</h4>
              <p>
                is a tube used in a building or other structure to protect and
                route electrical wiring. Metal, plastic, fiber, or burned clay
                can all be used to make electrical conduit.
              </p>
            </div>
            <div class="single-list">
              <h3>13 mm</h3>
              <h3>16 mm</h3>
              <h3>19 mm</h3>
              <h3>21 mm</h3>
            </div>
            <div class="single-list">
              <h3>25 mm</h3>
              <h3>32 mm</h3>
              <h3>40 mm</h3>

              <button class="btn btn-secondary row-max-grid">
                <a href="./order"> Order Now</a>
              </button>
            </div>
          </div>
        </div>
      </section>
      <Contactus />
    </div>
    <Footer />
  </div>
</template>

<script>
import Footer from "../components/Footer.vue";
import Contactus from "../components/Contactus.vue";
import Nav from "../components/Nav.vue";
export default {
  name: "IndexPage",
  mounted() {
    window.addEventListener("load", (event) => {
      const arrowNext = document.querySelector(".button-next"),
        arrowPrev = document.querySelector(".button-prev"),
        imageActive = document.querySelector(".active img"),
        imageNext = document.querySelector(".next img"),
        slideActive = document.querySelector(".active"),
        slideNext = document.querySelector(".next");

      const images = [
        {
          id: 0,
          image: "https://rafaelalucas.com/dailyui/3/assets/angele-03.jpg",
        },
        {
          id: 1,
          image: "https://rafaelalucas.com/dailyui/3/assets/angele-10.jpg",
        },
        {
          id: 2,
          image: "https://rafaelalucas.com/dailyui/3/assets/angele-11.jpg",
        },
        {
          id: 3,
          image: "https://rafaelalucas.com/dailyui/3/assets/angele-12.jpg",
        },
      ];

      arrowNext.addEventListener("click", nextPhoto);
      arrowPrev.addEventListener("click", prevPhoto);

      function nextPhoto() {
        const nextId = ~~imageNext.dataset.id + 1,
          nextPicture = images.find((element) => element.id == nextId),
          bullet = document.querySelectorAll(".bullet"),
          activeBullet = [...bullet].find(
            (element) => element.dataset.id == ~~imageNext.dataset.id
          );

        // Add Classes to Anime Photos

        slideNext.classList.add("anime-next-in");
        slideActive.classList.add("anime-in");

        // To Remove the Class that anime in
        setTimeout(function () {
          slideActive.classList.remove("anime-in");
          slideNext.classList.remove("anime-next-in");
        }, 960);

        // To Populate the Active and Next Slide

        imageActive.src = imageNext.src;
        imageActive.dataset.id = imageNext.dataset.id;

        if (imageActive.dataset.id == images.length - 1) {
          imageNext.src = images[0].image;
          imageNext.dataset.id = images[0].id;
        } else {
          imageNext.src = nextPicture.image;
          imageNext.dataset.id = nextPicture.id;
        }

        // To Add Active bullets
        bullet.forEach(function (el) {
          el.classList.remove("selected");
        });
        activeBullet.classList.add("selected");
      }

      function prevPhoto() {
        const prevId = ~~imageActive.dataset.id - 1,
          prevPicture = images.find((element) => element.id == prevId),
          bullet = document.querySelectorAll(".bullet");
        let activeBullet = [...bullet].find(
          (element) => element.dataset.id == prevId
        );

        // Add Classes to Anime Photos

        slideActive.classList.add("anime-out");
        slideNext.classList.add("anime-next-out");

        // To Remove the Class that anime in
        setTimeout(function () {
          slideActive.classList.remove("anime-out");
          slideNext.classList.remove("anime-next-out");
        }, 960);

        // To Populate the Active and Next Slide
        if (imageActive.dataset.id == 0) {
          imageNext.src = imageActive.src;
          imageNext.dataset.id = imageActive.dataset.id;
          imageActive.src = images[images.length - 1].image;
          imageActive.dataset.id = images[images.length - 1].id;
          activeBullet = [...bullet].find(
            (element) => element.dataset.id == imageActive.dataset.id
          );
        } else {
          imageNext.src = imageActive.src;
          imageNext.dataset.id = imageActive.dataset.id;
          imageActive.src = prevPicture.image;
          imageActive.dataset.id = prevPicture.id;
        }

        // To Add Active bullets
        bullet.forEach(function (el) {
          el.classList.remove("selected");
        });
        activeBullet.classList.add("selected");
      }

      // To Populate the first images on page load
      imageActive.src = images[0].image;
      imageActive.dataset.id = images[0].id;

      imageNext.src = images[1].image;
      imageNext.dataset.id = images[1].id;

      // Sticky menu

      window.onscroll = function () {
        if (window.pageYOffset >= 90) {
          iconMenu.classList.add("sticky");
        } else {
          iconMenu.classList.remove("sticky");
        }
      };
      // open menu

      const iconMenu = document.querySelector(".icon-menu"),
        menuOverlay = document.querySelector(".main-nav"),
        body = document.querySelector("body");

      iconMenu.addEventListener("click", openMenu);

      // Sticky menu

      window.onscroll = function () {
        if (window.pageYOffset >= 90) {
          iconMenu.classList.add("sticky");
        } else {
          iconMenu.classList.remove("sticky");
        }
      };

      function openMenu() {
        if (iconMenu.classList.contains("icon-open")) {
          menuOverlay.classList.add("menu-close");
          iconMenu.classList.remove("icon-open");
          body.classList.remove("no-scroll");
          iconMenu.classList.remove("sticky");

          setTimeout(function () {
            menuOverlay.classList.remove("menu-open");
          }, 800);
          setTimeout(function () {
            menuOverlay.classList.remove("menu-close");
          }, 900);
        } else {
          menuOverlay.classList.remove("menu-close");
          menuOverlay.classList.add("menu-open");
          iconMenu.classList.add("icon-open");
          body.classList.add("no-scroll");

          setTimeout(function () {
            iconMenu.classList.remove("sticky");
          }, 500);
        }
      }

      // open modal video

      const videoItem = document.querySelectorAll(".video-item"),
        modalVideo = document.querySelector(".modal-video"),
        iconCloseVideo = document.querySelector(".close-video"),
        videoFrame = document.querySelector(".video-code iframe"),
        videoOpen = document.querySelector(".video-open");

      videoItem.forEach(function (el) {
        el.addEventListener("click", openVideo);
      });

      iconCloseVideo.addEventListener("click", closeVideo);
      // body.addEventListener("click", closeVideo);

      function openVideo(e) {
        const videoSrc = e.currentTarget.dataset.video;

        body.classList.add("no-scroll");

        modalVideo.classList.add("video-open");

        videoFrame.src = videoSrc;
      }

      // ytLink.href = videoUrl;

      function closeVideo() {
        body.classList.remove("no-scroll");
        modalVideo.classList.remove("video-open");
        videoFrame.src = "";
      }
    });
  },
  components: { Footer, Contactus, Nav },
};
</script>
