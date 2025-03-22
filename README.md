<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Accounting Solution Lab</title>
  <style>
    /* Global Styles */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      color: #333;
      background-color: #f4f4f4;
    }

    .container {
      width: 80%;
      margin: 0 auto;
      max-width: 1200px;
    }

    h1, h2, h3 {
      color: #2c3e50;
    }

    a {
      text-decoration: none;
      color: #2980b9;
    }

    .cta-btn {
      background-color: #2980b9;
      color: white;
      padding: 10px 20px;
      text-align: center;
      display: inline-block;
      border-radius: 5px;
    }

    .cta-btn:hover {
      background-color: #3498db;
    }

    /* Header */
    header {
      background-color: #2c3e50;
      padding: 20px 0;
      color: white;
      text-align: center;
      opacity: 0;
      transform: translateY(-20px);
      animation: fadeInDown 1s forwards;
    }

    header nav ul {
      list-style-type: none;
      margin: 0;
      padding: 0;
      display: flex;
      justify-content: center;
    }

    header nav ul li {
      margin-left: 20px;
    }

    header nav ul li a {
      color: white;
      font-size: 16px;
    }

    /* Typing Animation for Website Name */
    h1 {
      font-size: 48px;
      color: white;
      text-align: center;
      font-weight: bold;
      overflow: hidden;
      white-space: nowrap;
      width: 0;
      animation: typing 3s steps(30) 1s forwards, blink 0.75s step-end infinite;
    }

    /* Typing Effect */
    @keyframes typing {
      to {
        width: 100%;
      }
    }

    /* Cursor Blinking Effect */
    @keyframes blink {
      50% {
        border-color: transparent;
      }
    }

    /* About Section */
    .about {
      padding: 60px 0;
      text-align: center;
      position: relative;
      background-image: url('https://test.onlinevidyalaya.net//Content/9931/TempImageRepository/TemplateImage_03222025030340780911PM.jpg');
      background-size: cover;
      background-position: center;
      color: white;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 1s 0.5s forwards;
    }

    /* Overlay */
    .about::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.4);
      z-index: 1;
    }

    .about h2, .about p {
      animation: blink 1.5s linear infinite;
    }

    .about h2 {
      font-size: 36px;
      color: white;
      text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
      z-index: 2;
      position: relative;
    }

    .about p {
      font-size: 18px;
      max-width: 800px;
      margin: 0 auto;
      text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
      z-index: 2;
      position: relative;
    }

    /* Services Section */
    .services {
      padding: 60px 0;
      background-color: #fff;
      text-align: center;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 1s 1s forwards;
    }

    .services h2 {
      font-size: 36px;
      animation: blink 2s linear infinite;
    }

    .service {
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 1s ease-in-out forwards;
    }

    .service h3 {
      font-size: 24px;
      margin-bottom: 10px;
      animation: blink 2s linear infinite;
    }

    .service p {
      font-size: 18px;
      max-width: 800px;
      margin: 0 auto;
    }

    .service img {
      width: 100%;
      max-width: 400px;
      margin-top: 30px;
      opacity: 0;
      transform: translateY(20px);
      animation: fadeInUp 1s ease-in-out forwards;
    }

    /* Animations */
    @keyframes fadeInDown {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes fadeInUp {
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Blinking Effect */
    @keyframes blink {
      0%, 100% {
        opacity: 1;
      }
      50% {
        opacity: 0;
      }
    }

    /* Testimonials Section */
    .testimonials {
      padding: 60px 0;
      background-color: #f9f9f9;
      text-align: center;
    }

    .testimonials h2 {
      font-size: 36px;
      color: #2c3e50;
      margin-bottom: 30px;
    }

    .testimonial {
      max-width: 800px;
      margin: 0 auto;
      background-color: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
      margin-bottom: 30px;
    }

    .testimonial p {
      font-size: 18px;
      color: #555;
      margin-bottom: 10px;
    }

    .testimonial span {
      font-weight: bold;
      color: #2980b9;
    }

    /* Contact Section */
    .contact {
      padding: 60px 0;
      background-color: #f9f9f9;
      text-align: center;
    }

    .contact h2 {
      font-size: 36px;
      color: #2c3e50;
    }

    .contact form {
      max-width: 600px;
      margin: 0 auto;
      text-align: left;
      background-color: white;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    }

    .contact label {
      display: block;
      margin-bottom: 10px;
      font-size: 16px;
    }

    .contact input, .contact textarea {
      width: 100%;
      padding: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 16px;
    }

    .contact button {
      background-color: #2980b9;
      color: white;
      padding: 10px 20px;
      font-size: 16px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    .contact button:hover {
      background-color: #3498db;
    }

    /* Footer Section */
    footer {
      background-color: #2c3e50;
      color: white;
      padding: 20px 0;
      text-align: center;
    }

    footer p {
      margin: 0;
      animation: blink 2s linear infinite;
    }

  </style>
</head>
<body>

  <!-- Header Section -->
  <header>
    <div class="container">
      <h1>Accounting Solution Lab</h1>
      <nav>
        <ul>
          <li><a href="#about">About Us</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#testimonials">Testimonials</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- About Section -->
  <section class="about" id="about">
    <div class="container">
      <h2>About Us</h2>
      <p>At Accounting Solution Lab, we provide expert accounting services tailored to meet your business's needs. Our team of professionals is dedicated to simplifying your financial processes, offering accurate and timely accounting solutions to help you grow your business.</p>
      <img src="https://via.placeholder.com/400x250" alt="About Us">
    </div>
  </section>

  <!-- Services Section -->
  <section class="services" id="services">
    <div class="container">
      <h2>Our Services</h2>

      <div class="service">
        <h3>Accounting Services</h3>
        <p>We offer full accounting services, including bookkeeping, financial reporting, tax preparation, and financial analysis to ensure your business stays on track.</p>
        <img src="https://test.onlinevidyalaya.net//Content/9931/TempImageRepository/TemplateImage_03222025033637748084PM.jpg">
      </div>

      <div class="service">
        <h3>Tax Advisory</h3>
        <p>Our tax advisory services help your business navigate complex tax laws, ensuring you maximize deductions and minimize liabilities.</p>
        <img src="https://test.onlinevidyalaya.net//Content/9931/TempImageRepository/TemplateImage_03222025033720348871PM.jpg">
      </div>

      <div class="service">
        <h3>Financial Planning</h3>
        <p>Our financial planning services help you strategically manage your business finances for long-term growth and stability.</p>
        <img src="https://test.onlinevidyalaya.net//Content/9931/TempImageRepository/TemplateImage_03222025033659291795PM.jpg">
      </div>

      <div class="service">
        <h3>Business Consulting</h3>
        <p>We provide business consulting services to optimize your business operations, strategies, and financial performance.</p>
        <img src="https://via.placeholder.com/400x250" alt="Business Consulting">
      </div>

      <div class="service">
        <h3>Audit Services</h3>
        <p>Our audit services help businesses ensure financial accuracy, transparency, and compliance with regulations.</p>
        <img src="https://via.placeholder.com/400x250" alt="Audit Services">
      </div>
    </div>
  </section>

  <!-- Testimonials Section -->
  <section class="testimonials" id="testimonials">
    <div class="container">
      <h2>What Our Clients Say</h2>
      <div class="testimonial">
        <p>"Accounting Solution Lab has helped our business with all our accounting needs. Their team is professional, reliable, and always provides timely financial reports."</p>
        <span>- John Doe, CEO of ABC Corp</span>
      </div>
      <div class="testimonial">
        <p>"The tax advisory services were a lifesaver! They saved us a significant amount of money by helping us navigate complex tax laws. Highly recommend!"</p>
        <span>- Jane Smith, Founder of XYZ Enterprises</span>
      </div>
    </div>
  </section>

    <!-- Contact Section -->
  <section class="contact" id="contact">
    <div class="container">
      <h2>Contact Us</h2>
      <form action="sendemail.php" method="post">
        <label for="name">Your Name:</label>
        <input type="text" id="name" name="name" required>

        <label for="email">Your Email:</label>
        <input type="email" id="email" name="email" required>

        <label for="message">Your Message:</label>
        <textarea id="message" name="message" rows="4" required></textarea>

        <button type="submit">Submit</button>
      </form>
    </div>
  </section>

