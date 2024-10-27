# AI-Enhanced Websites with LLM APIs

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

> **Figure:** Workflow for creating a new element in the Review Datatype

### Step 3: Calling the Gemini API for Sentiment Analysis

Immediately after storing the review, the workflow calls the **Gemini API** to analyze the sentiment of the submitted review. This API call is automatically triggered within the workflow for real-time processing of feedback.

The API is called with a dynamic prompt structured as follows:

**Prompt**:
> "You are a sentiment analysis tool. Analyze the sentiment of the following sentence and classify it as either 'positive,' 'negative,' or 'neutral.' Sentence: [User review taken dynamically]. Provide a one-word answer indicating the sentiment: positive, negative, or neutral."

In this prompt, the user review is dynamically inserted, allowing the system to adapt to various feedback. The Gemini API processes the review text and returns a one-word sentiment classification: positive, negative, or neutral.

> **Figure:** Calling Gemini API using Bubble workflow for Sentiment Analysis

### Step 4: Storing the Sentiment Result

Once the Gemini API returns the sentiment classification, the workflow updates the corresponding review entry in the database. The sentiment field is set based on the API response, allowing administrators to view the sentiment of each review through the Admin Panel.

### Step 5: Display in the Admin Panel

The Admin Panel is updated in real time to reflect new reviews and their associated sentiments, ensuring that administrators can quickly see how customers respond to their experiences. The system assigns a color code based on the sentiment:
- **Green** if the sentiment is positive, indicating satisfaction and positive feedback.
- **Red** if the sentiment is negative, highlighting areas where attention may be needed.

> **Figure:** The sentiment analysis page showing customer reviews. The top review was detected as positive, indicated by green, while the bottom review was classified as negative, indicated by red.

---

The **Sentiment Analysis** feature, implemented using the **Gemini API** within the **Bubble.io** platform, showcases how sentiment analysis can be seamlessly integrated into any website to enhance understanding of customer feedback and enable actions based on user insights.


