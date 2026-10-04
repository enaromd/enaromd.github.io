---
layout: page
title: "Contact"
logo: "/assets/images/logo.png" 
hide_hero: true
permalink: contact/
lang: es

contact_section:
  title: "Ponte en contacto"
  subtitle: "Completa el formulario a continuación para enviarme un mensaje."
  access_key: "06da97ae-30e6-4475-bc31-15c9251a0ace"
  email_subject: "Nuevo mensaje desde el sitio web"
  
  # Button States (Passed to JavaScript)
  button_text: "Enviar mensaje"
  btn_sending: "Enviando..."
  btn_success: "¡Mensaje enviado!"
  btn_error: "¡Error! Inténtalo de nuevo"

  # Form Labels & Messages
  label_first_name: "Nombre"
  placeholder_first_name: "Juan"
  error_first_name: "Por favor, proporciona tu nombre."

  label_last_name: "Apellido"
  placeholder_last_name: "Pérez"
  error_last_name: "Por favor, proporciona tu apellido."

  label_email: "Correo electrónico"
  placeholder_email: "usuario@empresa.com"
  error_email: "Por favor, proporciona un correo electrónico válido."

  label_message: "Tu mensaje"
  placeholder_message: "Escribe tu mensaje aquí"
  error_message: "Por favor, escribe tu mensaje."

  social_title: "Conéctate conmigo"
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