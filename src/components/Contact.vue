<script>
  import emailjs from "emailjs-com";

  export default {
    data() {
      return {
        contact_info: {
          name: "",
          email: "",
          subject: "",
          message: ""
        }
      }
    },

    methods: {
      sendEmail(e) {
        try {
          emailjs.sendForm("service_qva8heg", "template_rprmiwf", e.target, "rnRdJdjo2ks7ipfQ-", {
            name: this.contact_info.name,
            email: this.contact_info.email,
            message: this.contact_info.message,
            subject: this.contact_info.subject
          })
          alert("OK")
        } catch(err) {
          console.log(err)
        }
        this.contact_info.name = ""
        this.contact_info.email = ""
        this.contact_info.message = ""
        this.contact_info.subject = ""
      }
    }
  }
</script>

<template>
  <div class="min-h-screen text-slate-100" id="contact">
    <div>
      <h1 class="text-center text-2xl sm:text-5xl p-5">Contact</h1>
    </div>
    <div class=" md:flex md:justify-center">
      <div class="md:w-1/2 md:flex md:flex-row md:items-center md:justify-center">
        <form class="md:w-4/5  flex flex-col m-3 p-10 bg-slate-600 shadow-lg shadow-slate-900 rounded-md" @submit.prevent="sendEmail">
          <h3 class="font-semibold text-lg">Contact form</h3>

          <div class="my-2">
            <label for="fullname">Full Name</label>
            <input 
              type="text" 
              name="name" 
              id="name"
              class="px-4 py-3 w-full bg-slate-700 border-2 border-slate-500 outline-none rounded-md"
              placeholder="Your fullname"
              required
              v-model="contact_info.name"
            />
          </div>

          <div class="my-2">
            <label for="email">Email</label>
            <input 
              type="email" 
              name="email" 
              id="email"
              class="px-4 py-3 w-full bg-slate-700 border-2 border-slate-500 outline-none rounded-md"
              placeholder="Your Email" 
              v-model="contact_info.email"
            />
          </div>

          <div class="my-2">
            <label for="subject">Subject</label>
            <input 
              type="text" 
              name="subject" 
              id="subject" 
              class="px-4 py-3 w-full bg-slate-700 border-2 border-slate-500 outline-none rounded-md"
              placeholder="Subject"  
              v-model="contact_info.subject"
            />
          </div>

          <div class="my-2">
            <label for="message">Message</label>
            <textarea 
              name="message" 
              id="message"
              class="px-4 py-3 w-full bg-slate-700 border-2 border-slate-500 outline-none h-32 rounded-md"
              v-model="contact_info.message"
            ></textarea>
          </div>
          
          <div class="my-2">
            <button class="px-4 py-3 bg-teal-400 rounded-md">Send Message</button>
          </div>
        </form>
      </div>
      <div class="md:w-1/2">
        <div class="m-10">
          <h3 class="font-semibold text-xl">Contact details</h3>

          <ul class="text-sm md:text-lg m-5">
            <li><i class="fa fa-map-marker m-2" aria-hidden="true"></i> Betongolo, Tananarivo, Madagascar</li>
            <li><i class="fa fa-envelope m-2"></i> avonasandratra2003@gmail.com</li>
            <li><i class="fa fa-phone m-2"></i> +261340133099</li>
          </ul>

          <div class="flex flex-wrap items-center justify-center">
            <div class="m-2 bg-slate-700 p-2 border-2 border-slate-600 rounded-md">
              <a href="https://github.com/Nasan01" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-github fa-3x"></i>
              </a>
            </div>
            <div class="m-2 bg-slate-700 p-2 border-2 border-slate-600 rounded-md">
              <a href="https://www.linkedin.com/in/avonasandratra-ramaroson-a38a05200/" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-linkedin fa-3x"></i>
              </a>
            </div>
            <div class="m-2 bg-slate-700 p-2 border-2 border-slate-600 rounded-md">
              <a href="https://www.facebook.com/nasandratra.nits" target="_blank" rel="noopener noreferrer">
                <i class="fab fa-facebook fa-3x"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <footer class="p-14 bg-slate-900">
      <h1 class="text-center text-sm"><i>Thanks for visiting my portfolio <i class="fa fa-smile"></i></i></h1>      
    </footer>
  </div>
</template>
