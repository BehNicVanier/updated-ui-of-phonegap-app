# updated-ui-of-phonegap-app
has the ui of the final copy, need to add the functions of the arduino
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta name="apple-mobile-web-app-capable" content="yes" />
    <meta name="mobile-web-app-capable" content="yes" />

    <!-- JS dependencies -->
    <script src="scripts/appBundle.js"></script>
    <script src="lib/onsen/js/onsenui.js"></script>
    

    <!-- CSS dependencies -->
    <link rel="stylesheet" href="lib/onsen/css/onsenui.css" />
    <link rel="stylesheet" href="lib/onsen/css/onsen-css-components-blue-basic-theme.css" />
    <!--
    <link rel="stylesheet" href="onsenui/css/onsenui.min.css">
    <link rel="stylesheet" href="onsenui/css/onsen-css-components.min.css">

    <link rel="stylesheet" href="onsenui/css/font_awesome/css/font-awesome.min.css" />
    <link rel="stylesheet" href="onsenui/css/ionicons/css/ionicons.min.css" />
    <link rel="stylesheet" href="onsenui/css/material-design-iconic-font/css/material-design-iconic-font.min.css" /> -->

    <title>Plant Monitoring System</title>

    <!--THE SIDEBAR-->
    <script>
            function openMenu() {
                document.getElementById('mySplitter').left.open();
            }

            function loadPage(page) {
                var splitter = document.getElementById('mySplitter');
                splitter.content.load(page).then(function() {
                    splitter.left.close();
                });
            }
    </script>

    <style>
        ons-splitter-side .page__background {
            background-color: forestgreen;
        }

        page__background {
            background-color: forestgreen;
        }

        .menu-list,
        .menu-item {
            background-color: transparent;
            background-image: none !important;
            border-color: transparent;
            color: #fff;
            box-shadow: none !important;
        }

        .menu-list {
            margin-top: 25px;
        }

        .menu-notification {
            display: inline-block;
            margin-top: 12px;
            font-size: 14px;
            height: 16px;
            line-height: 16px;
            min-width: 16px;
            font-weight: 600;
            margin-left: -3px;
        }

        .bottom-menu-list,
        .bottom-menu-item:first-child,
        .bottom-menu-item:last-child,
        .bottom-menu-item {
            border-color: #393939;
            background-color: transparent;
            background-image: none !important;
            color: #ccc;
            box-shadow: none !important;
        }
    </style>
</head>
 <!--THE SIDEBAR-->

<body>
    <!-- Cordova reference -->
    <script src="cordova.js"></script>
    <script src="scripts/index.js"></script>
    <!-- -->

    <ons-splitter id="mySplitter">
        <ons-splitter-side side="left" width="220px" collapse swipeable>
            <ons-page>
                <ons-list class="menu-list">
                    <ons-list-item class="longdivider menu-item" tappable tap-background-color="blue" onclick="loadPage('plants.html')">
                        <div class="left">
                            <v-ons-icon icon="fa-pagelines"></v-ons-icon>
                        </div> 
                        Plants <!--Creating the page for Plants-->
                    </ons-list-item>

                    <ons-list-item class="longdivider menu-item" tappable tap-background-color="#555" onclick="loadPage('magic.html')">
                        <div class="left">
                            <ons-icon icon="fa-pagelines" class="list__item__icon"></ons-icon>
                        </div>
                        Magic <!--Creating the page for Magic-->
                    </ons-list-item>

                    <ons-list-item class="longdivider menu-item" tappable tap-background-color="#555" onclick="loadPage('instructions.html')">
                        <div class="left">
                            <ons-icon icon="fa-twitter" class="list__item__icon"></ons-icon>
                        </div>
                        Instructions <!--Creating the page for Instructions-->
                    </ons-list-item>
                </ons-list>

                <br>

                <ons-list class="bottom-menu-list">
                    <ons-list-item class="longdivider bottom-menu-item" tappable tap-background-color="#555" onclick="loadPage('home.html')">
                        Home <!--Creating the page for Home-->
                        <!-- <div class="notification menu-notification">3</div> -->
                    </ons-list-item>
                    <ons-list-item class="longdivider bottom-menu-item" tappable tap-background-color="#555" onclick="loadPage('waitingarea.html')">
                        Waiting Area <!--Creating the page for Waiting Area-->
                    </ons-list-item>
                    <ons-icon icon="clock" class="list__item__icon"></ons-icon>
                    <ons-list-item class="longdivider bottom-menu-item" tappable tap-background-color="#555" onclick="loadPage('extra.html')">
                        Extra <!--Creating the page for Extra-->
                    </ons-list-item>
                </ons-list>
            </ons-page>
        </ons-splitter-side>
        <ons-splitter-content page="home.html"></ons-splitter-content>
    </ons-splitter>

    <!------------------------------------------------------------------------------------------------------------------->

    <ons-template id="home.html">
        <ons-page class="red">
            <ons-toolbar>
                <div class="left">
                    <ons-toolbar-button onclick="openMenu()">
                        <ons-icon icon="ion-navicon, material:md-menu"></ons-icon>
                    </ons-toolbar-button>
                </div>
                <div class="center">
                    Plant Monitoring System
                </div>
            </ons-toolbar>
            <!--Continuing-->
            <ons-row style="margin-top: 100px; text-align: center;">
                <ons-col>
                    <ons-button modifier="light" onclick="openMenu()">
                        Menu
                    </ons-button>
                    <p style="color: #999; font-size: 13px;">  </p>
                    <p>1. Add photos od plants maybe, and discription</p>
                </ons-col>
            </ons-row>
        </ons-page>
    </ons-template>

  
    <ons-template id="plants.html">
        <ons-page class="page__background">
            <div class="background"></div>
            <style>page__background {
            background: forestgreen;
        }</style>
            <ons-toolbar>
                <div class="left">
                    <ons-toolbar-button onclick="openMenu()">
                        <ons-icon icon="ion-navicon, material:md-menu"></ons-icon>
                    </ons-toolbar-button>
                </div>
                <div class="center">
                    Plants
                </div>
            </ons-toolbar>
            <!--Code for the Plants page-->
                  
                <p > 1.     <a href="javascript:alert('Temperature: 13 - 27°C;     Light: High;     Water: Moderately dry soil;     Humidity: Low;');">Aloe Vera</a> </p>
                <p >   2.  <a href="javascript:alert('Temperature: 18 - 25°C;     Light: Med-high;     Water: Evenly moist soil;     Humidity: Average;');">Rose</a> </p>
                <p > 3. <a href="javascript:alert('Temperature: 20 - 27°C;     Light: High;     Water: Evenly moist soil;     Humidity: High;');">Tomato </a> </p>
                <p >   4. <a href="javascript:alert('Temperature: 18 - 24°C;     Med-high;     Water: Evenly moist soil;     Humidity: Average;');"> Spider Plant </a> </p>
                <p > 5.  <a href="javascript:alert('Temperature: 26 - 30°C;     Light: Low-high;     Water: Moderately dry soil;     Humidity: Average;');">Snake Plant</a> </p>
                <p >   6.  <a href="javascript:alert('Temperature: 13 - 21°C;     Light: Med-high;     Water: Evenly moist soil;     Humidity: Average- High;');">English Ivy </a> </p>
                <p > 7.<a href="javascript:alert('Temperature: 7 - 30°C;     Light: Low;     Water: Evenly moist soil;     Humidity: Average;');"> Cast Iron Plant </a> </p>
                <p >   8.  <a href="javascript:alert('Temperature: 13 - 16°C;     Light: High;     Water: Evenly moist soil;     Humidity: Average;');">Sunflower </a> </p>
                <p > 9.  <a href="javascript:alert('Temperature: 15 - 21°C;     Light: High;     Water: Moderately dry soil;     Humidity: Average;');">Dill Plant</a> </p>
                 <!--Code for the Plants page-->
        </ons-pageclass="page__background">
</ons-template>


    <ons-template id="instructions.html">
        <ons-page>
            <ons-toolbar>
                <div class="left">
                    <ons-toolbar-button onclick="openMenu()">
                        <ons-icon icon="ion-navicon, material:md-menu"></ons-icon>
                    </ons-toolbar-button>
                </div>
                <div class="center">
                    Instructions
                </div>
            </ons-toolbar>
            <!--Code for the Instructions page-->
            <ons-page>
                <p>Insert instructions on how to use the app</p>
            </ons-page>
            <!--Code for the Instructions page-->
        </ons-page>
    </ons-template>


    <ons-template id="magic.html">
        <ons-page>
            <ons-toolbar>
                <div class="left">
                    <ons-toolbar-button onclick="openMenu()">
                        <ons-icon icon="ion-navicon, material:md-menu"></ons-icon>
                    </ons-toolbar-button>
                </div>
                <div class="center">
                    Magic
                </div>
            </ons-toolbar>
            <!--Code for the Magic page-->
            <ons-page>
                <p>This is where all the magic happens, where the information from the arduino code shows on the screen</p>
            </ons-page>
            <!--Code for the Magic page-->
        </ons-page>
    </ons-template>

 
    <ons-template id="waitingarea.html">
        <ons-page>
            <ons-toolbar>
                <div class="left">
                    <ons-toolbar-button onclick="openMenu()">
                        <ons-icon icon="ion-navicon, material:md-menu"></ons-icon>
                    </ons-toolbar-button>
                </div>
                <div class="center">
                    Waiting Area
                </div>
            </ons-toolbar>
            <!--Code for the Waiting Area page-->
            <ons-page>
                <p>This is where the user can check for interesting information about plants/ something creative</p>
            </ons-page>
            <!--Code for the Waiting Area page-->
        </ons-page>
    </ons-template>


    <ons-template id="extra.html">
        <ons-page>
            <ons-toolbar>
                <div class="left">
                    <ons-toolbar-button onclick="openMenu()">
                        <ons-icon icon="ion-navicon, material:md-menu"></ons-icon>
                    </ons-toolbar-button>
                </div>
                <div class="center">
                    Extra
                </div>
            </ons-toolbar>
            <!--Code for the Extra page-->
            <ons-page>
                <p>SOmething can go here, anything at all  </p>
            </ons-page>
            <!--Code for the Extra page-->
        </ons-page>
    </ons-template>

</body>
</html>
