# Development / UX Deep Dive

### Tech Stack

The website for NomadSprint.com is a Single Page Application (SPA) created with React and Typescript. The website has CI/CD - it is deployed to AWS on commit to the main branch.  
The API uses the Santander Typescript SDK to communicate with the OpenID portal.

### Architecture / scaling / security

Please see the diagram below for architecture. We already deployed the site as a SPA to AWS S3 with CloudFront CDN. This CDN makes the site very scalable to users around the globe as content is cached at edge locations. We can also add SSL at the CDN layer. The API layer is deployed in a docker container with AWS Load balancer which can scale the required number of docker containers. For the API SSL can be applied to the Load Balancer. SSL Certificates are managed in AWS Certificate Manager.

### UX User Journey Mapping

As part of the UX process we have drawn out key parts of the UX in Whimsical. See the image below for an example.

### UX Designs

As part of the UX process we have designed key parts of the UI in Figma.

### Design System

The design system is Typescript-based to aid quick development the repo is here
https://github.com/createistic/designsystem

# Architecture diagram

![Architecture](https://github.com/createistic/resources/blob/main/images/architecture.png)

# Persona example

![Persona](https://github.com/createistic/resources/blob/main/images/persona.png)

# User Journey example

![UserJourney](https://github.com/createistic/resources/blob/main/images/user-journey.png)
