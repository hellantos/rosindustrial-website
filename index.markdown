---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults
slug: index
layout: homepage
---
<div class="container-fluid">
    <div class="homepage-header">
        <div class="row row align-items-end homepage-header-image">
            <div class="col-sm-12">
                <div class="homepage-header-text">
                    <div class="row homepage-main-wrapper justify-content-end">
                        <div class="col-xs-12 col-lg-8 col-sm-12">
                            <div class="homepage-headline">
                                <h1>The consortium for open-source robot automation</h1>
                                <p class="main-text">
                                    Controlling industrial robots independently of the manufacturer<br/>
                                    and enabling new and advanced industrial robot applications
                                </p>
                                <div class="button-group">
                                    <a class="button button-transparent" href="#">Get Started</a>
                                    <a class="button button-transparent" href="#">Get Involved</a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="homepage">
        <div class="row homepage-text g-4">
            <div class="col-xs-12 col-lg-4 col-sm-12" style="text-align: right;">
                <h2>Advanced Manufacturing</h2>
                <p>ROS-Industrial is an open-source project with the mission to extend the advanced capabilities
                of ROS to manufacturing automation and robotics.</p>
                <a class="button button-transparent" style="margin-right: 0px; margin-bottom: 0px;" href="#">More Information</a>
            </div>
            <div class="col-lg-8">
                <div class="embed-responsive embed-responsive-16by9">
                    <iframe class="embed-responsive-item" src="https://www.youtube.com/embed/IxTJ473MY3Y?controls=0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
                </div>
            </div>
            <div class="col-xs-12 col-lg-3 col-sm-12" style="text-align: left;">
                <h3>Drivers</h3>
                <p>Robots, Actuators and Sensors</p>
            </div>
            <div class="col-xs-12 col-lg-3 col-sm-12" style="text-align: left;">
                <h3>Motion Planning</h3>
                <p>Moveit, Tesseract, Descartes</p>
            </div>
            <div class="col-xs-12 col-lg-3 col-sm-12" style="text-align: left;">
                <h3>Advanced Automation Tools</h3>
                <p>Scan & Plan, Pick & Place</p>
            </div>
            <div class="col-xs-12 col-lg-3 col-sm-12" style="text-align: left;">
                <h3>Software Quality Tools</h3>
                <p>Continuous Integration, Model-driven Software Engineering</p>
            </div>
        </div>
    </div>

    <div class="homepage">
        <div class="row homepage-services">
            <div class="col-sm-12 col-lg-4" style="text-align: right;">
                <h2>Services for Members</h2>
                <p>The ROS-Industrial Consortium offers a wide range of services to its members in order to support
                the uptake of ROS in manufacturing.</p>
                <a class="button button-transparent" style="margin-right: 0px; margin-bottom: 0px;" href="#">More Information</a>
            </div>
            <div class="col-sm-12 col-lg-8">
                <div class="row justify-content-center">
                    <div class="col-sm-12">
                        <div class="row align-items-start justify-content-center">
                            <div class="col-xs-12 col-lg-6 col-sm-12">
                                <img class="ros-i-icons" src="assets/images/software-stack.png" alt="Robot Icon">
                                <h3>Software Stack</h3>
                                <p>The open source software stack to control robots and build new industrial automation applicaitons.</p>
                            </div>
                            <div class="col-xs-12 col-lg-6 col-sm-12">
                                <img class="ros-i-icons" src="assets/images/cooperation.png" alt="Cooperation Icon">
                                <h3>Cooperation</h3>
                                <p>Joint workshops, conferences and projects to improve robotics software for industrial automation.</p>
                            </div>
                            <div class="col-xs-12 col-lg-6 col-sm-12">
                                <img class="ros-i-icons" src="assets/images/technical-support.png" alt="Support Icon">
                                <h3>Technical Support</h3>
                                <p>Access expertise from partner institutions to solve your robotics challenges in industrial automation.</p>
                            </div>
                            <div class="col-xs-12 col-lg-6 col-sm-12">
                                <img class="ros-i-icons" src="assets/images/training.png" alt="Training Icon">
                                <h3>Training</h3>
                                <p>High quality training for professional ROS developers.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <div class="homepage">
        <div class="row homepage-event justify-content-center">
            <div class="col-sm-4" style="text-align: right;">
                <h2 class="h2">Events</h2>
                <p>ROS-Industrial is an open-source project that extends the advanced capabilities of ROS to manufacturing automation and robotics.</p>
                <a class="button button-transparent" style="margin-right: 0px; margin-bottom: 0px;" href="#">More Information</a>s
            </div>
            <div class="col-sm-8">
                <div class="row">
                    {% assign counter = 0 %}
                    {% for event in site.events %}
                    {% capture buildtime %}{{'now' | date: '%s'}}{% endcapture %}
                    {% capture event_time %}{{event.start_date | date: '%s'}}{% endcapture %}
                    {% if event_time > buildtime %}
                    {% assign counter = counter | plus: 1 %}
                    <div class="col-sm-6 col-lg-4 p-2" style="height: 100%; padding: 0 0;">
                        <div class="media-wrapper" style="height:100%;  margin: 0;">
                        <div class="blog-text-wrapper">
                            <h5>
                            {{ event.title }}
                            </h5>
                            <p class="event-date">
                            {{ event.start_date | date: "%B %d, %Y" }} - {{ event.end_date | date: "%B %d, %Y" }}<br/>
                            {{event.location}}
                            </p>
                            <a class="button" href="/rosindustrial-website/install">Register</a>
                        </div>
                        </div>
                    </div>
                    {% if counter == 5 %}
                        {% break%}
                    {% endif %}  
                    {% endif %}  
                    {% endfor %}
                </div>
            </div>
        </div>
    </div>

    <div class="homepage">
        <div class="row homepage-title justify-content-center">
            <div class="col-sm-12">
                <h2 class="h2">Members of the Consortium</h2>
            </div>
        </div>
        <div class="row homepage-text justify-content-center">
            <div class="col-sm-12">
                <img class="member-logo" src="/rosindustrial-website/assets/member-logos/3M.png" alt="3M Logo">
                <img class="member-logo" src="/rosindustrial-website/assets/member-logos/Adlink.jpg" alt="3M Logo">
                <img class="member-logo" src="/rosindustrial-website/assets/member-logos/Aerobotix.png" alt="3M Logo">
                <img class="member-logo" src="/rosindustrial-website/assets/member-logos/AFManTech.jpeg" alt="3M Logo">
                <img class="member-logo" src="/rosindustrial-website/assets/member-logos/AL-Logo.png" alt="3M Logo">
                <img class="member-logo" src="/rosindustrial-website/assets/member-logos/Alias Robotics.png" alt="3M Logo">
            </div>
        </div>
    </div>
</div>
