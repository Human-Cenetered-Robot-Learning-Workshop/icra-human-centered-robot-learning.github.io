---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

permalink: /
title: Home
layout: home
---

<h1 class="page-heading">Human-Centered Robot Learning in the Era of Big Data and Large Models</h1>

<p class="workshop-location" align="center">
    Location and Date: TBD
</p>
<!-- <p align="center">
    <a href="">[Live Stream Link]</a>
</p> -->


<!-- <video autoplay muted loop style="object-fit: cover; height: 320px; width: 100%; border-radius: 8px; box-shadow: 0 4px 8px rgba(0,0,0,0.2);">
    <source src="assets/img/teaser_video.mp4" type="video/mp4">
    Your browser does not support the video tag.
</video> -->

<br>
<br>

Recent advances in training large-scale models on massive internet-scale data show promise for producing foundation models that enable robots to perform sophisticated tasks in human-centered environments (e.g., transportation, households, healthcare, and warehouses). These models enable new paradigms for human-robot interaction, allowing robots to follow complex human instructions, collaborate with humans, and understand and comply with social norms. 


However, compared to deploying AI models that interact with humans virtually, deploying those embodied AI agents to interact with humans in the physical world imposes additional challenges, for example: 1) These models must be grounded in human representations and understandings of the physical world for effective and trustworthy interactions; 2) The risk of physical harm to humans imposes significantly higher requirements on AI safety; 3) acquiring human-robot interaction data is significantly harder than accessing internet data used for training large language models (LLMs). 

This workshop aims to bring together interdisciplinary experts in related fields, such as robot learning, human-robot interaction, natural language processes, cognitive science, and trustworthy AI, to gather and discuss these grand challenges. We envision this exchange of ideas within and across disciplines can build new bridges to developing and deploying large-scale models for interactive embodied AI systems.

We intend to guide our conversations with the following questions:
<ul>
    <li>What are the ideal data types for learning embodied interactions, and how can we acquire them efficiently and safely?</li>
    <li>How can we train large models for human-centered robots to ensure robustness across diverse human interaction behaviors?</li>
    <li>What challenges do human-centered robotic applications pose for AI safety and alignment, and how can we align robot behaviors with stakeholder values?</li>
    <li>What new interaction paradigms between humans and robots are enabled by big data and large models? Given these new paradigms, what are the best practices for allocating tasks to robots and people in a collaborative setting?</li>
</ul>

<!-- ![](assets/img/banner.jpg) -->



<section id="speakers">
    <h2 class="mb-4">Speakers</h2>
    <div class="row">
        {% for speaker in site.data.speakers %}
        <div class="col-lg-3 col-md-4 mb-3">
            <div class="card h-100">
                <div class="card-img-container mx-auto">
                    <img src="{{ '/assets/img/speakers/' | append: speaker.img }}" class="card-img-top rounded-img mx-auto" alt="{{ speaker.name }}">
                </div>
                <div class="card-body">
                    <h5 class="card-title  text-center"><a href="{{ speaker.webpage }}"> {{speaker.name}} </a></h5>
                    <h5 class="card-title  text-center">
                    <a href="{{ speaker.affil_link }}">{{ speaker.affil }}</a></h5>
                    <!-- <p class="card-text">{{ speaker.bio }}</p> -->
                </div>
            </div>
        </div>
        {% endfor %}
    </div>
</section>

<!-- Call for Papers -->

<section id="papers">
    <h2 class="mb-3">Call For Papers</h2>
    <p>Submission deadline: <b>March 31st, 11:59PM UTC-0</b></p>
    <div class="submission-box">
    <a href="">Submission Link Available Later</a>
    </div>
    <br>
     We invite submissions that address the fundamental challenges in enabling large-scale human-centered robot learning or demonstrate novel human-centered embodied AI systems enabled by large-scale data and models. The related topics include but are not limited to:
    <ul>
        <li>Foundation models for embodied AI</li>
        <li>Data accessibility for embodied AI</li>
        <li>AI Safety and alignment for embodied AI</li>
        <li>Efficient fine-tuning of pre-trained large models for embodied AI</li>
        <li>Applications in human-robot interaction and collaboration</li>
    </ul>
    Accepted papers will be presented as spotlight talks and the posters, and will be made available on the workshop website with the authors’ consent. All papers will be presented on-site during the workshop.
    <br>
    <br>
    <h4 class="mb-3">Submission Guidelines</h4>
    TBD.
    <!-- There is <b>no</b> strict page limit; however, we encourage submissions to be within 4-8 pages (excluding references) to facilitate thorough review.
    <br>
    Papers should be submitted in PDF format, adhering to the ICRA template and submission guidelines on our workshop website.
    <br>
    Submissions will be evaluated based on their originality, technical quality, relevance to the workshop themes, and potential to spark discussions on the future of robot manipulation.
    <br>
    <b>Additionally</b>, to encourage discussion on the workshop topic, we ask authors to provide 1~2 paragraphs of statements on how their work relates to the workshop theme (See the submission page). These information will help us organize the workshop discussion and better feature the accepted works on the website.
    Accepted papers will be presented either as posters or orals, and will be archived on the workshop website with the authors’ consent. All papers will be presented on-site during the workshop. -->

    <br>
    <br>
    
</section>


<section id="schedules">
    <h2 class="mb-3">Schedule</h2>
    <!-- Schedule -->
    <!-- Comment out the following line and uncomment it if there is urgent notice about schedule.  -->
    <!-- <p class="highlight">Important notice.</p> -->
    <div class="countdown-container">
    <div class="time-box">
        <span id="days" class="time-number">00</span>
        <span class="time-label">days</span>
    </div>
    <div class="time-box">
        <span id="hours" class="time-number">00</span>
        <span class="time-label">hours</span>
    </div>
    <div class="time-box">
        <span id="minutes" class="time-number">00</span>
        <span class="time-label">minutes</span>
    </div>
    </div>
    <div id="real-time-clock">
    </div>
    <div class = "post-content">
        <div id="timezone-buttons">
        <input type="radio" id="tokyo-time-btn" name="timezone" class="timezone-radio" onclick="selectTokyoTime()" checked>
        <label for="tokyo-time-btn" class="timezone-label">Atlanta Time</label>
        <input type="radio" id="local-time-btn" onclick="selectLocalTime()" name="timezone" class="timezone-radio">
        <label for="local-time-btn" class="timezone-label">Local Time</label>
        <div id="slider"></div>
    </div>
    <table>
        {% for scheduleitem in site.data.schedules %}
        <tr class="schedule-row" data-event-time="{{ scheduleitem.time }}">
            <td class="time-cell" data-tokyo-time="{{ scheduleitem.time }}">
                <!-- Initially shows Tokyo time; will be updated by JavaScript -->
                <p align="center">
                <!-- {{ scheduleitem.time }} -->
                    <div align="center" class="time-display"></div>
                    <div align="center" class="timezone-info"></div>
                </p>
            </td>
            <td align="center">
                <div class="col-xs-12">
                    <b>{{ scheduleitem.title }}</b>
                </div>
                <br>
                {% if scheduleitem.description %}
                <div class="col-xs-12" align="center">
                    {{ scheduleitem.description }}
                </div>
                {% endif %}
            </td>
            <td>
                <div class="people-name text-center">
                    <!-- scheduleitem name (link to webpage if provided) -->
                    {% if scheduleitem.speaker_webpage %}
                        <a href="{{ scheduleitem.speaker_webpage }}" target="_blank">{{ scheduleitem.speaker }}</a>
                    {% else %}
                        {{ scheduleitem.speaker }}
                    {% endif %}
                    <br>
                    <!-- scheduleitem affiliation (if provided) -->
                    {% if scheduleitem.affiliation %}
                        {{ scheduleitem.affiliation }}
                    {% endif %}
                </div>
            </td>
        </tr>
        {% endfor %}
    </table>
    </div>
</section>

<!-- Force time display in the table -->
<script>
    selectTokyoTime();
    updateScheduleStyles();
</script>

<!-- <section id="workshop-location" class="mt-5">
    <h2 class="mb-3">Workshop Location</h2>
    <div class="row">
        <div class="col-lg-12 col-md-12 mx-auto">
            <img src="assets/img/workshop_location.jpg" alt="Workshop Location" class="img-fluid">
        </div>
    </div>
</section> -->

<!-- Organizers Section -->
<section id="organizers" class="mt-5">
    <h2 class="mb-3">Organizers</h2>
    <div class="row">
        {% for organizer in site.data.organizers %}
            {% unless organizer.is_advisor %}
                <div class="col-lg-2 col-md-4 col-sm-6 mb-4">
                    <div class="card h-100">
                        <div class="card-img-container mx-auto">
                            <img src="{{ '/assets/img/organizers/' | append: organizer.img }}" class="card-img-top rounded-img mx-auto" alt="{{ organizer.name }}">
                        </div>
                        <div class="card-body">
                            <h5 class="card-title text-center">
                                <a href="{{ organizer.webpage }}">{{ organizer.name }}</a>
                            </h5>
                            <h5 class="card-title text-center">
                                <a href="{{ organizer.affil_link }}">{{ organizer.affil }}</a>
                            </h5>
                        </div>
                    </div>
                </div>
            {% endunless %}
        {% endfor %}
    </div>
</section>

<!-- Organizers Section -->
<section id="organizers" class="mt-5">
    <h2 class="mb-3">Advisory Board</h2>
    <div class="row">
        {% for organizer in site.data.organizers %}
            {% if organizer.is_advisor %}
                <div class="col-lg-2 col-md-4 col-sm-6 mb-4">
                    <div class="card h-100">
                        <div class="card-img-container mx-auto">
                            <img src="{{ '/assets/img/organizers/' | append: organizer.img }}" class="card-img-top rounded-img mx-auto" alt="{{ organizer.name }}">
                        </div>
                        <div class="card-body">
                            <h5 class="card-title text-center">
                                <a href="{{ organizer.webpage }}">{{ organizer.name }}</a>
                            </h5>
                            <h5 class="card-title text-center">
                                <a href="{{ organizer.affil_link }}">{{ organizer.affil }}</a>
                            </h5>
                        </div>
                    </div>
                </div>
            {% endif %}
        {% endfor %}
    </div>
</section>