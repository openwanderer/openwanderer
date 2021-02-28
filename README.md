# OpenWanderer

OpenWanderer is a project to develop a 100% free and open source panorama sharing platform.

## Why?

There are a few platforms out there already which allow you to view, and share, 360 degree panoramic imagery of roads and hiking trails, allowing you to navigate from panorama to panorama. However, none of the leading players are completely free and open source. Google StreetView now allows you to contribute panoramas, but comes with restrictive licensing. [Mapillary](https://mapillary.com) is much more open with the licensing of the panoramas themselves, and they have open-sourced some software components, but the source code for the Mapillary server-side platform is proprietary and closed-source. And [OpenStreetCam](https://github.com/kartaview/openstreetcam.org) used to be free and open-source software but, as can be seen from the commits, sadly the original server-side code has again been replaced by a closed-source backend.

We believe, therefore, that there is a place for a completely free and open-source platform which can be freely used and modified by all, in which not only the panoramas themselves and the client-side code are free, but the entire stack - panoramas, client-side code, data processing scripts, and server-side application. We also believe in complete transparency as to how the panoramas will be used; one danger of a closed-source and proprietary server-side platform is that no-one knows for sure how the panoramas are processed. In an era in which personal privacy is a key concern of many, we believe this is absolutely vital - and making the source code fully open is the surest way of enabling this.

## Philosophy - a modular and distributed platform, installable on your own server

Our philosophy is not to create a monolithic application residing on one server farm and owned by one single organisation. Instead, we aim to produce a platform that can be installed on your own server - so that you can serve what *you* want. If you are only interested in showing panoramas of a 400km^2 national park, rather than the entire world, OpenWanderer aims to be the platform for you. We recognise that panoramas use a large amount of storage space, so it is not our aim to try and cover the entire world on the central OpenWanderer website. We would (eventually!) like to cover as much of the world as possible... but our aim is to realise this via a *distributed* system. So we envisage (well, perhaps dream of would be more realistic at this stage) a system made up of many, many OpenWanderer servers, hosted all around the world and covering just a small area of the world, of city, county, region or national park size. A "master" server could then receive a request to view panoramas of any part of the world and the request would then be dispatched to the appropriate server for that area. That way, we can in theory cover the whole world without any one individual or organisation having to foot the entire bill for hosting.

As well as that, though, it's our aim that you can install the OpenWanderer platform for your own private use. So if you manage an outdoor tourist attraction, for example, we aim to produce a platform that you can install on your own server space to host panos of your tourist attraction, and your tourist attraction only. For example, you could provide virtual tours of some flower gardens or the grounds of a country house, and in doing so, encourage people to visit your attraction for-real. (Rather than reducing people's desire to visit somewhere through providing virtual tours, we believe it encourages people to visit a location for-real having seen a virtual taster).

## OpenWanderer and OpenTrailView

You may know that one of us (@nickw) has been developing [OpenTrailView](https://www.opentrailview.org), a project to produce fully free and open panoramas of walking routes and hiking trails, something neglected by the major players until recently.  How does OpenWanderer relate to OpenTrailView? Well, following discussions between both of us (@nickw and @MrAceT) and with other members of the panos community, we decided that a more general open panos platform, covering any environment - including urban environments - would be a goal well worth pursuing. And so the OpenWanderer concept was born. And what of the future of OpenTrailView? Well it will continue to be developed, but from version 4, will use the OpenWanderer platform as its core engine.

## Status

At the moment, OpenWanderer is very early in development but even at this stage comprises a basic platform to upload and view panoramas and panorama sequences.

## Components

OpenWanderer is not a single monolithic applicatiom, but rather a series of modular components which you can pick and choose from. There is a client-side JavaScript API which can be used standalone with static panoramic images, and a server-side application which can serve panorama sequences and manage the upload of new ones. Additionally, there is a server-side 'bot' which aims to perform background processing tasks such as add elevation to panoramas, and later, perform vital anonymisation tasks such as blur faces and license plates. (We have already done preliminary work on this but are in the process of selecting the best anonymisation approach).

## Repositories

Please see the individual repositories:

- [jsapi](https://github.com/openwanderer/jsapi) - the client-side JavaScript API
- [server](https://github.com/openwanderer/server) - the server platform
- [server-bot](https://github.com/openwanderer/server-bot) - the server-side "bot"
- [example-app](https://github.com/openwanderer/example-app) - the example full OpenWanderer application, designed to show what the platform is currently capable of. As well as the full example, there is also a minimal, basic example showing the absolute basic functionality (upload and navigation) only.

## Licensing

All code is licensed under the Lesser GNU General Public License 3. This ensures that OpenWanderer platform code is completely free and open-source, and that any modifications you make to platform code must be contributed back to the project and remain under the same free license. However, it also allows you to *use* OpenWanderer in your own proprietary application, should you wish.

