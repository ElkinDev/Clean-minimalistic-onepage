    <template>


         <b-navbar toggleable="md"  class="container transparent" id="nav">
            <b-navbar-brand to="/" >OzHouse Clean</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="m-auto">

                <b-nav-item to="/" router-tag="li">Home</b-nav-item>
                <b-nav-item  to="/about" router-tag="li">Pricing</b-nav-item>
                <b-nav-item  to="/about" router-tag="li">Services  Contact</b-nav-item>
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav >
                <b-nav-item to="/"  >
                <div class="d-flex flex-row align-items-center">
                <span>
                    <svg width="45px" height="40px" viewBox="0 0 45 40" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                
                    <g id="Services-Wireframe" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
                        <g id="Services-Prototype" transform="translate(-878.000000, -15.000000)">
                            <g id="oval-banner" transform="translate(770.000000, 210.000000) rotate(24.000000) translate(-770.000000, -210.000000) translate(507.000000, -101.000000)" fill="">
                                <g transform="translate(0.053678, 0.068629)" id="Oval">
                                    <path d="M473.902368,546.577186 C559.939181,450.375822 490.851885,324.846542 490.851885,220.259446 C490.851885,115.672349 560.515857,12.7559266 460.088161,12.7559266 C406.145128,12.7559266 110.647801,-13.7945147 143.077511,109.63441 C179.18438,247.058769 28.6723164,255.842757 28.6723164,350.693644 C28.6723164,452.081836 200.178186,525.170355 269.01046,566.519903 C346.743487,613.216391 437.938387,586.790019 473.902368,546.577186 Z"></path>
                                </g>
                            </g>
                            <g id="Header-protoype">
                                <g id="Header">
                                    <g>
                                        <rect x="0" y="0" width="1024" height="65"></rect>
                                        <g id="e.-links" transform="translate(726.000000, 9.000000)">
                                            <text id="Call-us-1800-333-333" font-family="Gilroy-Medium" font-size="14" font-weight="500" fill="#FFFFFF">
                                                <tspan x="0" y="32.9047619">Call us 1800 333 333</tspan>
                                            </text>
                                            <g id="Group" transform="translate(147.000000, 0.000000)">
                                                <path d="M26.5,45 C38.3741221,45 33.0869065,39.7063001 48,26 C62.9130935,12.2936999 38.3741221,7 26.5,7 C14.6258779,7 5,15.5065898 5,26 C5,36.4934102 14.6258779,45 26.5,45 Z" id="Oval" fill="#EBF4F6" transform="translate(28.834650, 26.000000) rotate(-18.000000) translate(-28.834650, -26.000000) "></path>
                                                <g id="_Icons-/-Phone-/-Default" transform="translate(16.114266, 12.721447)">
                                                    <g id="Phone">
                                                        <rect id="Container" x="0" y="0" width="21" height="25"></rect>
                                                        <path d="M19.3096522,2.27789049 L15.4502746,1.21775446 C15.0304188,1.10240607 14.6012486,1.36142085 14.4313989,1.83319618 L12.6501477,6.78098365 L12.6501477,6.78098369 C12.4938395,7.21518178 12.5976768,7.72011215 12.9047924,8.01924484 L15.1542529,10.2102898 C13.8193164,13.597627 11.482723,16.4176322 8.57664882,18.0407267 L6.73617101,15.3628417 L6.73617104,15.3628417 C6.48489884,14.997228 6.06075769,14.8736117 5.69603167,15.0596933 L1.5398902,17.1802304 C1.14371024,17.3823441 0.925989392,17.8932168 1.02291914,18.3931777 L1.91343342,22.9876748 C2.00598426,23.4651049 2.36368177,23.8095155 2.78123674,23.8095155 C12.2844717,23.8095155 20,14.6411964 20,3.31098976 C20,2.81725803 19.7137364,2.38886535 19.3096522,2.27789057 L19.3096522,2.27789049 Z" id="Icon-Style" fill="#484A54"></path>
                                                    </g>
                                                </g>
                                            </g>
                                        </g>
                                    </g>
                                </g>
                            </g>
                        </g>
                    </g>
                </svg>
                </span>

                                <span class="text-white">Call us 1800 333 333</span>

                    
                </div>
                </b-nav-item>
            </b-navbar-nav>

            </b-collapse>
        </b-navbar>
    </template>

    <script>
    export default {
        
    name: 'headerc',

    }
    </script>

    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>

    </style>
