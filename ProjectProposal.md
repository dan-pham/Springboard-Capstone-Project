# Chronic Disease Wellness and Education Platform Proposal

## Introduction
This project aims to develop a website specifically designed to support individuals with chronic conditions by offering personalized educational content and general wellness tips. Leveraging today’s advancements in technology, including AI-powered tools like GPT-3 or GPT-4, the website will tailor resources to meet the unique needs of each user through effective prompt engineering. While it will not provide medical advice or diagnostics, my goal is to equip users with the knowledge they need to enhance their well-being and manage their conditions effectively. By prioritizing education and wellness, this platform seeks to help users feel informed and empowered in their health journeys.

## Tech Stack
This project will be developed using the MERN (MongoDB, Express.js, React.js, Node.js) stack. By utilizing Javascript across the entire stack, the project is more manageable and it reduces context-switching between programming languages. The front-end will be built using React for a responsive, user-friendly interface. The backend will use Express for quick RESTful API development and Node to process real-time data to enhance user engagement. The database will be MongoDB, a NoSQL database designed to handle large volumes of data efficiently.

## Focus of the Project
The project will be a full-stack application, with an even focus across the entire stack. By developing each part of the stack, I will be able to provide an engaging user experience with an equally robust backend to handle all the data processing needed to meet and exceed user expectations. 

## Target Users
While chronic conditions can affect a wide range of age groups, they are typically seen in older adults, often aged 65 and above. To ensure the website is usable for them, I will be implementing basic accessibility features, like color contrast, alt text for images, text resizing, and focus indicators to highlight the current interactive element.

## Data Usage and Collection
For the purposes of this Capstone project, I will be using dummy data for testing instead of real health information. I will only gather the information necessary to showcase the app’s features, and I will inform users that the app is for demonstration purposes only and that no real data should be entered.

In my app, I will collect essential user profile data, including basic information like age, gender, and chronic conditions, to tailor personalized educational content and recommendations. By leveraging external health educational content APIs, I will provide users with relevant articles that align with their needs while minimizing data collection by only gathering necessary information and avoiding the storage of sensitive health data. I am committed to transparent privacy practices, ensuring that users are informed about data usage policies. 

## Project Plan
### Database Schema
- Users Collection
```swift
{
    "id": "ObjectId",
    "username": "String",
    "email": "String",             
    "password": "String",       
    "profile": {
      "age": "Number",              
      "gender": "String",           
      "chronicConditions": [          // Array of user's chronic conditions
        {
          "conditionId": "ObjectId", 
          "conditionName": "String" 
        }
      ],
      "preferences": {                // Array of interests for personalized content
        "contentInterests": [        
          "String"
        ]
      }
    },
    "createdAt": "Date",            
    "updatedAt": "Date" 
}
```

- Conditions Collection
```swift
{
    "id": "ObjectId",
    "name": "String",               
    "description": "String",        
    "resources": [                  // Array of resources associated with the condition
      {
        "resourceId": "ObjectId"    
      }
    ]
}
```

- Resources Collection
```swift
{
    "id": "ObjectId",
    "title": "String",              
    "type": "String",               // Article, video, image, etc     
    "content": "String",            
    "conditions": [                 // Array of conditions associated with the resource
      {
        "conditionId": "ObjectId"   
      }
    ],
    "tags": [                       // Tags for easier searching  
      "String"  
    ],
    "createdAt": "Date",            
    "updatedAt": "Date"             
}
```

### Sourcing Data
- User profile data: user input / dummy data
- Chronic conditions: user input / prefilled list of common conditions
- Resources: Educational resource APIs (Mayo Clinic, MedlinePlus Connect, Healthline)

### User Flows
- User Flow 1: No Account User
  - Landing Page
    - User visits the home page.
    - Action: Clicks on "Start Here" to enter the app.
  - Select/Enter Conditions
    - User is presented with a list of common chronic conditions.
    - Action: Selects one or more conditions (e.g., diabetes, hypertension).
    - Alternative: Can enter a custom condition in a text box.
  - Receive Recommendations
    - User is directed to a recommendations page.
    - Action: Sees personalized recommendations for educational resources based on selected conditions.
  - Explore Resources
    - User can browse through recommended articles, videos, and wellness tips.
  - End of Flow
    - User can choose to exit the app or return to the home page to select conditions again.
   
- User Flow 2: Account User
  - Landing Page
    - User visits the home page.
    - Action: Clicks on "Log In" or "Sign Up."
  - User Authentication
    - User enters credentials to log in.
    - Action: Successfully logs in.
  - Select/Enter Conditions
    - User is presented with a list of common chronic conditions.
    - Action: Selects one or more conditions.
  - Receive Recommendations
    - User is directed to a recommendations page.
    - Action: Sees personalized recommendations for educational resources.
  - Save Recommended Resources
    - User can click a "Save" button next to each recommended resource.
    - Action: Saved resources are stored in the user’s account.
  - End of Flow
    - User can choose to explore saved resources or log out.

- User Flow 3: No Account User with Signup Option
  - Landing Page
    - User visits the home page.
    - Action: Clicks on "Start Here."
  - Select/Enter Conditions
    - User selects one or more chronic conditions.
  - Receive Recommendations
    - User is directed to a recommendations page.
    - Action: Sees personalized recommendations.
  - Sign Up to Save Resources
    - User is prompted with a message: "Sign up to save your resources."
    - Action: Clicks on "Sign Up."
    - Alternative: Can choose to exit without signing up.
  - User Authentication
    - User fills in sign-up form.
    - Action: Successfully creates an account and is redirected to the recommendations page.
  - End of Flow
    - User can now save resources and explore the app.

- User Flow 4: Account User Viewing Saved Resources
  - Landing Page
    - User logs in to their account.
  - Dashboard
    - User is taken to their dashboard/home page.
    - Action: Sees options for viewing saved resources and new recommendations.
  - View Saved Resources
    - User clicks on "My Saved Resources."
    - Action: Sees a list of resources they have previously saved.
  - View New Recommended Resources
    - User clicks on "New Recommendations."
    - Action: Sees updated personalized recommendations based on selected conditions.
  - End of Flow
    - User can choose to explore saved resources or log out.

- User Flow 5: Account User Viewing General Wellness Tips
  - Landing Page
    - User logs in to their account.
  - Dashboard
    - User is taken to their dashboard/home page.
  - View General Wellness Tips
    - User clicks on "Wellness Tips."
    - Action: The app generates general wellness tips based on saved and recommended resources.
  - Explore Tips
    - User can browse through tips, which may include lifestyle changes, nutrition advice, and exercise recommendations.
  - End of Flow
    - User can choose to save tips, explore other areas of the app, or log out.

### Functionality
- No account usage
  - Users can use the website without registering
- User authentication and profile 
  - Users can create an account to save information
  - Users can fill out their profile for a tailored experience
- Resource library
  - Users can browse a collection of resources based on the chronic conditions they entered
- Content recommendations
  - Users can receive recommended resources based on the conditions and interests from their profile

### Tasks
| Task Name | Description | Labels |
|-----------|-------------|--------|
| Design database schema | Determine the models and database schema required | Documentation, Easy |
| Source data | Determine the APIs that will be used in the project | Documentation, Easy |
| User flows | Determine user flows | Documentation, Easy |
| Design basic mockups | Draft basic mockups with empty states, loading states, success states, error states | Documentation, Easy |
| Set up backend and database | Configure the backend and set up database | Backend, Medium |
| Set up frontend | Set up the frontend and link it to the backend with a simple API test call | Frontend, Easy |
| Set up home page | Set up chronic condition inputs | Frontend, Easy |
| Set up resource library | Use condition inputs to retrieve resources from APIs | Must have, Fullstack, APIs, Medium |
| Browse resource library | Open resource for viewing on the project website | Must have, Fullstack, APIs, Medium |
| Set up user authentication | Authenticate user (sign in, sign up) | Must have, Fullstack, Easy |
| Set up user profile | Save user profile information | Must have, Fullstack, Easy |
| Save resources | Save resources to user profile | Must have, Fullstack, Easy |
| Recommend resources | Recommend resources based on user’s conditions and saved resources | Must have, Prompt Engineering, Medium |
| Basic accessibility | Color contrast, alt text for images, text resizing, and focus indicators to highlight the current interactive element | Must have, Frontend, Easy |
| Basic HIPAA Compliance | Obtain user consent, clearly display privacy policy, check third-party compliance with HIPAA | Must have, Frontend, Easy |
| Testing | Perform unit testing for API endpoints and integration testing between frontend and backend | Must have, Fullstack, Medium |
| Security | Hashing password, encrypting sensitive data | Must have, Backend, Hard |
| Recommend wellness tips | Recommend tips based on user’s conditions and saved resources | Stretch goal, Prompt Engineering, Easy |
| Interactive quizzes | Create simple true/false or 2-answer-choice quizzes based on user’s conditions and opened, saved resources. Show the resource that was used to create the question so the user can learn more | Stretch goal, Frontend, Medium |
| Intermediate accessibility | Keyboard navigation for forms (Tab to go to next field, Enter to submit) | Stretch goal, Frontend, Medium |
| Advanced accessibility | Screen reader compatibility | Stretch goal, Frontend, Hard |
| Intermediate HIPAA compliance | Data anonymization, Strict access controls | Stretch goal, Backend, Medium |
| Advanced HIPAA compliance | Data encryption - in transit (HTTPS), at rest (encrypt stored data on database), Audit trails | Stretch goal, Backend, Hard |
