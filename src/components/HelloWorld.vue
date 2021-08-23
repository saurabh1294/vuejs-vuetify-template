<template>
	<div id="app">
		<v-app>
			<v-content class="ma-10 pa-10">
				<v-row class="header">
					<v-col md="1" class="test">
						<v-img
							class="mx-2"
							src="https://www.tafensw.edu.au/o/mrkt-2-theme/images/logos/tafe-nsw-logo-white.svg"
							max-height="150"
							max-width="150"
							contain
							></v-img>
					</v-col>
					<v-col md="10" class="beta">
						BETA
					</v-col>
					<v-col md="1" class="test">
						<v-btn icon style="color:white">
							<v-icon>mdi-magnify</v-icon>
						</v-btn>
					</v-col>
				</v-row>
				<hr/>
				<v-row class="header">
					<v-col md="11" class="menu">
						<span
							v-for="item in nav"
							:key="item.icon"
							to="#"
							:title="item.title"
							flat
							style="padding:20px;">{{ item.title }}</span>
					</v-col>
					<v-col md="1" class="text-left test menu">
						<span style="margin-right:5px"> Shortlist </span>
						<v-badge
							color="red"
							content="3"
							style="margin-top:7px"
							>
						</v-badge>
					</v-col>
				</v-row>
				<v-row class="breadcrumbs">
					<v-col md="1" class="icon-home-container">
						<i class="fas fa-home"></i>
					</v-col>
					<v-col md="11" class="menu">
						<div class="breadcrumbs-container">
							<v-breadcrumbs :items="items">
								<template v-slot:divider>
									>
								</template>
								<template v-slot:item="{ item }">
									<v-breadcrumbs-item :disabled="item.disabled">
										<span class="breadcrumbs-item">
										<a href="#">{{ item.text }}</a>
										</span>
									</v-breadcrumbs-item>
								</template>
							</v-breadcrumbs>
						</div>
					</v-col>
				</v-row>
				<v-row class="banner">
					<v-col md="6" class="course-banner">
						<span>NATIONAL COURSE CODE: HLT54115</span>
						<span class="diploma-text">DIPLOMA OF NURSING</span>
						<span class="button-ask-question">
							<v-btn id="ask-question">
								<v-icon dark left></v-icon>
								ASK A QUESTION
							</v-btn>
							<v-btn id="location-btn">
								<v-icon left></v-icon>
								FIND A LOCATION TO ENROL
							</v-btn>
						</span>
					</v-col>
					<v-col md="6" >
						<img class="img-banner" 
							src="../assets/banner-half.png"/>
					</v-col>
				</v-row>
				<v-row>
					<v-col md="12">
						<div class="content-container-left">PATHWAYS</div>
					</v-col>
					<v-col md="12">
						<div class="future-heading">FUTURE CAREER AND STUDY OPTIONS</div>
					</v-col>
				</v-row>
				<hr class="underline"/>
				<v-row>
					<v-col md="12">
						<div class="content-container-left">Career pathways</div>
					</v-col>
					<v-col md="12">
						<div>Our graduates go on to roles like:</div>
					</v-col>
				</v-row>
				<v-row no-gutters>
					<v-col
						cols="6"
						md="4"
						>
						<v-card
							class="pa-2"
							outlined
							tile
							>
							.col-12 .col-sm-6 .col-md-8
						</v-card>
					</v-col>
					<v-col
						cols="12"
						sm="6"
						md="8"
						>
						<v-card
							class="pa-2"
							outlined
							tile
							>
							.col-6 .col-md-4
						</v-card>
					</v-col>
				</v-row>
				<v-row>
					<v-col md="12">
						<div class="content-container-left">Other jobs include: Other, Another and third one</div>
					</v-col>
					<v-col md="12">
						<div class="content-container-left">Licensing</div>
					</v-col>
					<v-col md="12">
						<p>You need to be a registered practitioner to apply for jobs in the industry.Completion of an NMBA approved diploma of</p>
						<p>Nursing program will make you eligible to apply to the NMBA for registration as an enrolled nurse.For more information</p>
						<p><a href="https://www.nursingmidwiferyboard.gov.au/Registration-and-Endorsement.aspx">
							visit https://www.nursingmidwiferyboard.gov.au/Registration-and-Endorsement.aspx</a>
						</p>
					</v-col>
				</v-row>
				<v-row>
					<v-col md="12">
						<div class="content-container-left">Study pathways</div>
					</v-col>
					<v-col md="12">
						<div>Take your study further with other courses offered at TAFE NSW:</div>
					</v-col>
				</v-row>
				<v-row>
					<v-col md="4">
						<v-card
							class="pa-2"
							outlined
							tile
							>
							<div class="card-prev-study">TEST1</div>
						</v-card>
					</v-col>
					<v-col md="4">
						<v-card
							class="pa-2"
							outlined
							tile
							>
							<div class="card-further-study">TEST2</div>
						</v-card>
					</v-col>
					<v-col md="4">
						<v-card
							class="pa-2"
							outlined
							tile
							>
							<div class="card-related-study">TEST3</div>
						</v-card>
					</v-col>
				</v-row>
				<v-row>
					<v-col md="12">
						<div class="content-container-left">Your experience counts</div>
					</v-col>
					<v-col md="12">
						<p>At TAFE NSW, we recognise your previous study and work experience. You can apply for recognition of prior learning or a</p>
						<p>credit transfer with any of our four courses. If you're successful you will get your qualification faster.</p>
					</v-col>
				</v-row>
				<v-content class="footer-container">
					<v-row>
						<v-col md="10">
							<v-img
								class="mx-2"
								src="https://www.tafensw.edu.au/o/mrkt-2-theme/images/logos/tafe-nsw-logo-white.svg"
								max-height="150"
								max-width="150"
								contain
								></v-img>
						</v-col>
						<v-col md="1">
							131 601
						</v-col>
						<v-col md="1">
							Contact Us
						</v-col>
					</v-row>
					<hr/>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Use of services</a>
						</v-col>
						<v-col md="3">
							<a href="#">Vet student loans</a>
						</v-col>
						<img src="../assets/tafe-abor-banner.png" class="tafe-abor-banner"/>
					</v-row>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Agency information guide</a>
						</v-col>
						<v-col md="3">
							<a href="#">Recognition and credit transfer</a>
						</v-col>
						<v-col md="6">
						</v-col>
					</v-row>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Smart and skilled</a>
						</v-col>
						<v-col md="3">
							<a href="#">Withdrawals and refunds</a>
						</v-col>
						<v-col md="6">
						</v-col>
					</v-row>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Student rights and responsibilities</a>
						</v-col>
						<v-col md="3">
							<a href="#">Agency information guide</a>
						</v-col>
						<v-col md="6">
						</v-col>
					</v-row>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Policies and procedures</a>
						</v-col>
						<v-col md="5">
							<a href="#">Corporate</a>
						</v-col>
						<v-col md="4">
							Registered traning Organisation 90003
						</v-col>
					</v-row>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Complaints and feedback</a>
						</v-col>
						<v-col md="5">
							<a href="#">Higher education corporate governance</a>
						</v-col>
						<v-col md="4">
							CRICOS Provider Number 00591E
						</v-col>
					</v-row>
					<v-row class="footer-link-row">
						<v-col md="3">
							<a href="#">Fees</a>
						</v-col>
						<v-col md="5">
							<a href="#">Payment and funding</a>
						</v-col>
						<v-col md="4">
							Higher education provider PRV 12049
						</v-col>
					</v-row>
				</v-content>
				<v-content class="footer-bottom dark">
					<v-row>
						<v-col md="10">
							<span class="footer-bottom-text-disclaimer"><a href="#">Disclaimer</a></span>
							<span class="footer-bottom-text-privacy"><a href="#">Privacy</a></span>
						</v-col>
						<v-col md="2">
							© TAFE NSW 2021
						</v-col>
					</v-row>
				</v-content>
			</v-content>
		</v-app>
	</div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'HelloWorld',

  props: [
    'msg'
  ],

  data: () => ({
    items: [
        {
          text: 'Course Areas',
          disabled: false,
          href: 'breadcrumbs_dashboard',
        },
        {
          text: 'Healthcare',
          disabled: false,
          href: 'breadcrumbs_link_1',
        },
        {
          text: 'Nursing',
          disabled: false,
          href: 'breadcrumbs_link_2',
        },
        {
          text: 'Diploma of Nursing',
          disabled: false,
          href: 'breadcrumbs_link_2',
        },
    ],
    nav: [
        {
          icon: 'home',
          text: 'Home',
          title: 'Return to main Site',
          active: true
        },
        {
          icon: 'info',
          text: 'About',
          title: 'Browse Course Areas',
          active: false
        },
        {
          icon: 'assignment_turned_in',
          text: 'Todos',
          title: 'Course Search',
          active: false
        },
        {
          icon: 'email',
          text: 'Contact',
          title: 'Study Seeker',
          active: false
        }
      ],
    ecosystem: [
      {
        text: 'vuetify-loader',
        href: 'https://github.com/vuetifyjs/vuetify-loader',
      },
      {
        text: 'github',
        href: 'https://github.com/vuetifyjs/vuetify',
      },
      {
        text: 'awesome-vuetify',
        href: 'https://github.com/vuetifyjs/awesome-vuetify',
      },
    ],
    importantLinks: [
      {
        text: 'Documentation',
        href: 'https://vuetifyjs.com',
      },
      {
        text: 'Chat',
        href: 'https://community.vuetifyjs.com',
      },
      {
        text: 'Made with Vuetify',
        href: 'https://madewithvuejs.com/vuetify',
      },
      {
        text: 'Twitter',
        href: 'https://twitter.com/vuetifyjs',
      },
      {
        text: 'Articles',
        href: 'https://medium.com/vuetify',
      },
    ],
    whatsNext: [
      {
        text: 'Explore components',
        href: 'https://vuetifyjs.com/components/api-explorer',
      },
      {
        text: 'Select a layout',
        href: 'https://vuetifyjs.com/layout/pre-defined',
      },
      {
        text: 'Frequently Asked Questions',
        href: 'https://vuetifyjs.com/getting-started/frequently-asked-questions',
      },
    ],
  }),
});
</script>

<style scoped>
.header {
  background: #373737;
}

.beta {
  color: #3B7FCF;
  margin-top:2px;
}

.menu {
  color: white;
  height: 70px;
}

.breadcrumbs {
  background: #3AC178;
  font-weight: bold;
  color: black;
  margin-top: -4px;
}

.icon-home-container {
  margin-top: 1%;
  margin-right: -8%;
}

.banner {
  background: #373737;
  height: 370px;
}

.banner-image {
  background-image: url ('https://www.tafensw.edu.au/documents/60140/1073963204/Lockdown-homepage-banner-2-v2--1-desktop.jpg') no-repeat;
}

.course-banner {
  color: white;
  font-weight: bold;
  text-align: center;
  margin-top: 5%;
}

.diploma-text {
  color: #3AC178;
  font-weight: bold;
  font-size: 36px;
  display: block;
  text-align: center;
}

.buitton-ask-question {
  display:block;
}

#location-btn {
  background: #3A80D0;
  padding: 10px;
  margin: 10px;
  border-radius: 0;
}

#ask-question {
  background: #4D4D4D;
  padding: 10px;
  margin: 10px;
  border-radius: 0;
}

.img-banner {
  width: 100%;
  height: 85%;
}

.content-container-left {
  margin-top: 30px;
  font-weight: bold;
  margin-bottom: -20px;
}

.future-heading {
  font-size: 32px;
}

hr.underline {
  height: 5px;
  width: 50%;
  background: green;
}
.pa-2 {
  height: 200px;
}

.card-further-study,
.card-related-study,
.card-previous-stidy {
  height: 400px;
}

.footer-container {
  background: #373737;
  height: auto;
  color: white;
}

.footer-bottom {
  height: 50px;
  background: black;
  color: white;
}

.footer-bottom-text-disclaimer {
  padding: 2%;
}

.footer-bottom-text-privacy {
  padding: 10px;
}

.footer-bottom-text-disclaimer > a,
.footer-bottom-text-privacy > a {
  color: white;
}

.breadcrumbs-item > a {
  color: black;
  margin-bottom: 2px;
}

.v-breadcrumbs {
  padding-top: 14px;
}
.footer-link-row {
  margin-left: 2%;
  color: white;
}

.footer-link-row > div > a {
  color: white;
}

.tafe-abor-banner {
  width: 50%;
  margin-left: 47%;
  margin-top: 1%;
  position: absolute;
}
</style>
