<template>
  <div class="about">
        <div class="banner banner-about">
              <div class="container">
                
                <div class="row justify-content-around align-items-center">
                  <div class="col-md-6  banner-text">
                    <h1>At Ozhouse Clean we come to your house and do your cleaning for you.</h1>
                    <p>As an add-on service, we can also do your ironing, change beds and general tidying.</p>
                  </div>
                  <div class="col-md-6 p-relative d-none d-md-block d-lg-block">
                    <div class="illustration_4">

                    </div>
                  </div>
                </div>
                

              </div>


        </div>

        <div class="container service-component">
            <div class="row justify-content-center">

              <div class="col-md-5">
                <div class="shape_1 illustration_2">

                </div>
              </div>

              <div class="col-md-5 d-flex service_e flex-column justify-content-center">
                <h3 class="pl-0 ml-0"> Regular Clean</h3>

                <p>This service includes full cleaning of living areas, bedrooms and bathrooms.</p>
                <p>All staff insured </p>
                <p class="font-weight-bold">
                  First 2 hours (minimum charge): $70  

                </p>

                <p class="font-weight-bold">
                    Each additional hour thereafter: $25  
                </p>
              </div>
              

            </div>
        </div>

        <div class="container service-component">
            <div class="row justify-content-center">



              <div class="col-md-5 d-flex flex-column  service_e justify-content-center">
                <h3 class="pl-0 ml-0">Spring clean (blitz):</h3>

                <p>Our spring clean service It is designed for customers who don’t’ want a regular cleaner but every now and again want someone to come in and do a spring clean. </p>
                <p>All staff insured </p>
                <p class="font-weight-bold">
                    4 hours blocks at $110 per block.  
                </p>
              </div>

                <div class="col-md-5">
                  <div class="shape_1 illustration_3">

                  </div>
                </div>
              

            </div>
        </div>


      <div class="banner ">
              <div class="container">
                
                <div class="row justify-content-around align-items-center">
                  <div class="col-md-6  banner-text text-center">
                    <h2>We focus on devilering excelent services to our all customers</h2>
                  </div>
                  <div class="col-md-5 banner-form">
                      <b-card class="text-center card">
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


  </div>
</template>


<script>
export default {
    name: 'About',

  data() {
      return {
        form: {
          email: '',
          name: '',
          food: null,
          checked: []
        },
        foods: [{ text: 'Service Type', value: null }, 'Carrots', 'Beans', 'Tomatoes', 'Corn'],
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
    }
}
</script> 

<style lang="scss">

  .banner-about{
    padding: 8em 0px;
     .banner-text{
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
          width: 560px;
          height: 560px;
          background:url('../assets/img/oval-banner.png')  no-repeat top right;
          -webkit-background-size: contain;
          -moz-background-size: contain;
          -o-background-size: contain;
          background-size: contain;
          animation: animateWave 1.9s cubic-bezier(0.23, 1, 0.32, 1) backwards;

        
      }


      .illustration_4{
        position: relative;
        height: 340px;
        &:before{
            width: 30em;
          height: 30em;
        }

      }

      .illustration_2{
        position: relative;

          &:before{
            content: "";
            width: 30em;
            height: 30em;

          }

      }

      .illustration_3{
        position: relative;

          &:before{
            content: "";
            width: 30em;
            height: 30em;

          }

      }




  }

  .service-component{
    padding-bottom: 0;
    padding-top: 12em;
    .service_e{
      text-align: center;
    }
  }

  @media (min-width: 865px) {

    .banner-about{
    padding: 4em 0px;


     

     &:before
       {
          content: "";
          z-index: -2;
          width: 560px;
          height: 560px;

        
      }




  }
      .service-component{
        padding: 9em 0;
        padding-bottom: 5em;
        .service_e{
          text-align: inherit;
    }
      }
 }
  
</style>
