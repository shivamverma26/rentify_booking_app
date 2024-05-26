# Rentify - Where Renting Meets Simplicity

## Overview
Rentify is a real estate platform designed to connect property owners with potential tenants. The platform simplifies the rental process by providing a user-friendly interface for listing and searching rental properties. This document outlines the implementation details for the Rentify challenge, which includes developing a full-stack application with a focus on both backend and frontend components, and additional features.

## Tech Stack
- **Frontend**: React
- **Backend**: Node.js with Express
- **Database**: MongoDB with Prisma ORM
- **Authentication**: JWT with Cookies

## Part I: Basic Application (Mandatory)

### Features

#### User Registration and Login
- **Fields**: First Name, Last Name, Email, Phone Number
- **Roles**: User can register as either a seller or a buyer.

#### Seller Flow
- **Post Property**: Sellers can list their properties by providing essential details (e.g., location, area, number of bedrooms, bathrooms, nearby amenities such as hospitals and colleges).
- **View Properties**: Sellers can view a list of their posted properties.
- **Update/Delete Properties**: Sellers can update or delete their property listings.

#### Buyer Flow
- **View Properties**: Buyers can browse all posted rental properties.
- **Interested Button**: Buyers can express interest in a property. Clicking "I’m Interested" reveals seller details.
- **Filters**: Buyers can apply filters based on property details (e.g., location, price range, number of bedrooms).

### Implementation Steps

#### Backend
1. **Setup Node.js with Express**: Initialize the backend with Express, and setup routing.
2. **Database Configuration**: Configure MongoDB using Prisma ORM.
3. **User Authentication**: Implement JWT authentication for user login and registration.
4. **CRUD Operations**: Create endpoints for property CRUD operations (Create, Read, Update, Delete).
5. **Filtering**: Implement query parameters in GET requests to filter properties based on criteria.

#### Frontend
1. **Setup React App**: Initialize a React project.
2. **UI Components**: Design components for registration, login, property listing, and property details.
3. **State Management**: Use React Context or Zustand for managing global state.
4. **API Integration**: Connect frontend with backend using Axios for API calls.
5. **Routing**: Use React Router for navigation between pages.

## Part II: Add-On Features (Advanced)

### Features

1. **Pagination**: Implement pagination for property listings.
2. **Form Validation**: Add client-side and server-side validation for forms.
3. **Mandate Login**: Ensure buyers must log in to view seller details.
4. **Like Button**: Add a like button to each property and track the count live.
5. **Email Notifications**: 
   - Send email to buyers with seller contact details when interested in a property.
   - Send email to sellers with buyer details when a buyer shows interest.

### Implementation Steps

#### Backend
1. **Pagination**: Modify GET endpoints to support pagination parameters.
2. **Form Validation**: Use libraries like Joi for backend validation and Formik with Yup for frontend validation.
3. **Authentication Middleware**: Protect routes to ensure only authenticated users can access certain endpoints.
4. **Real-time Updates**: Implement Socket.io for live updates on like counts.
5. **Email Integration**: Use NodeMailer to send emails when interest is expressed in a property.

#### Frontend
1. **Pagination UI**: Add pagination controls to the property listing page.
2. **Validation**: Integrate Formik and Yup for form validation.
3. **Protected Routes**: Implement protected routes in React using React Router.
4. **Like Button**: Create a like button component and integrate with Socket.io for real-time updates.
5. **Email Notifications**: Trigger email notifications on specific user actions.

## Readme File Content


# Rentify - Where Renting Meets Simplicity

## Introduction
Rentify is a platform designed to connect property owners with potential tenants. This README file provides instructions on setting up and running the Rentify application.

## Features
- User Registration and Login
- Seller: Post, View, Update, Delete properties
- Buyer: View properties, Express interest, Apply filters
- Pagination, Form Validation, Authentication
- Like button with real-time updates
- Email notifications

## Tech Stack
- **Frontend**: React
- **Backend**: Node.js with Express
- **Database**: MongoDB with Prisma
- **Authentication**: JWT with Cookies

## Setup Instructions

### Prerequisites
- Node.js
- MongoDB
- Prisma

### Installation

1. **Clone the repository**
   
   git clone https://github.com/shivamverma26/rentify_booking_app
   cd rentify

2. **Backend Setup**
cd backend
npm install
npx prisma generate
npm start

3. **Frontend Setup**
cd frontend
npm install
npm start

4. **Environment Variables**
Create a .env file in the backend directory and add the following:
DATABASE_URL=<your-mongodb-url>
JWT_SECRET=<your-jwt-secret>
EMAIL_SERVICE=<your-email-service>
EMAIL_USER=<your-email-user>
EMAIL_PASS=<your-email-pass>

5. **Running the Application**
Start the backend server: npm start (from the backend directory)
Start the frontend server: npm start (from the frontend directory)
Access the application at http://localhost:3000
