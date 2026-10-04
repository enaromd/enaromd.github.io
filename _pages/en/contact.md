---
layout: page
title: "Contact"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: contact/
lang: en

contact_section:
  title: "Get in Touch"
  subtitle: "Fill out the form below to send me a message."
  access_key: "06da97ae-30e6-4475-bc31-15c9251a0ace"
  email_subject: "New message from the web page"
  
  # Button States (Passed to JavaScript)
  button_text: "Send Message"
  btn_sending: "Sending..."
  btn_success: "Message Sent!"
  btn_error: "Error! Try Again"

  # Form Labels & Messages
  label_first_name: "First Name"
  placeholder_first_name: "John"
  error_first_name: "Please provide your first name."

  label_last_name: "Last Name"
  placeholder_last_name: "Doe"
  error_last_name: "Please provide your last name."

  label_email: "Email Address"
  placeholder_email: "you@company.com"
  error_email: "Please provide a valid email address."

  label_message: "Your Message"
  placeholder_message: "Enter your message here"
  error_message: "Please enter your message."

  social_title: "Connect with Me"
  social_links:
    - name: "LinkedIn"
      handle: "Enyel Rodríguez"
      url: "https://www.linkedin.com/in/enaromd/"
      icon: "fab fa-linkedin"

    - name: "GitHub"
      handle: "enaromd"
      url: "https://github.com/enaromd"
      icon: "fab fa-github"

    - name: "Threads"
      handle: "enaromd"
      url: "https://threads.net/@enaromd"
      icon: "fab fa-threads"

    - name: "X"
      handle: "enaromd"
      url: "https://x.com/enaromd"
      icon: "fab fa-x-twitter"
---

{% include contact.html %}