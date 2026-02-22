# AI-Enhanced Bubble.io website with LLM APIs
**Created by Naveen Baburaj**  

Leveraging **LLM APIs** is an effective way to transform standard websites into interactive, AI-driven platforms. In this project, we demonstrate how LLM APIs can be seamlessly utilised to create powerful features like a chatbot and a sentiment analysis system, adding intelligence and engagement to the website with ease.

Through the LLM-powered chatbot, users enjoy real-time, responsive interactions, while the sentiment analysis system automatically processes feedback to uncover customer insights. This project showcases the versatility and efficiency of LLM APIs in building advanced, user-centered web features that enhance the overall digital experience.

---

## Liverpool Larder - A Showcase of LLM API-Enhanced Food Ordering Platform

**Liverpool Larder** is a sample food ordering website designed on **Bubble.io** to illustrate how **Large Language Model (LLM) APIs** can significantly enhance website interactions and functionality. This project utilizes the **Gemini API** to power **ChefBot**, an AI chatbot that assists users with personalized recommendations and answers to common queries, creating a seamless and interactive experience. Additionally, a **Sentiment Analysis System** analyzes user reviews to extract valuable feedback, helping the platform continuously improve its service.

[Click here to go to the Liverpool Larder website](https://liverpool-larder.bubbleapps.io/version-test)



**While the Gemini API is used here, similar results can be achieved with other LLM APIs, such as ChatGPT. These APIs offer versatile options for integrating intelligent features like chatbots, sentiment analysis, and personalized recommendations, making LLM technology an invaluable tool for enriching any website.**

---

### Website Creation Using Bubble.io

The **Liverpool Larder** platform was developed entirely on **Bubble.io**, which allowed for rapid and adaptable web development without requiring extensive coding knowledge. The choice of Bubble.io as the development platform was made to enable quick prototyping, easy modifications, and efficient management of both front-end and back-end components.

**Bubble Manual: https://manual.bubble.io/**

---

## Sentiment Analysis

The **Sentiment Analysis** feature was developed to help Liverpool Larder gain valuable insights into customer experiences. After placing orders, customers frequently leave feedback in the form of comments, offering insights into their likes and any areas needing improvement. However, manually analyzing this feedback can be time-consuming and inconsistent. By incorporating sentiment analysis, administrators can automatically assess the tone of each review—whether positive, negative, or neutral—enabling data-driven decisions to improve service quality.

### Implementation Approach Using Gemini API

The sentiment analysis system was implemented using the **Gemini API**, integrated within the **Bubble** platform to streamline the feedback analysis process. This setup allows for the automated categorization of customer comments, giving administrators actionable insights in real time.

- **Data Collection**: Feedback data is gathered whenever a customer leaves a comment. These comments are sent to the Gemini API through API workflows created in Bubble, ensuring feedback is collected and processed consistently without manual intervention.

- **Sentiment Analysis via Gemini API**: The feedback data is processed by the Gemini API, which applies **Natural Language Processing (NLP)** to analyze the text and determine sentiment. By examining key words, context, and phrases, the API classifies each review into one of three categories: positive, negative, or neutral. This approach leverages advanced AI algorithms, making the sentiment analysis accurate and reliable.

- **Integration with the Admin Panel**: The sentiment analysis results are displayed in the Admin Panel, allowing administrators to view a summary of customer sentiment. The integration with Bubble ensures that sentiment analysis outcomes are accessible and easy to interpret, enabling administrators to quickly assess overall feedback sentiment and address any emerging issues.

## Bubble Workflow for Adding a Review and Analyzing Sentiment

When a user submits a review on Liverpool Larder, a specific workflow is triggered to create a new entry in the system and analyze the sentiment of the feedback. This workflow ensures that user reviews are automatically processed, and the sentiment is categorized in real time. Below is a breakdown of how this workflow operates:

### Step 1: User Login Requirement

To ensure the integrity of the reviews and maintain accountability, only logged-in users are permitted to submit reviews. This step helps in reducing spam and fake reviews, ensuring that feedback comes from genuine customers who have placed orders through Liverpool Larder.

### Step 2: Creating a New Element in Review Data Type

Once the user submits their review, the workflow creates a new element in the "Review" data type. This entry stores all relevant details, including the text of the review, the user’s name, and a timestamp indicating when the review was submitted. This organization ensures that all reviews are properly cataloged for sentiment analysis and future reference.

![Screenshot](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss1.png)

> **Figure:** Workflow for creating a new element in the Review Datatype

### Step 3: Calling the Gemini API for Sentiment Analysis

Immediately after storing the review, the workflow calls the **Gemini API** to analyze the sentiment of the submitted review. This API call is automatically triggered within the workflow for real-time processing of feedback.

The API is called with a dynamic prompt structured as follows:

**Prompt**:
> "You are a sentiment analysis tool. Analyze the sentiment of the following sentence and classify it as either 'positive,' 'negative,' or 'neutral.' Sentence: [User review taken dynamically]. Provide a one-word answer indicating the sentiment: positive, negative, or neutral."

In this prompt, the user review is dynamically inserted, allowing the system to adapt to various feedback. The Gemini API processes the review text and returns a one-word sentiment classification: positive, negative, or neutral.

![Screenshot of ChefBot in action](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss2.png)

> **Figure:** Calling Gemini API using Bubble workflow for Sentiment Analysis

### Step 4: Storing the Sentiment Result

Once the Gemini API returns the sentiment classification, the workflow updates the corresponding review entry in the database. The sentiment field is set based on the API response, allowing administrators to view the sentiment of each review through the Admin Panel.

### Step 5: Display in the Admin Panel

The Admin Panel is updated in real time to reflect new reviews and their associated sentiments, ensuring that administrators can quickly see how customers respond to their experiences. The system assigns a color code based on the sentiment:
- **Green** if the sentiment is positive, indicating satisfaction and positive feedback.
- **Red** if the sentiment is negative, highlighting areas where attention may be needed.

![Screenshot of ChefBot in action](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss3.png)
![Screenshot of ChefBot in action](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss4.png)


> **Figure:** The sentiment analysis page showing customer reviews. The top review was detected as positive, indicated by green, while the bottom review was classified as negative, indicated by red.

---

The **Sentiment Analysis** feature, implemented using the **Gemini API** within the **Bubble.io** platform, showcases how sentiment analysis can be seamlessly integrated into any website to enhance understanding of customer feedback and enable actions based on user insights.

## Designing ChefBot – The Chatbot Powered by LLM

The purpose of **ChefBot** was to serve as a virtual assistant that guided customers through their food ordering process. ChefBot provided real-time assistance, answered user queries, and supported customers throughout their ordering journey. The chatbot’s design focused on making the experience as helpful, friendly, and efficient as possible.

### Implementation Approach Using Gemini API

ChefBot was implemented using the **Gemini API**, integrated with the **Bubble** platform to provide intelligent conversational capabilities. This integration allowed ChefBot to deliver a more natural and engaging interaction for users.

![Screenshot of ChefBot in action](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss5.png)

> **Figure:** The user asks a question about Liverpool Larder’s menu.

### Bubble Workflow for ChefBot

The ChefBot chatbot was developed to provide real-time assistance to users by answering questions about Liverpool Larder’s menu, including ingredients, pricing, and allergens.

- **Step 1: User Query Initiation**  
  Whenever a user types a question into the chat window, the workflow begins by preparing a prompt for the Gemini API. ChefBot uses a predefined prompt that includes current menu data, which is fetched dynamically from the database. This prompt is used for all questions to ensure consistency and accuracy.

  **Prompt Template**:
  > "You are an AI assistant named 'ChefBot' helping users with questions about Liverpool Larder cloud kitchen menu. Here is the current menu: [dynamic data which includes food name, price, ingredients]. Here is the user question: [the data filled by user in the input column]."

  The prompt is dynamically updated with the latest data from the menu data type, ensuring all responses reflect the most recent information.

- **Step 2: Call the Gemini API**  
  Once the dynamic prompt is ready, ChefBot makes an API call to the Gemini API.

  ![Screenshot of ChefBot in action](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss6.png)

  > **Figure:** Calling Gemini API using Bubble workflow for ChefBot

  **API Workflow in Bubble**: ChefBot is connected to the Gemini API through a Bubble workflow. The prompt, containing both the user’s question and current menu details, is sent to the Gemini API for processing. The Gemini API uses **Natural Language Processing (NLP)** to analyze the prompt and generate an appropriate response based on the user’s question.

- **Step 3: Receive and Display the Response**  
  After processing the prompt, the Gemini API returns a response, which ChefBot then displays to the user. The generated response is delivered in real time, providing the user with information regarding their query—such as the price of a dish, its ingredients, or any allergens.

- **Step 4: Handling Follow-Up Queries**  
  If the user asks a follow-up question or rephrases their initial query, ChefBot handles the new question in the same way, using the same workflow. ChefBot uses the same prompt structure each time a new question is asked. The only changes are the specific question asked by the user and the latest menu data from the database. The new question, along with the current menu data, is sent back to the Gemini API using the same workflow, ensuring consistency across all responses. This loop continues as long as the user keeps asking questions, providing consistent, comprehensive answers based on the latest menu information.

![Screenshot of ChefBot in action](https://raw.githubusercontent.com/Naveen-Baburaj/AI-Enhanced-Websites-with-LLM-APIs/main/ScreenShots/ss7.png)

  > **Figure:** User interacting with ChefBot

- **Step 5: Ending the Conversation**  
  Once the user is satisfied and stops interacting with ChefBot, the chat window remains available for any further questions. Users can close or minimize the chat window at any time. ChefBot will be available if the user decides to ask further questions later on.

---

## Conclusion

By leveraging **LLM APIs**, we can significantly enhance any website with minimal coding effort. This project demonstrated how to implement a **sentiment analysis tool** and a **chatbot**, transforming user interactions and feedback into valuable insights. However, the possibilities extend far beyond these examples. With the right dynamic prompts, LLM APIs can be utilized to create a wide range of intelligent, user-focused features, making websites more interactive, responsive, and valuable to their audiences.


