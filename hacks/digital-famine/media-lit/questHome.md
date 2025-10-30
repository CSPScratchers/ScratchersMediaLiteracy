---
layout: post 
tailwind: True
title: Media Literacy Quest
description: >
  Learn about media literacy and help defend Media Literacy Planet from foreign invaders. Build your shield level by completing the modules. 
author: CSP 2025-26
permalink: /digital-famine/media-lit/
breadcrumb: true
lxdData:
  Title: "Mastery of Media Literacy Modules"
  Description: "Complete your Media Literacy journey and unlock your vault and defend your planet!"
  Topics:
    - Title: "Awareness"
      Genre: "Integration"
      Level: 1
      Description: "Team-defined analytics and mastery module"
      Categories: ["Certificate", "Integration", "Achievement"]
      Video: "/digital-famine/media-lit/submodule_1-video"
      Lessons: "/digital-famine/media-lit/submodule_1/"
      Image: "/images/digital-famine/media-lit.svg"
      Alt: "Analytics Submodule 1"
    - Title: "Bias Detector"
      Genre: "Integration"
      Level: 2
      Description: "Team-defined analytics and mastery module"
      Categories: ["Certificate", "Integration", "Achievement"]
      Video: "/digital-famine/media-lit/submodule_2-video"
      Lessons: "/digital-famine/media-lit/submodule_2/"
      Image: "/images/digital-famine/media-lit.svg"
      Alt: "Analytics Submodule 2"
    - Title: "Truth Scanner"
      Genre: "Integration"
      Level: 3
      Description: "Team-defined analytics and mastery module"
      Categories: ["Certificate", "Integration", "Achievement"]
      Video: "/digital-famine/media-lit/submodule_3-video"
      Lessons: "/digital-famine/media-lit/submodule_3/"
      Image: "/images/digital-famine/media-lit.svg"
      Alt: "Analytics Submodule 3"
    - Title: "Bias Sort"
      Genre: "Integration"
      Level: 4
      Description: "Team-defined analytics and mastery module"
      Categories: ["Certificate", "Integration", "Achievement"]
      Video: "/digital-famine/media-lit/submodule_4-video"
      Lessons: "/digital-famine/media-lit/submodule_4/"
      Image: "/images/digital-famine/media-lit.svg"
      Alt: "Analytics Submodule 4"
---
{%- include tailwind/cs-portfolio-quest_info.html -%}

<style>
/* Galaxy background like Submodule 2 */
body {
  min-height: 100vh;
  background: url('{{ site.baseurl }}/hacks/digital-famine/media-lit/media/assets/spacebackground.jpg') no-repeat center center fixed;
  background-size: cover;
}

/* Optional: overlay for better contrast */
body::before {
  content: '';
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: linear-gradient(135deg, rgba(53,62,116,0.6), rgba(147,132,213,0.6));
  z-index: -1;
}
</style>
