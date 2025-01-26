# Hiring-Challenge---Website-Builder-with-AI-Chatbox-Integration

EventNook is hiring for talented software engineers based in Vietnam to help them build the new products integrated into the core product. Engineers are invited to submit the solution to below challenge. There is a 2nd challenge at this link https://github.com/thsonvt/Hiring-Challenge----Facial-Recognition/tree/main. You are welcome to attemp both challenges or you can just decide which challenge to take part. Cash award for the winner of each challenge is SGD 500

The CEO will be at the AI BuildCamp Demo Day on the morning of 22/02/2025 to talk about his company and the challenge in details. Interested candidates can speak to him at th event. Here is the event details https://lu.ma/x2a7cxn7

# Deadline for submission - 22/03/2025 23:59


Simple Website Builder with AI Chatbox Integration

## 1. Overview
This application is a conversational website builder enabling users to transform raw, unstructured data into visually appealing and functional web sections using chat prompts. The AI-powered chatbox is the core interaction method, allowing users to input raw information (e.g., from Google Docs or plain text), which the system processes and transforms into structured, visually styled HTML templates.

## 2. Functional Requirements
### 2.1. Core Features
#### AI-Powered Chatbox:
Allows users to interact with the system to create, modify, and customize webpage sections.
Accepts raw, unformatted information (e.g., text copied from Google Docs).
Responds with a neatly formatted UI section (HTML/CSS) based on user prompts.
Handles iterative prompts, allowing users to refine the output (e.g., "Make it two columns" or "Add more space between items").

#### Raw Data Transformation:
Processes unstructured text (e.g., event details, speaker bios) into well-structured, semantic HTML.
Maps raw data fields to pre-designed templates (e.g., speaker name, bio, photo URL).
Validates and cleans user input to ensure it aligns with template requirements.

#### Pre-Trained Templates:
Includes ready-to-use templates for common event-related sections, such as:
Event Speakers List: Displays speaker names, titles, bios, and photos.
Event Agenda: Formats session details with time, title, and descriptions.
Other Layouts: Headers, footers, galleries, and contact forms.
Offers multiple layouts and styles for each template (e.g., grid vs. list for speakers).

#### Customizable Outputs:
##### Users can:
Select a specific template layout via the chatbox.
Provide styling preferences (e.g., "Make it a dark theme").
Refine or override the generated HTML using further prompts.
##### Live Preview:
Displays real-time updates of the webpage as users interact with the chatbox.
Automatically applies generated HTML/CSS to the preview.
#####  Template Saving and Reuse:
Allows users to save generated sections as templates for future use.
Saved templates can be tagged and categorized for easy retrieval.
Supports incremental training to improve template generation based on saved data.
### 2.2. User Workflow
#### Data Input:
Users copy raw information (e.g., speaker list) and paste it into the chatbox.
Example: "Create an Event Speaker section from this list" with the pasted data.
Template Selection and Output:
The AI suggests or applies a relevant template.
Generates HTML/CSS for the requested section with default styling.
#### Refinement:
Users refine the output by providing additional prompts (e.g., "Center-align the speaker names," "Add padding around photos").
#### Preview and Edit:
Users view the live preview and tweak the section further if needed.
Advanced users can edit the HTML/CSS directly via the editor.
Save and Export:
Users save the section for reuse or export the final webpage as an HTML/CSS file.

## 3. Non-Functional Requirements
#### Performance:
Real-time responses from the chatbox for smooth user experience.
Efficient data transformation for large or complex inputs.
#### Scalability:
Supports concurrent users and high traffic through AWS auto-scaling.
Efficiently manages stored templates and projects in Amazon DynamoDB.
#### Security:
Protects user data with AWS encryption standards.
Ensures secure interactions with HTTPS and JWT-based user authentication.
#### Reliability:
High uptime using AWS infrastructure.
Backup and recovery for saved projects and templates.

## 4. Technical Stack
#### Front-End:
Framework: Vue.js or React.js.
Styling: TailwindCSS.
Live preview with dynamic rendering.
Back-End:
Framework: Node.js (Express.js for RESTful APIs).
Real-Time Communication: Socket.IO for live updates.
AI Integration: OpenAI API for natural language processing and data transformation.
#### Database:
Amazon DynamoDB for storing user projects, templates, and metadata.
#### Storage: Amazon S3 for saving assets like images and exported files.
Hosting:
AWS Elastic Beanstalk or AWS Lambda for back-end services.
Static assets served via Amazon CloudFront.
AI
OpenAI or Gemini

## 5. Example Use Cases
Use Case 1: Create an Event Speaker List
Input: "Here’s a list of speakers: Alice Smith, CEO, Innovate Inc. John Doe, CTO, Future Tech."
Process:
Chatbox recognizes names, titles, and companies.
Outputs a structured HTML speaker list with images as placeholders.
Refinement: User prompts, "Add photos for Alice and John," and uploads image URLs.
Use Case 2: Format an Event Agenda
Input: "Session 1: Opening Keynote, 9 AM. Session 2: Panel Discussion, 11 AM."
Process:
Chatbox generates a timeline-style agenda.
Applies styling like colors, borders, and fonts based on default template.
Refinement: User prompts, "Highlight the keynote session in bold."

## 6. Future Enhancements
Add support for AI-driven bulk imports (e.g., Excel files for speaker lists).
Integrate a visual drag-and-drop editor for non-technical users.
Extend template customization with saved user preferences.
Enable collaborative editing and feedback on shared projects.
