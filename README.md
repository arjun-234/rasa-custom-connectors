# Rasa and Instagram: A Chatbot Love Story

*How Rasa’s Conversational Magic Transforms Instagram Engagement*

![image](https://github.com/arjun-234/rasa-custom-connectors/assets/103405661/e3a5be83-7b28-44cf-b274-c3b4c40fc3d0)

## Introduction

In today’s digital age, chatbots are becoming increasingly popular for businesses and individuals alike. They provide a convenient and efficient way to interact with users, answer questions, and offer assistance. However, the capabilities of chatbots are often limited to text-based platforms. What if you want to extend your chatbot’s reach to a platform like Instagram? In this guide, we'll explore how to build an Instagram connector for Rasa chatbots, allowing you to engage with users on this visually-oriented social media platform.

## Why Instagram for Chatbots?

Instagram is one of the most popular social media platforms, boasting billions of users worldwide. It’s primarily focused on visual content, making it an ideal platform for showcasing products, services, and engaging users with images and videos. By integrating a chatbot with Instagram, you can provide a more interactive and personalized experience for your followers.

## Building the Instagram Connector

Before we dive into the steps, we have great news for you. We’ve already built a custom Instagram connector that you can easily incorporate into your Rasa chatbot project. This connector streamlines the process and ensures a smooth integration with Instagram. You can find our Instagram connector on [GitHub](https://github.com/arjun-234/rasa-custom-connectors).

### Now, let’s outline the general steps to get you started:

1. **Copy the connector code**: Begin by copying the connector code provided on [GitHub](https://github.com/arjun-234/rasa-custom-connectors). Once you’ve copied the code, navigate to your project directory and paste it there.

2. **Import the connector in** `credentials.yml`: Add the following snippet to your `credentials.yml` file, importing the InstagramInput class and providing the necessary parameters:

   ```yaml
   rasa-custom-connectors.instagram.InstagramInput:
     verify: "verify-token"
     secret: "app-secret-key"
     page-access-token: "page-access-token"
    ```
  - ***verify***: containing a string of your choice.
  - ***secret***: locate the App Secret in the app dashboard under **Settings → Basic**.
  - ***page-access-token***: navigate to your app’s dashboard. In the Products section, locate the **Messenger→Instagram settings** and click Set Up. Here, you can create or choose the page you wish to link with your chatbot. Once the setup is successful, simply click the **Generate Token** button, and the token displayed will be your `page-access-token`.

3. **Configuring the webhook**: Set up the webhook by configuring it with a minimal selection of the messaging and messaging_postback subscriptions. Insert your callback URL, which should follow this format: `https://<host>:<port>/webhooks/instagram/webhook`. Ensure you replace **host** and **port** with the correct values corresponding to your running Rasa server. Additionally, make sure to insert the **Verify Token**, ensuring it matches the `verify` entry in your `credentials.yml`.

4. **Testing and iteration**: To ensure your chatbot functions correctly on Instagram, initiate testing and iteration. Begin by sending a message from your designated test user account to your Instagram account. This action will trigger the chatbot to initiate and respond.

***Please Note***: To test the chatbot, use the Instagram account of your Meta test user. Ensure that the test user’s Facebook and Instagram accounts are linked together.

By adhering to these steps, you can effectively establish the connection and conduct testing for your Instagram chatbot in development mode.

### Conclusion
To sum up, by building an Instagram connector for your Rasa chatbot, you can tap into the vast audience of Instagram users, providing them with a more interactive and engaging experience. This opens up new opportunities for businesses, brands, and individuals to connect with their followers, answer questions, and showcase products or services.
