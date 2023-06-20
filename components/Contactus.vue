<template>
 <div>
   
      <section class="contact">
        <div class="container">
          <!-- <h2>Contact Us</h2> -->
          <p class="info-contact">
            Please contact us via social media or by filling out the form below.
          </p>
          <div class="contact-box">
            <div>
              <p class="header-contact"><b>Contact Form </b></p>
            </div>

            <p class="header-desc">
              To contact us, please fill out the form below and include the
              contact hours.
            </p>
            <div class="contact-wrapper">
              <div class="contact-form">
                <form action="#" method="post">
                  <div class="column">
                    <div class="box-column">
                      <div class="box">
                        <label for="firstname">First Name</label>
                      </div>
                      <input type="text" name="firstname" id="firstname" />
                    </div>

                    <div class="box-column">
                      <div class="box">
                        <label for="lastname">Last Name</label>
                      </div>
                      <input type="text" name="lastname" id="lastname" />
                    </div>
                    <div class="box-column">
                      <div class="box">
                        <label for="email">Email</label>
                      </div>
                      <input type="email" name="email" id="email" />
                    </div>

                    <div class="box-column">
                      <div class="box">
                        <label for="phone">Phone Number</label>
                      </div>
                      <input type="tel" name="phone" id="phone" />
                    </div>
                  </div>
                  <div class="box-column">
                    <div class="box">
                      <label for="message">Messages</label>
                    </div>
                    <textarea name="message" id="message"></textarea>
                  </div>

                  <div class="submit-buttons">
                    <button type="submit" class="btn btn-secondary">Submit</button>
                  </div>
                </form>
              </div>
              <div class="line"></div>
              <div class="contact-info">
                <p>
                  Use the links below to contact us through our social media
                  platforms.
                </p>
                <div class="socials">
                  <ul class="social-links">
                    <li>
                      <a href=""
                        ><img
                          src="../assets/img/facebook2.svg"
                          alt=""
                        />https://www.facebook.com</a
                      >
                    </li>
                    <li>
                      <a href=""
                        ><img
                          src="../assets/img/youtube2.svg"
                          alt=""
                        />https://www.youtube.com</a
                      >
                    </li>
                    <li>
                      <a href=""
                        ><img
                          src="../assets/img/linkedin2.svg"
                          alt=""
                        />https://www.linkedin.com</a
                      >
                    </li>

                    <li>
                      <a
                        href="https://www.google.com/maps/dir//Moretech+industry+PLC,+Ethiopia,+Yeka+subcity+Woreda+07+COMOROS+STREET+Block+no+78%2F37,+Addis+Ababa,+Ethiopia/data=!4m6!4m5!1m1!4e2!1m2!1m1!1s0x164b8fbd21b0901b:0x8b85b87620e90d53?sa=X&ved=2ahUKEwjuqL7E1ff1AhVMSvEDHeQHDScQ48ADegQIAhBT"
                        ><span class="bold-spacing"> Location:</span> Gonder,
                        Ethiopia
                      </a>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="socials2">
              <ul class="social-links">
                <li>
                  <a href=""
                    ><img src="../assets/img/facebook2.svg" alt=""
                  /></a>
                </li>
                <li>
                  <a href=""><img src="../assets/img/youtube2.svg" alt="" /></a>
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/img/linkedin2.svg" alt=""
                  /></a>
                </li>
                <!-- <li>
                  <a href=""><img src="../assets/img/google2.svg" alt="" /></a>
                </li> -->
              </ul>
            </div>
          </div>
        </div>
      </section>
 </div>
  </template>
  
  <style></style>
  <script>
  import axios from "axios";
  import Footer from "../components/Footer.vue";
  export default {
    components: { Footer },
    mounted(){
       // Get a reference to the HTML form element
const form = document.querySelector('form');
console.log('form')
console.log(form)
// Add a listener to the submit event of the form
form.addEventListener('submit', (event) => {
  // Prevent the default form submission behavior 
  event.preventDefault();

  const firstname = document.querySelector('#firstname').value;
  const lastname = document.querySelector('#lastname').value;
  const email = document.querySelector('#email').value;
  const phone = document.querySelector('#phone').value;
  const message = document.querySelector('#message').value;

  // Create an object with the input values as properties
  const formData = {
    firstname,lastname,email,phone,message
  };

  // Log the form data to the console (for testing purposes)
  console.log(formData);
//  axios.post()
  // Submit the form using the submit() method on the form element
//   form.submit();
});
    }
  };
 
 
  </script>
  