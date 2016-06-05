---
layout: post
permalink: /post/61666962950/giving-up-on-mapstraction
title: "Giving up on mapstraction"
date: "2013-09-19 14:40:16+0000"
categories: "mapstraction, leaflet, maps, javascript, nestoria, endofanera"
---
Today we&rsquo;re going live with the major test (50% of users I believe) of a new design of <a href="http://www.nestoria.com" target="_blank">Nestoria</a> in four of our eight markets. I&rsquo;m proud of this not just because I think the new design is a nice improvement, but also because it&rsquo;s a major user facing project that I had no input into (I&rsquo;ve been able to largely turn my attention to <a href="http://www.opencagedata.com">new projects</a>, for which I&rsquo;m very grateful). It&rsquo;s been a great effort by all involved. It&rsquo;s a total visual refresh, including new branding and logo, while staying true to our ethos of making property search as simple as possible.


One behind the scenes technical aspect of the new design is that we will stop using <a href="http://mapstraction.com">mapstraction</a>, the javascript mapping abstraction library <a href="http://blog.nestoria.co.uk/post/44815473224/nestoria-sponsors-mapstraction">we funded the development of</a> when we started Nestoria over seven years ago. The map is a key component of the Nestoria search experience and from day one we knew we wanted to do everything we could to not be locked into a single mapping provider. So we worked with <a href="http://stevecoast.com/">Steve Coast</a>, <a href="https://twitter.com/mikel">Mikel Maron</a>, and <a href="http://www.tom-carden.co.uk/">Tom Carden</a> to get mapstraction off the ground. The project was open source, and over the years more and more people have contributed (including <a href="https://github.com/freyfogle/">me</a> occasionally), and more and more mapping providers have been added. <a href="https://github.com/mapstraction">Development of mapstraction is ongoing</a>, and version 3 is currently very close to being released, not least thanks to the valiant efforts of <a href="http://www.vicchi.org/">Gary Gale</a>. The software keeps getting better, and I&rsquo;m proud that my tiny start-up helped kickstart useful open software into life (BTW <a href="https://github.com/lokku">we also opensource other stuff</a>).


But the market situation mapstraction was built to address has changed. Fundamentally, it seems developers now face two choices - Google or OpenStreetMap (one could argue Yandex is a viable choice in certain markets, and to be honest I have no clue about China and Japan). Frankly, none of the other mapping providers have critical mass, at least in the digital circles I frequent. Some, like Yahoo, have disappeared completely ** lone purple tear runs down my cheek **. Almost all of the innovative stuff I see is being done using OpenStreetMap. And while I still come across the occasional use of <a href="http://openlayers.org/">OpenLayers</a> for displaying OSM tiles, by a wide majority devs have switched to using the excellent <a href="http://leafletjs.com/">leaflet</a> library, not least because of the emphasis on lightness and the excellent documentation. 


With leaflet using tiles from any of the OSM tile services, or indeed any tile service, is trivial (at Nestoria we use <a href="http://open.mapquest.com/">MapQuest&rsquo;s OSM tiles</a>). There are more and more OSM tile providers (see <a href="http://www.mapbox.com/">MapBox</a> or <a href="http://www.thunderforest.com">Thunderforest</a>), I can&rsquo;t really foresee a scenario in which we&rsquo;ll move away from it to another commercial service. 


And so, rather than build mapstraction into our site - at the cost of additional bandwidth for the user to download and additional maintenance burden for our team (having to stay on top of what&rsquo;s new in mapstraction), we&rsquo;ve moved to the assumption that we will always use leaflet or Google. 


Similarly I don&rsquo;t understand why commercial providers like <a href="http://here.com">HERE</a> or <a href="http://www.ordnancesurvey.co.uk">Ordnance Survey</a>, who have amazing data, continue to bother with their own javascript libraries. Instead they should support leaflet, either directly, or by providing their own plugin or wrappers, similarly to how MapBox does it. The value proposition and differentiator of these services to us as operators of a consumer service is their amazing content, NOT the javascript library used to render the maps. Actually, by forcing me to even contemplate another library they raise the &ldquo;cost&rdquo; of using their service. 


All good wishes to those who continue to use mapstraction, and heartfelt thanks to all the contributors - on Nestoria alone your code has been used by millions of people, be proud. But as the online mapping landscape changes the cost of an abstraction layer no longer justifies the benefit. 
















