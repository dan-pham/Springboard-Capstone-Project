# Initial Project Ideas

## 1 - Chronic Disease Wellness and Education Platform

### Project Scope
A platform designed to support users with chronic conditions through personalized educational content and general wellness tips, without providing medical advice or diagnostics. The app will empower users make informed decisions about their lifestyle and wellness through education.

### Key features
- No account usage
    - Allows the user to use the platform without saving their information after the session ends
    - Provides a no obligation experience for the user
- User authentication and profile
    - Allow users to create an account to save their information and recommendations across sessions
    - User can enter basic information about themselves and select chronic conditions they are managing (e.g. diabetes, hypertension, arthritis)
    - User can select from a predefined list of common chronic conditions
    - Provides a personalized experience for the user
    - If saving personally identifiable information, must be HIPAA compliant
- Curated resource library
    - Provide a library of articles, videos, infographics tailored to each chronic condition
    - These resources will focus on general information, condition management tips, and lifestyle changes
- Dynamic content recommendations
    - Use prompt engineering to recommend content based on the user's conditions and interests
    - For example, a user managing diabetes might receive content on blood sugar-friendly diets, exercise routines, and stress management techniques
- Data privacy and security
    - Minimized data collection: Collect only the necessary data to provide personalized content and recommendations, and avoid storing sensitive health data
    - Clear privacy practices: Clearly communicate data usage policies and ensure that all data handling practices align with user privacy rights

### Potential features
- General wellness and lifestyle recommendations
    - Provide non-medical, general suggesionts that are beneficial to overall health and wellness, such as maintaining a balanced diet
- Habit tracking and goal setting
    - Allow users to set goals related to wellness activities (walking 10,000 steps, drinking 8 glasses of water a day, etc) and track their progress
- Interactive learning modules
    - Create interactive modules or quizzes to educate users about their condition
    - For example, a module on hypertension could explain how lifestyle factors like diet and exercise affect blood pressure, without suggesting specific treatments

### Technologies to use
- Frontend: React for building a responsive, user-friendly interface
- Backend: Node.js and Express for handling server-side logic
- Database: MongoDB for storing user profiles, wellness logs, and educational content
- AI/ML: Look into GPT3 or GPT4 prompt engineering for personalized recommendations 


## 2 - Marine Wildlife Sighting and Reporting Platform

### Project Scope
A platform designed for citizen scientists to report marine wildlife sightings, with AI-assisted species identification to increase accuracy.

### Key features
- No account usage
    - Allows the user to use the platform without saving their sightings after the session ends
    - Provides a no obligation experience for the user
- User authentication and profile
    - Allow users to create an account to save their sightings across sessions
    - User can enter basic information about themselves and their location
- Sight reporting interface
    - Easy-to-use form where users can report sightings of marine wildlife
    - The form should include options to upload photos, provide location data (via GPS integration), and add basic observations
- AI-assisted species identification
    - Integrate an AI model for species identification from uploaded photos
    - This model can provide suggestions or auto-identify common marine species based on visual input, reducing the reliance on user expertise

### Potential features
- Educational feedback
    - After reporting a sighting, users receive immediate feedback about the species they encountered, along with educational information about its conservation status and ecological role
- Basic data visualization and contribution tracking
    - Allow users to see a map of all reported sightings and track their contributions over time. This feature could include heatmaps to show sighting densities or patterns

### Technologies to use
- Frontend: React for building a responsive user interface
- Backend: Node.js and Express for handling server-side logic
- Database: MongoDB to store user profiles, sighting data, and species information
- AI/ML: Use a pre-trained image classification model (like TensorFlow.js or a custom-trained model on marine species) to assist in identifying species from user-uploaded photos