# Pollution-analysis

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Go Green</title>

    <!-- FAVICON -->
    <link rel="icon" type="image/png" href="images/favicon.png" />

    <!-- Bootstrap 5 CDN Links -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/5.1.0/css/bootstrap.min.css"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.3.0/css/font-awesome.min.css"
    />

    <!-- Custom File's Link -->
    <style>
      .banner_wrapper {
        height: 100%;
        margin: 0;
        /* The image used */
        background-image: url("https://sp-ao.shortpixel.ai/client/to_webp,q_glossy,ret_img,w_664,h_242/https://aeramaxpro.com/wp-content/uploads/aeramax/2017/01/china-smog-6.gif");

        /* Full height */
        height: 50%;

        /* Center and scale the image nicely */
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
      }
      /* 1 General */

      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      :root {
        /* Background Color */
        --primary-color: #429f1d;
        --secondary-color: #333333;
        --bg-black: #111111;
        --bg-dark: #1c1819;
        --bg-white: #fff;
        --bg-gray: #e5e5e5;

        /* Text Color */
        --primary-text: #429f1d;
        --text-white: #fff;
        --text-black: #325b17;

        /* Font Family */
        --primary-font: "Ubuntu", sans-serif;
        --secondary-font: "Open Sans", sans-serif;
      }

      body {
        font-family: var(--secondary-font);
        background-color: var(--bg-white);
      }

      a {
        text-decoration: none;
      }

      /* 1 Custom CSS */

      ::-webkit-scrollbar {
        width: 6px;
      }

      ::-webkit-scrollbar-track {
        background: var(--bg-dark-blue);
      }

      ::-webkit-scrollbar-thumb {
        background: var(--primary-color);
      }

      section {
        padding: 100px 0;
      }

      .main-btn {
        display: inline-block;
        border-radius: 50px;
        padding: 10px 27px;
        border: 1px solid var(--primary-color);
        color: var(--primary-text);
        font-weight: 600;
        font-size: 14px;
        text-transform: uppercase;
        letter-spacing: 1px;
        background: linear-gradient(
          to right,
          var(--primary-color) 50%,
          transparent 50%
        );
        background-size: 200% 100%;
        background-position: right bottom;
        transition: all 0.5s ease-out;
      }
      .main-btn:hover {
        color: var(--text-white);
        background-position: left bottom;
      }

      h1 {
        font-size: 80px;
        line-height: 1.2;
        font-weight: 400;
        color: var(--text-black);
        margin-bottom: 20px;
        font-family: var(--primary-font);
      }

      h1 span {
        color: var(--primary-color);
      }

      h2 {
        font-weight: 700;
        font-size: 35px;
        margin-bottom: 15px;
        color: var(--text-black);
        font-family: var(--primary-font);
      }

      h3 {
        font-weight: 700;
        font-size: 28px;
        margin-bottom: 15px;
        color: var(--text-black);
        font-family: var(--primary-font);
      }

      h5 {
        font-weight: 700;
        font-size: 20px;
        color: var(--primary-text);
      }

      p {
        color: var(--text-black);
        font-size: 18px;
        line-height: 1.7;
        letter-spacing: 1px;
        font-weight: 300;
      }

      /* 2 Navbar */
      .header_wrapper .navbar {
        padding: 15px 0;
        -webkit-transition: all 0.2s linear;
        -o-transition: all 0.2s linear;
        transition: all 0.2s linear;
      }

      .header_wrapper .navbar-brand img {
        max-width: 120px;
        height: auto;
      }

      .header_wrapper .navbar-toggler:focus {
        box-shadow: none;
      }

      .header_wrapper .nav-item {
        margin: 0 10px;
      }

      .header_wrapper .nav-item .nav-link {
        font-size: 18px;
        font-weight: 500;
        letter-spacing: 1px;
        color: var(--text-black);
        display: inline-block;
      }

      .header_wrapper .nav-item .nav-link.active,
      .header_wrapper .nav-item .nav-link:hover {
        color: var(--primary-text);
      }

      .header-scrolled {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        background-color: var(--bg-white);
        -webkit-box-shadow: 0 4px 6px 0 rgba(12, 0, 46, 0.05);
        box-shadow: 0 4px 6px 0 rgba(12, 0, 46, 0.05);
      }

      /* 3 Banner */
      .banner_wrapper {
        padding-top: 100px;
      }

      .banner_wrapper .top-menu .card {
        height: 275px;
        overflow: hidden;
        cursor: pointer;
      }

      .banner_wrapper .top-menu .card img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        transition: transform 500ms ease;
      }

      .banner_wrapper .top-menu .card:hover img {
        transform: scale(1.1);
      }

      /* 4 About */
      .about_wrapper {
        background-color: var(--bg-gray);
        padding-bottom: 130px;
      }

      .about_wrapper .card {
        z-index: 10;
        right: -25%;
        top: 30%;
      }

      /* 5 menu wrapper */
      .menu_wrapper {
        width: 100%;
        height: auto;
        background-image: url("");
        background-repeat: no-repeat;
        background-position: 50% 50%;
        background-size: cover;
        background-color: var(--bg-gray);
      }

      .menu_wrapper .row {
        padding-top: 70px;
      }

      .menu_wrapper .card {
        background-color: var(--secondary-color);
      }

      .menu_wrapper .card h3,
      .menu_wrapper .card p {
        color: var(--text-white);
      }

      .menu_wrapper .card h3 span {
        background-color: var(--primary-color);
        width: 70px;
        height: 70px;
        display: inline-block;
        text-align: center;
        line-height: 70px;
        font-size: 40px;
        border-radius: 50%;
        margin-right: 20px;
      }

      /* 6 offers */
      .offers_wrapper .card {
        height: 100%;
        min-height: 260px;
        box-shadow: 0 0 16px 4px var(--bg-dark-blue);
        background-position: 50% 50%;
        background-size: cover;
      }

      .offers_wrapper .card .offer-text {
        width: 50%;
        height: 100%;
        background-color: var(--bg-black);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
      }

      /* 7 review */

      .review_wrapper {
        width: 100%;
        height: auto;
        background-image: url("https://images.unsplash.com/photo-1582980752625-10783b273e2d?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxzZWFyY2h8OXx8cG9sbHV0aW9ufGVufDB8fDB8fA%3D%3D&w=1000&q=80");
        background-repeat: no-repeat;
        background-position: 50% 50%;
        background-size: cover;
      }

      .review_wrapper .carousel-item {
        min-height: 500px;
        height: 100%;
      }

      .review_wrapper .carousel-item img {
        width: 65px;
        margin-bottom: 20px;
      }

      .review_wrapper .carousel-control-prev-icon,
      .review_wrapper .carousel-control-next-icon {
        filter: brightness(0.1);
      }

      /* 8 footer */
      .footer_wrapper {
        background-color: var(--bg-white);
        padding: 20px 0;
      }

      .footer_wrapper .footer-logo img {
        width: 100px;
      }

      .footer_wrapper .social-icon li {
        margin: 6px;
      }

      .footer_wrapper .social-icon a {
        width: 35px;
        height: 35px;
        line-height: 30px;
        font-size: 14px;
        display: inline-block;
        border: 2px solid var(--bg-black);
        color: var(--text-black);
        text-align: center;
        border-radius: 100%;
        -webkit-transition: all 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
        transition: all 0.3s cubic-bezier(0.645, 0.045, 0.355, 1);
      }

      .footer_wrapper .social-icon a:hover {
        background-color: var(--primary-color);
        border-color: var(--primary-color);
        color: var(--text-white);
        box-shadow: 0 10px 15px 0 rgb(0 0 0 / 10%);
        transform: translateY(-3px);
      }

      .footer_wrapper .copyright-text p {
        font-size: 11px;
        line-height: 20px;
        font-weight: 600;
      }

      .footer_wrapper .copyright-text a {
        color: var(--primary-color);
      }

      /*Responsive Design*/
      @media (max-width: 1199px) {
        /* custom css */
        h1 {
          font-size: 65px;
        }
      }

      @media (max-width: 991px) {
        /* custom css */

        h2 {
          font-size: 30px;
          line-height: 40px;
        }

        h3 {
          font-size: 20px;
        }

        /* 2 Navbar */
        .header_wrapper .navbar-brand img {
          max-width: 80px;
        }

        .header-scrolled {
          height: auto;
        }
        .header_wrapper .navbar-collapse {
          margin-top: -2px;
        }
        .header_wrapper .menu-navbar-nav {
          text-align: center;
          background-color: var(--bg-white);
          padding-bottom: 15px;
        }

        .header_wrapper .nav-item .nav-link {
          margin-top: 15px;
        }

        .header_wrapper .navbar-brand img {
          max-width: 67px;
          height: auto;
        }

        /* banner */
        .banner_wrapper {
          padding-top: 70px;
        }

        .banner_wrapper .top-menu .card {
          height: 200px;
        }

        /* About */
        .about_wrapper {
          padding-bottom: unset;
        }

        .about_wrapper .card {
          z-index: 10;
          right: unset;
          top: unset;
        }
      }

      @media (max-width: 767px) {
        /* custom css */
        h1 {
          font-size: 40px;
          line-height: 48px;
        }

        p {
          font-size: 14px;
          line-height: 24px;
        }

        /* Menu */
        .menu_wrapper .row {
          padding-top: 70px;
        }

        .menu_wrapper .card h3 span {
          width: 50px;
          height: 50px;
          line-height: 50px;
          font-size: 30px;
        }

        /* offers */
        .offers_wrapper .card .offer-text {
          width: 65%;
        }

        /* review */
        .carousel-caption {
          bottom: 0;
        }

        .review_wrapper .carousel-item {
          min-height: 460px;
        }
      }
      .wrapper1 {
        padding-bottom: unset;
      }

      i.custom {
        font-size: 2em;
        color: rgb(41, 160, 41);
      }
    </style>
  </head>

  <body
    data-bs-spy="scroll"
    data-bs-target=".navbar"
    data-bs-offset="75"
    action="/index"
    method="GET"
  >
    <!-- <img
      src="https://i.kinja-img.com/gawker-media/image/upload/s--5FPmv1yn--/c_fit,fl_progressive,q_80,w_636/cu6hvck25tsdhetygf2c.gif"
      style="
        position: relative;
        background-repeat: no-repeat;
        background-size: cover;
      " -->
    <!-- Navbar section -->
    <header class="header_wrapper">
      <nav class="navbar navbar-expand-lg fixed-top">
        <div class="container">
          <a class="navbar-brand" href="#">
            <!-- <img
              src="data:image/png;base64,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"
              class="img-fluid"
              alt="logo"
            /> -->
          </a>
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarNav"
            aria-controls="navbarNav"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <i class="fas fa-stream navbar-toggler-icon"></i>
          </button>
          <div
            class="collapse navbar-collapse justify-content-end"
            id="navbarNav"
          >
            <ul class="navbar-nav menu-navbar-nav">
              <li class="nav-item">
                <a class="nav-link active" aria-current="page" href="#home"
                  >Home</a
                >
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#about">About</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#menu">Pollutions</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#review">FAQs</a>
              </li>
              <li class="nav-item mt-3 mt-lg-0">
                <a class="main-btn" href="https://forms.gle/HRcH8yaw7Lj4Hbq3A"
                  >Join</a
                >
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
    <!-- Navbar section exit -->

    <!-- Banner section -->
    <section id="home" class="banner_wrapper">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-5 text-center text-lg-start order-lg-1 order-2">
            <h1>
              <span>Go Green</span>
            </h1>
            <h2 style="color: beige">Smart Pollution Tropper</h2>
            <p style="color: #ffffff">
              We detect pollution in a very smart way.There are pollution all
              around you and for this you need a
              <i>smart way</i>, a <i>smart machine</i>to detect and report.
              Hence, this can help the citizens know about the condition of
              their city.
            </p>

            <a
              style="color: white"
              class="main-btn mt-4"
              href="https://forms.gle/HRcH8yaw7Lj4Hbq3A"
              >Join The Beta Launch</a
            >
          </div>
          <div class="col-lg-7 text-center order-lg-2 order-1"></div>
        </div>
        <!-- <div class="row top-menu mt-5">
          <div class="col-lg-3 col-sm-6 mb-4">
            <div class="card">
              <img
                src="Images/litti-chokha-or-liti-choka-from-bihar-jharkhand-and-uttar-pradesh-is-stuffed-with-chana-sattu-served-with-alu-or-aloo-baingan-bharta-desi-ghee-lehsun-2FK07X0.jpg"
                alt="menu"
              />
            </div>
          </div>
          <div class="col-lg-3 col-sm-6 mb-4">
            <div class="card">
              <img
                src="Images/Mochar_Ghonto_Recipe_with_Steps__to_clean_the_Plantain_flower__Traditional_Banana_Blossom_Curry_from_West_Bengal.jpg"
                alt="menu"
              />
            </div>
          </div>
          <div class="col-lg-3 col-sm-6 mb-4">
            <div class="card">
              <img
                src="Images/bihari_dal_pitha_recipe_traditional_bihari_delicacy.jpg"
                alt="menu"
              />
            </div>
          </div>
          <div class="col-lg-3 col-sm-6 mb-4">
            <div class="card">
              <img
                src="Images/bengali-traditional-food-patishapta-pitha-260nw-2044884164.webp"
                alt="menu"
              />
            </div>
          </div>
        </div> -->
      </div>
    </section>
    <!-- Banner section exit -->

    <!-- About section -->
    <section id="about" class="about_wrapper">
      <div class="container">
        <div class="row">
          <div class="col-xl-4 col-lg-5 mb-4 mb-lg-0 order-lg-1 order-2">
            <div class="card rounded-0">
              <div class="card-body pt-5">
                <h4>About US</h4>
                <p>
                  “The future depends on what you do in the present” - M.K
                  Gandhi<br />
                  every person living on the planet is responsible for what we
                  give back to our mother nature. we believe, together we can
                  join hands to create a sustainable ecosystem.
                  <br />Join us ! BE THE REVOLUTION!
                </p>

                <a href="#" class="main-btn mt-4">Learn More</a>
              </div>
            </div>
          </div>
          <div class="col-xl-8 col-lg-6 mb-4 mb-lg-0 order-lg-2 order-1">
            <img
              src="https://i.ndtvimg.com/i/2015-03/air-pollution_600x294_51427105180.png"
              width="1000"
              height="1900"
              class="img-fluid"
              alt="About Us"
            />
          </div>
        </div>
      </div>
    </section>
    <!-- About section exit -->

    <!-- Menu Section STARTS-->
    <section id="menu" class="offers_wrapper">
      <div class="container">
        <div class="row">
          <div class="col-sm-12 text-center mb-4">
            <h2>Go Green</h2>
            <p>
              Checkout Pollution Near You!!!<br class="d-none d-md-block" />
              Smart Pollution Troop has something for every pollution.
            </p>
          </div>
        </div>
        <div class="row">
          <div class="col-md-6 mb-4">
            <div
              class="card rounded-0"
              style="
                background-image: url('https://upload.wikimedia.org/wikipedia/commons/a/aa/AlfedPalmersmokestacks.jpg');
              "
            >
              <div class="offer-text bg-black bg-opacity-50">
                <h3 class="text-white">Air Pollution</h3>
                <!-- <h5>$8.50 <del class="fst-italic opacity-75">$10.50</del></h5> -->
                <h5>Coming Soon</h5>
                <a
                  href="https://colab.research.google.com/drive/1MIxd1wNXWoZZuU_jkd1zRnZnbcFhior7#scrollTo=qxxiEZ4Xw1FA"
                  class="main-btn mt-3"
                  >Explore</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <div
              class="card rounded-0"
              style="
                background-image: url('https://joy.videvo.net/videvo_files/video/free/2019-08/thumbnails/190802_05_PlasticPollution_HD_11_small.jpg');
              "
            >
              <div class="offer-text bg-black bg-opacity-50">
                <h3 class="text-white">Water Pollution</h3>
                <h5>Coming Soon</h5>
                <a
                  href="https://anshul407-waterquality-app-mpyp1g.streamlit.app/"
                  class="main-btn mt-3"
                  >Explore</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <div
              class="card rounded-0"
              style="
                background-image: url('https://img.freepik.com/premium-photo/pollution-concept-garbage-pile-trash-waste-dump-landfill-waste-from-household-global-warning_310913-1110.jpg?w=2000');
              "
            >
              <div class="offer-text bg-black bg-opacity-50">
                <h3 class="text-white">Garbage Detection</h3>
                <h5>Coming Soon</h5>
                <a
                  href="https://colab.research.google.com/drive/1nZUQdxuG2-4XqXNpjVwrJvBnhgoSIdl1?usp=sharing#scrollTo=lJSKKfZdzu9r"
                  class="main-btn mt-3"
                  >Explore</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <div
              class="card rounded-0"
              style="
                background-image: url('https://www.iberdrola.com/documents/20125/40615/suelo_746x419.jpg/0c7d2a0c-f3a8-0ec0-9ad7-61f7fbf023b6?t=1627531595008');
              "
            >
              <div class="offer-text bg-black bg-opacity-50">
                <h3 class="text-white">Soil Pollution</h3>
                <h5>Coming Soon</h5>
                <a
                  href="https://forms.gle/FhUHfX1i5u5CKQ7H6"
                  class="main-btn mt-3"
                  >Survey</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <div
              class="card rounded-0"
              style="
                background-image: url('https://starwalk.space/gallery/images/light-pollution/1920x1080.jpg');
              "
            >
              <div class="offer-text bg-black bg-opacity-50">
                <h3 class="text-white">Light Pollution</h3>
                <h5>Coming Soon</h5>
                <a
                  href="https://forms.gle/FhUHfX1i5u5CKQ7H6"
                  class="main-btn mt-3"
                  >Survey</a
                >
              </div>
            </div>
          </div>
          <div class="col-md-6 mb-4">
            <div
              class="card rounded-0"
              style="
                background-image: url('https://cdn.risingbd.com/media/imgAll/2017February/bg/sound20170205182237.jpg');
              "
            >
              <div class="offer-text bg-black bg-opacity-50">
                <h3 class="text-white">Noise Pollution</h3>
                <h5>Coming Soon</h5>
                <a
                  href="https://forms.gle/FhUHfX1i5u5CKQ7H6"
                  class="main-btn mt-3"
                  >Survey</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Menu Section exit -->

    <!--Frequently Asked Questions Section -->
    <section id="review" class="review_wrapper">
      <div class="container">
        <div class="row">
          <div class="col-lg-5 col-md-7 col-sm-7">
            <div class="card rounded-0 bg-white p-2">
              <div
                id="carouselExampleCaptions"
                class="carousel slide"
                data-bs-ride="carousel"
              >
                <div class="carousel-inner">
                  <div class="carousel-item active">
                    <div class="carousel-caption">
                      <!-- <img
                        src="Images/nolen-gurer-payeshrice-kheer-with-date-palm-jaggery-recipe-main-photo.webp"
                      /> -->
                      <h3>Q. What are the natural causes of air pollution?</h3>
                      <p>
                        Natural sources of air pollution include forest fires
                        and volcanoes, which pollute the air with smoke and
                        dust.
                      </p>
                    </div>
                  </div>
                  <div class="carousel-item">
                    <div class="carousel-caption">
                      <!-- <img
                        src="Images/sweet-roasted-makhana-kheer-indian-dessert-recipe-served-bowl-garnished-dry-fruits-tasty-made-using-foxnuts-188700295.jpg"
                      /> -->
                      <h3>Q. What Is Pollution Control?</h3>
                      <p>
                        Pollution control is a term used in environmental
                        management. It means the control of emissions and
                        effluents into air, water or soil.
                      </p>
                    </div>
                  </div>

                  <div class="carousel-item">
                    <div class="carousel-caption">
                      <!-- <img
                        src="Images/sweet-roasted-makhana-kheer-indian-dessert-recipe-served-bowl-garnished-dry-fruits-tasty-made-using-foxnuts-188700295.jpg"
                      /> -->
                      <h3>Q. How To Control Noise Pollution?</h3>
                      <p>
                        There are many methods which help to control the noise
                        pollution. The source of noise must be reduced. The path
                        of transmission of sound must be stopped and the
                        receiver of noise must be safe guarded. The amount of
                        traffic must be reduced near the residential homes,
                        educational institutes and hospitals.
                      </p>
                    </div>
                  </div>

                  <div class="carousel-item">
                    <div class="carousel-caption">
                      <!-- <img
                        src="Images/sweet-roasted-makhana-kheer-indian-dessert-recipe-served-bowl-garnished-dry-fruits-tasty-made-using-foxnuts-188700295.jpg"
                      /> -->
                      <h3>Q. What Are The Effects Of Noise Pollution?</h3>
                      <p>
                        There are many side effects of the noise pollution. It
                        affects the general health and hearing power of the
                        human beings. The high intensity of noise and its
                        continued use can cause injury to the ears. It may lead
                        to the permanent loss of hearing. A large explosion can
                        cause the injury to tympanic membrane.
                      </p>
                    </div>
                  </div>

                  <div class="carousel-item">
                    <div class="carousel-caption">
                      <!-- <img
                        src="Images/sweet-roasted-makhana-kheer-indian-dessert-recipe-served-bowl-garnished-dry-fruits-tasty-made-using-foxnuts-188700295.jpg"
                      /> -->
                      <h3>Q. What Is Noise Pollution?</h3>
                      <p>
                        The noise pollution is defined as the unwanted sound
                        which is released into the environment. It disturbs the
                        human being and cause an adverse effect on the mental
                        and psychological well being. It is measured in the
                        units of decibels and is denoted by the dB. The noise
                        which is more than 115 dB is tolerant.
                      </p>
                    </div>
                  </div>

                  <div class="carousel-item">
                    <div class="carousel-caption">
                      <!-- <img
                        src="Images/sweet-roasted-makhana-kheer-indian-dessert-recipe-served-bowl-garnished-dry-fruits-tasty-made-using-foxnuts-188700295.jpg"
                      /> -->
                      <h3>Q. How To Control Radioactive Pollution?</h3>
                      <p>
                        The radioactive pollution can be controlled by number of
                        ways. It includes the stoppage of leakage from the
                        radioactive materials including the nuclear reactors,
                        industries and laboratories. The disposal of radioactive
                        material must be safe and secure. They must be stored in
                        the safe places and must be changed into harmless form.
                      </p>
                    </div>
                  </div>
                </div>
                <button
                  class="carousel-control-prev"
                  type="button"
                  data-bs-target="#carouselExampleCaptions"
                  data-bs-slide="prev"
                >
                  <span
                    class="carousel-control-prev-icon"
                    aria-hidden="true"
                  ></span>
                  <span class="visually-hidden">Previous</span>
                </button>
                <button
                  class="carousel-control-next"
                  type="button"
                  data-bs-target="#carouselExampleCaptions"
                  data-bs-slide="next"
                >
                  <span
                    class="carousel-control-next-icon"
                    aria-hidden="true"
                  ></span>
                  <span class="visually-hidden">Next</span>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Frequently Asked Questions Section-->

    <!-- Footer section -->
    <section id="contact" class="footer_wrapper mt-3 mt-md-0">
      <div class="container" style="padding-top: 60px">
        <div class="row align-items-center">
          <div class="col-lg-4 col-md-6 text-center text-md-start">
            <div class="footer-logo mb-3 mb-md-0">
              <!-- <img
                src="data:image/png;base64,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"
              /> -->
            </div>
          </div>
          <div class="col-lg-4 col-md-6">
            <ul
              class="list-unstyled d-flex justify-content-center justify-content-md-end justify-content-lg-center jus social-icon mb-3 mb-md-0"
            >
              <li>
                <a href="#"><i class="fab fa-instagram"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-facebook-f"></i> </a>
              </li>
              <li>
                <a href="#"><i class="fab fa-twitter"></i></a>
              </li>
              <li>
                <a href="#"><i class="fab fa-linkedin-in"></i> </a>
              </li>
            </ul>
          </div>
          <div class="col-lg-4 col-md-12">
            <div class="copyright-text text-lg-start text-center mb-3 mb-lg-0">
              <p class="mb-0">
                Copyright © 2023 <a href="#">Smart Pollution Tropper</a>. All
                Rights Reserved.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer section exit -->

    <!-- Bootstrap 5 JS CDN Links -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/2.9.2/umd/popper.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/5.1.0/js/bootstrap.min.js"></script>

    <!-- Custom Js Link -->
    <script>
      // Header Scroll
      let nav = document.querySelector(".navbar");
      window.onscroll = function () {
        if (document.documentElement.scrollTop > 20) {
          nav.classList.add("header-scrolled");
        } else {
          nav.classList.remove("header-scrolled");
        }
      };

      // nav hide
      let navBar = document.querySelectorAll(".nav-link");
      let navCollapse = document.querySelector(".navbar-collapse.collapse");
      navBar.forEach(function (a) {
        a.addEventListener("click", function () {
          navCollapse.classList.remove("show");
        });
      });
    </script>
  </body>
</html>
