<template>

  <div class="home">
      <div class="banner banner-home"  ref="banner-home">
        <div class="container">
          
          <div class="row justify-content-around align-items-center">
            <div class="col-lg-6  banner-text">
              <h1>At Ozhouse Clean we come to your house and do your cleaning for you.</h1>
              <p>As an add-on service, we can also do your ironing, change beds and general tidying.</p>
            </div>
            <div class="col-lg-4 banner-form">
                <b-card class="text-center card" ref="banner-form" id="banner-form" v-model="card">
                <div class="">
                  <h3>Get a Quote!</h3>
                  <p>Or call us, we’d dicuss how we could help you</p>

                  <b-form class="form" @submit="onSubmit" @reset="onReset" v-if="show">


                          <b-form-group id="input-group-2" >
                            <b-form-input
                              id="input-2"
                              v-model="form.name"
                              required
                              placeholder="Name"
                            ></b-form-input>
                          </b-form-group>


                          <b-form-group id="input-group-3" >
                            <b-form-input
                              id="input-2"
                              v-model="form.name"
                              required
                              placeholder="Phone Number"
                            ></b-form-input>
                          </b-form-group>

                          <b-form-group
                            id="input-group-1"
                            label-for="input-1"
                            description="We'll never share your email with anyone else."
                          >
                            <b-form-input
                              id="input-1"
                              v-model="form.email"
                              type="email"
                              required
                              placeholder="Enter email"
                            ></b-form-input>
                          </b-form-group>



            <b-form-group id="input-group-3" >
              <b-form-select
                id="input-3"
                v-model="form.food"
                :options="foods"
                required
              ></b-form-select>
            </b-form-group>


            <b-button type="submit" variant="primary">Submit</b-button>
                  </b-form>
                </div>
            </b-card>

            </div>
          </div>
          

        </div>
      </div>

      <div class="pt-5 pb-5 container main-feature">
        <div class="row justify-content-center">

          <div class="col-md-5">
            <div class="shape_1 illustration_1">

            </div>
          </div>

          <div class="col-md-5 d-flex flex-column justify-content-around">
            <h3>The Ozhouse Clean Advantage</h3>

            <p>Fully trained staff</p>
            <p>All staff insured </p>
            <p>Safe cleaning procedures  </p>
            <p>All work is backed up by our 24-hour service guarantee: if something isn't done as expected, notify us within 24 hours and we'll return to clean that part off the job free of charge </p>
            <p>Call now. We're confident you won't find a better cleaning service </p>
          </div>
          

        </div>
        

      </div>

      <div class="container call-to-action-1">
        <div class="row text-center justify-content-center">
          <div class="col-md-7">
            <h2 class="pb-3">We focus on devilering efficient services for all customers</h2>
            <b-button type="button" variant="primary">Contact Us</b-button>
          </div>
           

        </div>
      </div>

      <div class="container services">
        <div class="row justify-content-center">
          <div class="col-md-6 text-center service-e">
                                      <div class="shape_2 illustration_2"></div>

            <div class="caption ">
              <h4 class="mt-5">
                Regular Clean
              </h4>
              <p>This service includes full cleaning of living areas, bedrooms and bathrooms.  </p>
              <b-button type="button"  class="mt-2" variant="primary">Know more</b-button>

            </div>
          </div>

          <div class="col-md-5 text-center  service-e">
                          <div class="shape_3 illustration_3"></div>

            <div class="caption flex-column justify-content-between">


              <h4 class="mt-5">
                Spring Clean
              </h4>
              <p class="">Fast But efficient Cleaning</p>
              <b-button type="button" class="mt-4" variant="primary">Know more</b-button>

            </div>
          </div>

        </div>
      </div>


    <div class="testi ">
        <div class="container testimonials">
        <div class="row justify-content-center">
          <div class="col-md-2 m-0 section-avatar  align-self-center small-rounded-shape">
            <img src="../assets/img/avatar1.png" class="rounded-circle avatar">
          </div>
          <div class="col-md-5 align-self-center testi-caption small-rounded-shape-2">
              
              <h4>
                “My house used to be a total disaster, i had not much time for it, then ozhouse clean showed up in my life, and  made it easier” 
              </h4>
              <h5>
                -Paul Blank Stater, Colaba24 CEO
              </h5>
          </div>
        </div>
      </div>
    </div>
      
  </div>

</template>

<script>
// @ is an alias to /src
import { TimelineLite } from 'gsap'


export default {
  
  name: 'Home',

  data() {
      return {
        form: {
          email: '',
          name: '',
          food: null,
          checked: [],
          card:null,
        },
        foods: [{ text: 'Service Type', value: null }, 'Swift Clean s', 'Regular Clean','other service'],
        show: true
      }
    },
    methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.name = ''
        this.form.food = null
        this.form.checked = []
        // Trick to reset/clear native browser form validation state
        this.show = false
        this.$nextTick(() => {
          this.show = true
        })
      }
    },
     mounted() {

      //  const { box } = this.$refs
        //  var content = getComputedStyle(document.querySelector('.banner'), ':before')

         const timeline = new TimelineLite()
          timeline.to("#banner-form", 0, {
            // y: 4,
            autoAlpha:0,
            // rotation: 100,
            // ease: Back.easeInOut, // Specify an ease
          },          '-=0' 
          )
    
          timeline.to("#banner-form", 1.5, {
            // y: 4,
            scale:1.131,
            autoAlpha:0,
            // rotation: 100,
            // ease: Back.easeInOut, // Specify an ease
          })
          timeline.to("#banner-form",1.4, {
            // y: 0,
            scale:1,
            autoAlpha:1,

            // rotation: 0,

          },
          
          )


    },
    created() {
    console.log('At this point, this.property is now reactive and propertyComputed will update.')
    this.property = 'Example property updated.'
  }
}
</script>

<style lang="scss">

@keyframes animateWave {
  0% {
    transform: scale(15,15) skewY(-50deg);
    z-index: 999;
  }
  
  100% {
    transform: scale(1,1) skewX(0);
    z-index: 0;
    
  }
}
  .banner{
    padding: 4em 0px;
     .banner-text{
       h1{
         text-shadow: 0 0 0.4rem white;
       }
       p{
          font-family:'Helvetica Neue';
          font-style: italic;
        

       }
      
     }

     

     &:before
       {
         content: "";
        position: absolute;
        top: 0;
        right: 0;
        z-index: -2;
        width: 650px;
        height: 650px;
        background:url('../assets/img/oval-banner.png')  no-repeat top right;
        -webkit-background-size: contain;
        -moz-background-size: contain;
        -o-background-size: contain;
        background-size: contain;
        animation: animateWave 1.9s cubic-bezier(0.23, 1, 0.32, 1) backwards;

        
    }
  }


  .banner-form{
       border: none;
       .card{
         border: none;
        box-shadow: 14px 10px 61px 0 rgba(0,0,0,0.19);
        border-radius: 10px;
        background: #FFFFFF;
        padding: 1.2em 1.8em;

        p{
           font-family:'Helvetica Neue';
          font-style: italic;
        }
        .form{
          ::placeholder { /* Chrome, Firefox, Opera, Safari 10.1+ */
              padding: 0;
              font-size:0.8rem;
              position: absolute;
              top: 0;
              left: 0;
              margin-top: -20px;
            }
        }

     


         
       }
     }

   #banner-form{

        }

  .service-e{
    padding: 7em 0;
  }

  .testi{
    position: relative;
    &:before{
         content: "";
          position: absolute;
          width: 100px;
          height:100px;
          left:-50px;
          bottom: 5vh;
          background:url('../assets/img/oval-small-4.svg')  no-repeat center left;
        -webkit-background-size: contain;
        -moz-background-size: contain;
        -o-background-size: contain;
        background-size: contain;
    }

    &:after{
         content: "";
          position: absolute;
          width: 100px;
          height:100px;
          right:-50px;
          top: 5vh;
          background:url('../assets/img/oval-small-1.svg')  no-repeat center right;
        -webkit-background-size: contain;
        -moz-background-size: contain;
        -o-background-size: contain;
        background-size: contain;
    }

    .testimonials{
    padding: 7em 0;
    position: relative;
    .section-avatar{
      position: relative;
        text-align: center;
      img{
        background: #D8D8D8;
        box-shadow: -9px 9px 29px -7px rgba(0,0,0,0.50);
        margin-bottom:20px;

      }
      &:before{
        left:-50px;
      }
    }
    .testi-caption{

      padding: 0 2em;
      &:before{
        width: 70%;
        height: 80%;
        right: -20%;
        bottom: 0%;
      }
       h4{

        font-family:'Gilroy-Light';
        font-size: 24px;
        color: rgba(5,5,77,0.75);
        letter-spacing: 0.06px;
        font-style: italic;

       }
       h5{
        font-size: 18px;
        color: #03045E;
        letter-spacing: 0.06px;
        line-height: 36px;
       }
    }
    }
  }

@media (min-width: 865px) { 
  .service-e{
    padding: 0 0;

  }

  .testimonials{
    padding: 7em 0;
    position: relative;
    .section-avatar{
      position: relative;
      text-align: center;

    }
    .testi-caption{

        padding: 0 0;
      }
    }


 }


</style>
