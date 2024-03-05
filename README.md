# Learning Geeks Project

Welcome to the Learning Geeks project! This is a personal project that implements a full-stack application using React for the front end and Spring Boot for the back end. The project leverages various technologies and services for authentication, state management, and database storage.

## Overview

The Learning Geeks project consists of a React Single Page Application (SPA) for the front end, utilizing Google OAuth for authentication. The global state is managed using Redux Store, and Redux Thunk middleware is employed for asynchronous API calls.

![Application Overview](./Overview.gif)

For the back end, two Spring Boot microservices have been developed:

1. **Profile Service:**
   - Manages profiles with operations such as adding a new profile, updating existing profiles, and deleting profiles.
   - Implemented in Java 8.
   - Utilizes AWS RDS as the database for profile management.

2. **Search Service:**
   - Takes skills as input and returns matched profiles.
   - Implemented in Java 8.

Both the front end and back end are deployed on AWS EC2 instances.

## Authentication Logic

The authentication logic in the front end is designed to accommodate both Guest profiles and Verified profiles. Here's how it works:

- **Guest Profiles:**
  - Guest users have limited access and can browse the application.
  - Guests can create a profile with limited information.
  - Guests can delete their own profiles.
  - They cannot view details of verified profiles.

- **Verified Profiles:**
  - Users with verified profiles have access to additional features.
  - Verified profiles can manage their corresponding profiles, update information, and delete profiles.
  - Verified profiles can view other verified profiles.

This logic is gracefully handled within the front-end application to ensure a seamless and secure experience for both guest and verified users.

## Technologies Used

- Front End:
  - React
  - Redux (State management)
  - Google OAuth (Authentication)

- Back End:
  - Spring Boot (Java 8)
  - AWS RDS (Database)
  
- Deployment:
  - AWS EC2

## Project Structure

- [`personal-profile-blogUI`](./personal-profile-blogUI): Contains the React SPA code.
- [`springboot-profile-blog-service`](./springboot-profile-blog-service/): Spring Boot microservice for profile management.
- [`springboot-profile-search-service`](./springboot-profile-search-service/): Spring Boot microservice for profile searching.
