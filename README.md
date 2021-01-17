<template>
  <div>
    <div
      id="dark-start"
      :style="{ backgroundColor: darkStartBackgroundColor }"
      :class="{ transition: darkStartTransition }"
    ></div>
    <div id="vanta" class="stationary-background"></div>
    <div class="container">
      <div class="full-title">
        <div class="profile">
          <img src="me.jpg" class="profile-pic" alt="Kayinajah Inyang" />
        </div>
        <h1
          id="typing-title"
          class="display-4"
          :style="{ zIndex: typingTitleZIndex, color: typingTitleColor }"
          @click="onTitleClick"
        >
          <span class="title">{{ titleText }}</span>
        </h1>
        <div>
          <span>
            <a href="#" @click="popupEmail">Email</a>
          </span>
          •
          <span>
            <a target="_blank" href="https://github.com/kayinajah/"
              >GitHub</a
            >
          </span>
          •
          <span>
            <a target="_blank" href="https://www.linkedin.com/in/kayinajah/"
              >LinkedIn</a
            >
          </span>
          <br />
          <span>
            <a target="_blank" href="https://www.facebook.com/"
              >Facebook</a
            >
          </span>
          •
          <span>
            <a target="_blank" href="https://open.spotify.com/user/1241777067"
              >Spotify</a
            >
          </span>
          •
          <span>
            <a target="_blank" href="https://www.last.fm/user/TankTan38"
              >Last.fm</a
            >
          </span>
          <listening />
        </div>
      </div>

      <div id="project-cards" :class="{ nonexistent: projectCardsNonexistent }">
        <div class="row">
          <div class="col-md-2"></div>
          <div class="col-md-8 card-col" style="justify-content: center;">
            <div class="card" style="width: 40em;">
              <div class="card-block">
                <div class="card-title" style="margin-top: 1.5em 0;">
                  <img
                    class="company-logo"
                    src="dss-dark.svg"
                    style="width: 9em; margin: .3em 0;"
                  />
                </div>
                <div class="row">
                  <div class="col-lg-6">
                    <div style="margin:1em;">
                      <h5 class="card-subtitle">App Developer</h5>
                      <div class="card-text">
                        Started October 2020 - Remote
                      </div>

                      <div class="card-buttons">
                        <button
                          type="button"
                          class="btn btn-outline-dark"
                          @click="popupDSSFull"
                        >
                          More Info
                        </button>
                      </div>
            </div>
          </div>
          <div class="col-md-2"></div>
        </div>

        <div class="row">
          <div class="col-md-4 card-col">
            <div class="card">
              <div class="card-block">
                <div class="card-title" style="margin-top: 8px;">
                  <img
                    class="company-logo"
                    src="gs-dark.svg"
                    @click="popupGS"
                  />
                </div>
                <br />
                <h5 class="card-subtitle">Referal Agent</h5>
                <div class="card-text">Dec 2020 - Remote</div>
                <div class="card-buttons">
                  <button
                    type="button"
                    class="btn btn-outline-dark"
                    @click="popupGS"
                  >
                    More Info
                  </button>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4 card-col">
            <div class="card">
              <div class="card-block">
                <div class="card-title" style="margin-top: 8px;">
                  <img
                    class="company-logo"
                    src="disney-parks-dark.svg"
                    @click="popupDisney"
                  />
                </div>
                <br />
                <h5 class="card-subtitle">App Developer</h5>
                <div class="card-text">Oct 2020 to Dec 2020 - Remote</div>
                <div class="card-buttons">
                  <button
                    type="button"
                    class="btn btn-outline-dark"
                    @click="popupDisney"
                  >
                    More Info
                  </button>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-4 card-col">
            <div class="card">
              <div class="card-block">
                <div class="card-title" style="margin-top: 8px;">
                  <img
                    class="company-logo"
                    src="espn-dark.svg"
                    @click="popupESPN"
                  />
                </div>
                <br />
                <h5 class="card-subtitle">App Developer</h5>
                <div class="card-text">Oct 2020 to Dec 2020 - Remote</div>
                <div class="card-buttons">
                  <button
                    type="button"
                    class="btn btn-outline-dark"
                    @click="popupESPN"
                  >
                    More Info
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div class="row">
          <div class="col-md-2"></div>
          <div class="col-md-8 card-col" style="justify-content: center;">
            <div class="card" style="width: 35em;">
              <div class="card-block">
                <div
                  class="card-title"
                  style="margin-top: -1.5em; margin-bottom: .4em;"
                >
                  <img
                    class="company-logo"
                    src="https://d2.alternativeto.net/dist/icons/krowser-web-services--app-store_181606.png?width=64&height=64&mode=crop&upscale=false"
                    style="max-height: 5em;"
                  />
                </div>
                <p class="card-text">
                  An android app store built with innovative technology for more speed, data saving, data privacy & more access to your favourite apps.
                </p>
                <div class="card-buttons">
                  <a href="https://kws.uk.to/" target="_blank">
                    <button type="button" class="btn btn-outline-dark">
                      Try it out
                    </button>
                  </a>
                  <a
                    href="https://github.com/"
                    target="_blank"
                  >
                    <button type="button" class="btn btn-outline-dark">
                      View on GitHub
                    </button>
                  </a>
                </div>
              </div>
            </div>
          </div>
          <div class="col-md-2"></div>
        </div>

        <div class="row">
          <project-card
            title="IITEDA Webinar and Conference App"
            left-button-href="https://play.google.com/store/apps/details?id=com.wIITEDAWebinarsandConferences_12632188"
            left-button-text="Dowlad the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
            rocketcrab="true"
          >
           The IITEDA Webinars & Conferences App provides easy access to relevant information about ongoing or upcoming IITEDA Webinars & Conferences. The app contains the Webinars & Conferences programme, abstracts, speaker profiles and other relevant information related to the Webinars & Conferences. The App also enables participants to rate each session and speaker. IITEDA (International Information Technology and Economic Development Association) is a research, development and innovation association that hosts ICITED (International Conference on Information Technology and Economic Development) often in collaboration with Universities and Working-life partners.
IITEDA and ICITED bring an array of participants and stakeholders from public and private sectors, academia, and professionals contributing towards constructive and sustainable development.
Available on the Google Play Store | Samsung Galaxy App Store
          </project-card>

          <project-card
            title="Krowser: Privacy Browser"
            left-button-href="https://play.google.com/store/apps/details?id=com.wKrowser_12664224"
            left-button-text="Download the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
            rocketcrab="true"
          >
            Krowser, a basic browser that respects your privacy, A basic web browser powered by Peekier, a new way to search the web. Peek through search results fast and securely on a search engine that respects your privacy. A privacy browser with only one feature, a search bar powered by Peekier. Website previews; Previews are generated on Peekier servers and sent to Krowser as a rendered image. Clicking on a result will maximize the preview and allow you to scroll through the website. You can then decide if the information displayed on the website interests you or not before clicking on the link.Strict privacy policy
We take your privacy very seriously. Peekier or Krowser does not log your passwords or track you throughout your browsing sessions.
          </project-card>
        </div>

        <div class="row">
          <project-card
            title="Your Feed News App and Aggregator"
            left-button-href="https://play.google.com/store/apps/details?id=com.wYourFeed_12349240"
            left-button-text="Download the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
          >
            Your Feed is a news app that offers a beautiful and light reading experience, build on RSS feeds from your favourite websites, news outlets and blogs. RSS ( Really Simple Syndication) is a web feed that allows users and applications to access updates to websites in a standardized, computer-readable format.
          </project-card>

          <project-card
            title="Your Transcription"
            left-button-href="http://bit.ly/yourtranscription"
            left-button-text="Order for Your Meetings"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
          >
           Your Transcription is an AI software that can transcribe live meetings.
           Just by inviting Your Transcription to a live meetings, it will provide transcription of the meeting and it will be sent to the provided email as soon as the meeting ends!
          </project-card>
        </div>
        <div class="row">
          <project-card
            title="Tip Calculator App"
            left-button-href="https://play.google.com/store/apps/details?id=com.wTipCalculator_12632147/"
            left-button-text="Download the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
          >
          This Ultra-light Tip Calculator App Help To Calculate Quickly The Amount Of Tip Base On The Percentage!
           </project-card>
          <project-card
            title="Your Basic Expense Reporter AI"
            left-button-href="https://galaxy.store/YBER/"
            left-button-text="Download the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
          >
             Your Basic Expense Reporter automates expense management. It dramatically reduces the time required to record receipt with the receipt scanning technology just by taking a picture of a receipt the built-in AI software captures the details and automatically records it!
          </project-card>
        </div>

        <div class="row">
          <project-card
            title="Stay Safe Watch Face"
            left-button-href="https://www.facer.io/watchface/T9qHcNYclu?watchModel=ticwatchexpress/"
            left-button-text="Sync to your watch face"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
            rocketcrab="true"
          >
            For the Wear OS & Tizen Smart Watches! 
          </project-card>

          <project-card
            title="Ekemini and Michael Wedding App"
            left-button-href="https://play.google.com/store/apps/details?id=com.wEkeminiandMichaelWeddingApp_12721876/"
            left-button-text="Download the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
          >
           All relevant information about Ekemini & Michael Wedding on 5th December 2020. This wedding app provides attendees with relevant information about Ekemini & Michael Wedding on 5th December 2020
          </project-card>
        </div>

        <div class="row">
          <project-card
            title="COVID-19 Information Resources - Nigeria (Web App & Mobile App)"
            left-button-href="https://covid19nigeria.glideapp.io/"
            left-button-text="Download the App"
            right-button-href="https://github.com/"
            right-button-text="View on GitHub"
          >
           A COVID-19 Information Resources Mobile App for Nigeria. As the Coronavirus pandemic resurges, the is a massive need of Information about the pandemic as most of the facts have changed. The app is building built in Collaboration with Aniebiet I. Ntui, a Professor of Library and Information Science at the University of Calabar, Nigeria.
          </project-card>
        </div>

        <br />
        <footer>
          Kayinajah Inyang,
          <span id="footer-year">{{ year }}</span>
          <br />
          <a
            href="https://github.com/kayinajah/kayinajah"
            target="_blank"
            >View on GitHub</a
          >
        </footer>
      </div>
    </div>
    <!-- /.container -->
  </div>
</template>

<script>
import Cookies from 'js-cookie'
import Typed from 'typed.js'
import Swal from 'sweetalert2'
import Listening from '~/components/Listening.vue'
import ProjectCard from '~/components/ProjectCard.vue'
const Popup = Swal.mixin({
  confirmButtonColor: '#a42e05'
})
export default {
  components: { Listening, ProjectCard },
  data: () => ({
    year: new Date().getFullYear(),
    titleText: '',
    typingTitleZIndex: () => 100,
    typingTitleColor: () => 'white',
    projectCardsNonexistent: true,
    darkStartBackgroundColor: '#212529',
    darkStartTransition: false
  }),
  mounted() {
    const shouldPlayAnimation = !(Cookies.get('typed') === 'true')
    const sixteenHours = 16 / 24
    Cookies.set('typed', 'true', { expires: sixteenHours })
    if (shouldPlayAnimation) {
      // start the title above the shadow, and as white text
      this.typingTitleZIndex = 100
      this.typingTitleColor = 'white'
      // execute the animation
      new Typed('.title', {
        strings: ['Kayinajah Inyang'],
        typeSpeed: 100,
        onComplete: () => {
          // wait a bit, then show the page
          setTimeout(() => this.showPage(), 300)
        }
      })
    } else {
      // forgo the animation, and just show the page
      this.titleText = 'Kayinajah Inyang'
      this.showPage()
    }
  },
  methods: {
    showPage() {
      // make the elements take up space by removing
      // display: none, without removing opacity 0
      this.projectCardsNonexistent = false
      // get rid of the solid color covering the page
      this.darkStartBackgroundColor = 'transparent'
      // invert title text color
      this.typingTitleColor = '#212529'
      // begin the circle transition
      this.darkStartTransition = true
    },
    popupEmail() {
      Popup.fire({
        title: 'Email me!',
        html:
          '<div style="color: #a42e05; text-align:center;"><a href="mailto:emailyourfeed@gmail.com">emailyourfeed@gmail.com</a></div>'
      })
    },
    popupESPN() {
      const innerHTML =
        'As an App Developer, I am responsible for creating mobile apps for the Samsung Galaxy App Store.'
      Popup.fire({
        html: innerHTML,
        imageUrl: 'https://i.imgur.com/aYKfZ62.jpg'
      })
    },
    popupDisney() {
      const innerHTML =
        '<p>'As an App Developer, I am responsible for creating mobile apps for the Samsung Galaxy App Store.
        '</p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: 'https://bestmobs.com/html/uploads/Samsungs-new-Silicon-Valey-office.jpg'
      })
    },
    popupGS() {
      const innerHTML =
        '<p>'As a Referral Agent, I am to help Developer Economics to reach more developers across the world and increase awareness about Developer Economics surveys!
        '</p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: 'https://developereconomics.com/static/a0a92776290917d6628e1f299aa90294/c076d/logo.png'
      })
    },
    popupDSSIntern() {
      const innerHTML =
        '<p>For my fourth and final internship, I spent my fall semester ' +
        'at Disney Streaming Services in NYC for the launch of Disney+. ' +
        'I joined the Web Platform Architecture team, which manages ' +
        'the servers for disneyplus.com on AWS. I also created an internal ' +
        'tool with Next.js and React to quickly find and view information ' +
        'about any microservice in the company.' +
        '</p>'
      Popup.fire({
        html: innerHTML,
        imageUrl: 'https://i.imgur.com/dmIzkPU.png'
      })
    },
    popupDSSFull() {
      const innerHTML =
        '<p>After graduating in May 2020, I returned to Disney Streaming ' +
        'Services as a full-time software engineer. I onboarded and work ' +
        'remotely due to the COVID-19 pandemic.' +
        '</p>'
      Popup.fire({
        html: innerHTML
      })
    },
    onTitleClick() {
      if (this.projectCardsNonexistent) {
        // forgo the animation, and just show the page
        this.titleText = 'Tanner Krewson'
        this.showPage()
      } else {
        this.popupReplayAnimation()
      }
    },
    popupReplayAnimation() {
      Popup.fire({
        title: 'Want to see the typing intro animation again?',
        type: 'question',
        showCancelButton: true,
        confirmButtonText: 'Yes',
        cancelButtonText: 'No'
      }).then((result) => {
        if (result.value) {
          Cookies.set('typed', 'false')
          location.reload()
        }
      })
    }
  }
}
</script>

<style>
/*
 *	Main
 */
body {
  padding-bottom: 2rem;
  color: #212529;
  text-align: center;
}
.gradient-background {
  background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}
.stationary-background {
  background: #a42e05;
  background-repeat: no-repeat;
  width: 100%;
  top: -80px;
  bottom: -80px;
  position: fixed;
  z-index: -1;
}
#dark-start {
  opacity: 1;
  position: fixed;
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  z-index: 1;
  pointer-events: none;
}
#dark-start:before {
  content: '';
  position: fixed;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  border-radius: 100%;
  animation-duration: 1s;
  box-shadow: 0px 0px 0px 100vmax #212529;
  width: 150vmax;
  height: 150vmax;
}
.transition:before {
  animation-name: spotlight;
}
.nonexistent {
  display: none;
}
@keyframes spotlight {
  from {
    width: 0vmin;
    height: 0vmin;
  }
  to {
    width: 150vmax;
    height: 150vmax;
  }
}
/*
 *	Header
 */
.full-title {
  padding-top: 0.5rem;
  padding-bottom: 1rem;
  font-size: 1.1rem;
}
.profile {
  display: inline-block;
  margin: 1rem 0;
}
.profile-pic {
  height: 130px;
  border-radius: 50%;
}
.breathe::before {
  content: '';
  position: absolute;
  z-index: -1;
  height: 130px;
  width: 130px;
  border-radius: 50%;
  box-shadow: inset 0 0 0 16px rgba(0, 0, 0, 0.3);
  animation: breathe 16s infinite;
}
@keyframes breathe {
  from,
  75%,
  to {
    transform: scale(1, 1);
  }
  25%,
  50% {
    transform: scale(1.25, 1.25);
  }
}
.full-title a,
a:active,
a:visited {
  display: inline-block;
  color: #212529;
  transition: all 0.2s ease-in-out;
}
a:hover {
  transform: scale(1.05);
}
body {
  font-family: 'Jost', sans-serif;
  font-weight: 400;
}
.full-title .display-4 {
  font-family: 'Jost', sans-serif;
  font-weight: 500;
  font-size: 2.5em;
}
span.avoidwrap {
  display: inline-block;
}
#typing-title {
  position: relative;
  margin-bottom: 12px;
  transition: all 0.2s ease-in;
}
.company-logo {
  max-width: 62.5%;
  max-height: 105px;
}
/* fix line appearing between buttons */
.card a:hover {
  color: transparent;
}
.card-buttons {
  margin-top: 0.8em;
}
.btn-outline-dark {
  color: #212529;
  border-color: #212529;
  margin-bottom: 0.3em;
}
/*
 *	SweetAlert
 */
#swal2-content {
  text-align: left;
  font-weight: normal;
}
#swal2-content a {
  color: #45c299;
}
#swal2-content a:hover {
  text-decoration: underline;
}
.swal2-image {
  margin-top: -1.25em;
  margin-left: -1.25em;
  max-width: calc(100% + 2.5em);
  border-radius: 5px 5px 0px 0px;
}
/*
 *	Typed.js
 */
.typed-cursor {
  opacity: 1;
  -webkit-animation: blink 0.7s infinite;
  -moz-animation: blink 0.7s infinite;
  animation: blink 0.7s infinite;
}
@keyframes blink {
  0% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
