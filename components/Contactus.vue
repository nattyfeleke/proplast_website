<template>
 <div>
   <div class="notification not-visible " id="notification">
    <div id='msg-sent' class="msg-sent hidden">
      <div class="tick">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"><g stroke-width="0" id="SVGRepo_bgCarrier"></g><g stroke-linejoin="round" stroke-linecap="round" id="SVGRepo_tracerCarrier"></g><g id="SVGRepo_iconCarrier"> <path stroke-linejoin="round" stroke-linecap="round" stroke-width="1.5" stroke="#fff" d="M20 7L9.00004 18L3.99994 13"></path> </g></svg>
      </div> 
    <h4 class="notfication-text">Email Sent</h4> 
    </div>
    <div id='msg-notsent' class="msg-notsent hidden">
      <div class="warn">
        <svg aria-hidden="true" stroke="white" stroke-width="1.5" viewBox="0 0 24 24" fill="none">
                <path d="M12 9v3.75m-9.303 3.376c-.866 1.5.217 3.374 1.948 3.374h14.71c1.73 0 2.813-1.874 1.948-3.374L13.949 3.378c-.866-1.5-3.032-1.5-3.898 0L2.697 16.126zM12 15.75h.007v.008H12v-.008z" stroke-linejoin="round" stroke-linecap="round"></path>
              </svg>
      </div> 
    <h4 class="notfication-text">Couldn't send message. Please try again!</h4> 
    </div>
   </div>
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
                      <input type="text" name="firstname" id="firstname" required/>
                    </div>

                    <div class="box-column">
                      <div class="box">
                        <label for="lastname">Last Name</label>
                      </div>
                      <input type="text" name="lastname" id="lastname" required/>
                    </div>
                    <div class="box-column">
                      <div class="box">
                        <label for="email">Email</label>
                      </div>
                      <input type="email" name="email" id="email" required/>
                    </div>

                    <div class="box-column">
                      <div class="box">
                        <label for="phone">Phone Number</label>
                      </div>
                      <input type="tel" name="phone" id="phone" required/>
                    </div>
                  </div>
                  <div class="box-column">
                    <div class="box">
                        <label for="subject">Subject</label>
                      </div>
                      <input type="text" name="subject" id="subject" required />
                  </div>
                  <div class="box-column">
                    <div class="box">
                      <label for="message">Messages</label>
                    </div>
                    <textarea name="message" id="message" required></textarea>
                  </div>

                  <div class="submit-buttons">
                    <button type="submit" class="btn btn-secondary" id="submitmessage">Submit
                     
                    </button>
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
form.addEventListener('submit', async(event) => {
  console.log('button clicked')
  // Prevent the default form submission behavior 
  event.preventDefault();
  const notification = document.querySelector('#notification');
  const sentMsg = document.querySelector('#msg-sent');
  const notsentMsg = document.querySelector('#msg-notsent');
  const submitMsgBtn = document.querySelector('#submitmessage');
  const firstname = document.querySelector('#firstname').value;
  const lastname = document.querySelector('#lastname').value;
  const email = document.querySelector('#email').value;
  const phone = document.querySelector('#phone').value;
  const subject = document.querySelector('#subject').value;
  const message = document.querySelector('#message').value;

  const formData = {
    firstname,lastname,email,phone,subject,message
  };

  console.log(formData);
  submitMsgBtn.textContent='Submitting...';
  submitMsgBtn.disabled=true;
  submitMsgBtn.classList.add('btn-disabled');
  try {
   const res = await axios.post('https://report.proplast.et/email/', formData);
 console.log(res); 
 if(res.status=='200'){
  console.log('success')
  //clear the form input fields
  document.querySelector('#firstname').value='';
  document.querySelector('#lastname').value='';
  document.querySelector('#email').value='';
  document.querySelector('#phone').value='';
  document.querySelector('#subject').value='';
  document.querySelector('#message').value='';
  submitMsgBtn.textContent='Submit Message';
  submitMsgBtn.disabled=false;
  submitMsgBtn.classList.remove('btn-disabled');
  notification.classList.remove('not-visible');
  notification.classList.add('notification-success');
  sentMsg.classList.remove('hidden');
  setTimeout(() => {
    notification.classList.add('not-visible');
    notification.classList.remove('notification-success');    
    sentMsg.classList.add('hidden');
  }, 3000);
 }else{
   console.log('Message not sent')
   submitMsgBtn.textContent='Submit';
   submitMsgBtn.disabled=false;
   submitMsgBtn.classList.remove('btn-disabled');
  notification.classList.remove('not-visible');
  notification.classList.add('notification-error');
  notsentMsg.classList.remove('hidden');
  setTimeout(() => {
    notification.classList.add('not-visible');
    notification.classList.remove('notification-error');    
    notsentMsg.classList.add('hidden');
  }, 3000);

 }
  } catch (error) {
    console.log('Message not sent')
   submitMsgBtn.textContent='Submit';
   submitMsgBtn.disabled=false;
   submitMsgBtn.classList.remove('btn-disabled');
  notification.classList.remove('not-visible');
  notification.classList.add('notification-error');
  notsentMsg.classList.remove('hidden');
  setTimeout(() => {
    notification.classList.add('not-visible');
    notification.classList.remove('notification-error');    
    notsentMsg.classList.add('hidden');
  }, 3000);
  }
 


  console.log('msg sent')

});
    }
  };
 
 
  </script>
  