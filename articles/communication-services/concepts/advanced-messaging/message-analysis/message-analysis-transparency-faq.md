---
title: Message Analysis transparency FAQ
titleSuffix: An Azure Communication Services Advanced Messaging concept
description: Learn about the Message Analysis transparency FAQ
author: gelli
manager: camilo.ramirez
services: azure-communication-services
ms.author: gelli
ms.date: 07/15/2024
ms.topic: conceptual
ms.service: azure-communication-services
ms.subservice: advanced-messaging
---

# Message Analysis: Responsible AI transparency FAQ 

[!INCLUDE [Public Preview Notice](../../../includes/public-preview-include-document.md)]

## What is Message Analysis? 

Message Analysis is an AI feature that analyses the incoming customer messages to extract insights that help developers enhance customer interactions. It detects the language, determines the intent (like a service question or complaint), and identifies key topics.  Message Analysis can help businesses understand how well their communication strategies are working and improve their interactions with customers. 

## What can Message Analysis do?  

Message Analysis leverages advanced AI capabilities with Azure OpenAI to offer multifaceted functionality for customer interaction. It uses Azure OpenAI services to process messages received through platforms like WhatsApp. Here’s what it does: 

* Language Detection: Identifies the language of the message, provides confidence scores, and translate the message into English if the original message isn't in English. 
* Intent Recognition: Analyzes the message to determine the customer’s purpose, such as seeking help or providing feedback. 
* Key Phrase Extraction: Extracts important terms and names from the message, which can be crucial for context. 

This combination of features enables businesses to tailor their responses and better manage customer interactions. 

## What are Message Analysis’s intended uses? 

* Providing Message Analysis for agents or departments helps businesses resolve issues efficiently and provide a seamless end-user experience. 

* Providing immediate feedback to customers by recognizing their needs. 

* Enhancing the efficiency of customer service teams by prioritizing messages based on urgency or emotion. 

* Improving the quality of customer interactions by understanding the context and nuances of their queries or comments. 

## How was Message Analysis evaluated? What metrics are used to measure performance? 

* Pre-Deployment Testing: 

   * Unit Testing: Develop and run unit tests for each component of the system to ensure they function correctly in isolation. 

   * Integration Testing: Test the integration of different system components, such as the interaction between the webhook receiver, Azure OpenAI API, and Event Grid. Testing helps to identify issues where components interact. 

* Validation and Verification: 

   * Manual Verification: Conduct manual testing sessions where team members simulate real-world use cases to see how well the system processes and analyzes messages. 

   * Bug Bashing: Organize bug bashing events where team members and stakeholders work together to find as many issues as possible within a short time. These events can help uncover unexpected bugs or usability problems.

* Feedback in Production: 

   * User Feedback: Collect and analyze feedback from end-users. This direct input can provide insights into how well the feature meets user needs and expectations. 

   * User Surveys and Interviews: Conduct surveys and interviews with users to gather qualitative data on the system’s performance and the user experience. 

## What are the limitations of Message Analysis? How can users minimize the impact of Message Analysis’s limitations when using the system? 

* False positives:  

   * The system may occasionally generate false positive analyses, particularly when dealing with ambiguous, conflicting, or sarcastic content, and culturally specific phrases and idioms from customer messages that it cannot accurately interpret. 

* Unsupported languages/ Translation Issues: 

   * If the model doesn't support the language, it can't be detected correctly or translated properly. There may also be misleading translations in the supported languages that you need to correct or build your own translation models. 

 

## Which operational factors and settings enable effective and responsible use of Message Analysis? 

* Explicit Meta-Prompt Components: Enhance the system's prompts with explicit meta-prompt components that guide the AI in understanding the context of the conversation better. This approach can improve the relevance and accuracy of the analysis by providing clearer instructions on what the system should focus on during its assessments. 

* Canned Responses for Sensitive Messages: Flags sensitive topics or questions in the analysis response. This helps ensure that replies are respectful and legally compliant, reducing the risk of errors or inappropriate responses generated by the AI. 

* Phased Release Plan: To gather feedback and ensure system stability, implement a staged rollout starting with a preview involving a limited user base before a full deployment. This phased approach enables real-time adjustments and risk management based on actual user experiences. 

* Update Incident Response Plan: Regularly update the incident response plan to include procedures that address the integration of new features or potential new threats. This strategy ensures the team is prepared to handle unexpected situations effectively and can maintain system integrity and user trust. 

* Rollback Plan: Develop a rollback strategy that enables quick reversion to a previous stable state if the new feature leads to unexpected issues. To ensure rapid response capabilities during critical situations, implement this strategy in the deployment pipelines. 

* Feedback Analysis: To gather actionable insights, regularly collect and analyze feedback from users, particularly from Contoso. This feedback is crucial for continuous improvement and helps the development team understand the real-world impact of the features, leading to more targeted and effective updates. 

## Next steps
- [Enable Message Analysis With Azure OpenAI Quick Start](../../../quickstarts/advanced-messaging/message-analysis/message-analysis-with-azure-openai-quickstart.md)
- [Handle Advanced Messaging events](../../../quickstarts/advanced-messaging/whatsapp/handle-advanced-messaging-events.md)
- [Send WhatsApp template messages](../../../quickstarts/advanced-messaging/whatsapp/send-template-messages.md)
