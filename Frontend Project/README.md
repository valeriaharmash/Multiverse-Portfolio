<h1>QuizApp</h1>

> The Trivia QuizApp, built with JavaScript and React, offers an engaging experience where users can select different categories to answer trivia questions. It utilizes React's context and reducer to manage game state, including tracking the current question, selected answers, and scores. The app leverages local storage to save the user's progress and chosen category, ensuring a seamless experience even after page reloads. With dynamic answer shuffling, each round of trivia feels fresh and challenging.

## Users:
Trivia enthusiasts or anyone looking to engage in a fun and interactive quiz experience.

## Key Functions for Users:
The app serves as an entertaining and educational tool, allowing users to challenge themselves with trivia questions, learn new information, and track their progress through scores. It also provides a casual and enjoyable way to pass the time.

## Key Features:
- Category Selection: Users can choose from different trivia categories based on their interests.
- Randomized Questions: Questions are shuffled to provide a unique experience each time.
- Immediate Feedback: Users receive instant feedback on their answers, showing correct or incorrect responses.
- Score Tracking: The app tracks users' scores.
- State Persistence: Progress is saved using local storage, so users can continue where they left off even after closing the app.

## Personal Contributions: 
**S** - I developed a trivia app to create an engaging and educational experience for users who enjoy testing their knowledge on various topics. I wanted to build a project that not only challenged my technical skills but also resulted in a fun and functional product that could be enjoyed by others.

**T** - Before building the app, I planned its structure, focusing on a user-friendly interface and responsive design. The application is divided into several components: the home page, where users can select categories; the quiz component, which presents the questions; and the results component, which summarizes the user’s performance. I utilized React's context API to manage state across the application, ensuring that data like selected categories, questions, and user answers were consistently accessible. The design process included brainstorming user flows, mapping out component hierarchies, and sketching wireframes to visualize the interface.

**A** - To implement the app, I used React's useReducer hook within a context provider to handle state management, which allowed me to efficiently update and track the user's progress throughout the quiz. The home page component enables category selection, which triggers the filtering of questions based on the selected category. In the quiz component, I implemented logic to shuffle answer options and determine the correctness of the user's selections. The result component provides feedback on the user’s performance and allows them to restart the quiz or return to the main menu. I also leveraged localStorage to preserve the user’s progress even if the page is refreshed.

**R** - The final application is a fully functional trivia quiz game that offers users a smooth and interactive experience. Users can choose from various categories, answer a series of questions, and receive immediate feedback on their performance. The app dynamically updates the score and tracks the number of correct answers, providing a clear summary at the end of the quiz. The intuitive design and responsive layout ensure that the application is accessible and enjoyable on various devices, fulfilling the goal of creating an engaging and educational tool.

[Check out the QuizApp on GitHub](https://github.com/React-Quiz-App/QuizApp)

### Landing Page:
<img width="1666" alt="Screenshot 2024-08-15 at 12 07 19 PM" src="https://github.com/user-attachments/assets/9df7943d-96f7-44e9-ac12-9bb1487849bc">

### If answered correctly:
<img width="1658" alt="Screenshot 2024-08-15 at 12 07 51 PM" src="https://github.com/user-attachments/assets/60a2b0a7-a9e8-4131-8908-274c2d3ec477">

### If answered incorrectly:
<img width="1654" alt="Screenshot 2024-08-15 at 12 08 17 PM" src="https://github.com/user-attachments/assets/11a9b481-950d-40a3-8c02-b695b19999fb">

### Score:
<img width="1659" alt="Screenshot 2024-08-15 at 12 08 58 PM" src="https://github.com/user-attachments/assets/d0adc3cc-0d59-42b5-974e-fa4f752afff8">

## Technologies
- Language: `JavaScript`
- Runtime:`Node.js`
- Framework: `React`
- UI Library: `MUI (Material-UI)`
- State Management: `Redux Toolkit`
- Routing: `React Router DOM`

## Competencies

### JF 2.5: Can implement a responsive User Interface
##### Situation:
While developing the Quiz App, I aimed to create an engaging and accessible experience for users across various devices, including desktops, tablets, and smartphones. A responsive User Interface was crucial to ensure that the app was usable and visually appealing on any screen size.
##### Actions:
To achieve this, I took the following steps:
- Responsive Design: I utilized CSS Flexbox and Grid layout techniques to create a flexible layout that adjusts to different screen sizes.
- Media Queries: I implemented media queries in the app's CSS to handle specific breakpoints, ensuring the layout, font sizes, and button spacing adapt appropriately on smaller screens.
- Material-UI Components: I incorporated Material-UI components, which are inherently responsive and provide a consistent design language across devices.
##### Results:
As a result of these actions, the Quiz App delivered a smooth and responsive experience across all tested devices. The layout remained intuitive and user-friendly, regardless of screen size. This improved the overall user experience, making the app accessible to a broader audience.
##### Connection to Project: 
This project showcased my ability to implement a responsive UI, resulting in a more inclusive and adaptable product that effectively meets user needs across various devices.
