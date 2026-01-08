---
enable: true # Control the visibility of this section across all pages where it is used
title: "¿Tienes algún proyecto en mente?"
description: "¡Genial! Estamos emocionados de escucharte y empezar algo juntos"

# image: "/images/about-us/about-one.jpg"
# imagePosition: "left" # Choose between "left" or "right"

map:
  enable: true
  position: "right" # Choose between "left" or "right"
  title: "Mapa de New Work City"
  url: https://maps.google.com/maps?width=100%25&amp;height=600&amp;hl=es&amp;q=1%20Grafton%20Street,%20Dublin,%20Ireland+(My%20Business%20Name)&amp;t=&amp;z=14&amp;ie=UTF8&amp;iwloc=B&amp;output=embed # Embed map iframe URL generated from https://www.maps.ie/create-google-map/

# Check config.toml file for form action related settings
# this is also used in the footer of the personal portfolio homepage
form:
  emailSubject: "Nuevo envío de formulario desde el sitio web" # Customized email subject (applicable when anyone submit form, form submission may receive by email depend on provider)
  submitButton:
    enable: false
    label: "ENVIAR MENSAJE"

  # This note will show at the end of form
  # note: |
  #   Your data is safe with us. We respect your privacy and never share your information. <br /> Read our [Privacy Policy](/privacy-policy/).
  inputs:
    - label: ""
      placeholder: "Nombre completo *"
      name: "Full Name" # This is crucial. Its indicate under which name you want to receive this field data
      required: true
      halfWidth: true
      defaultValue: ""
    - label: ""
      placeholder: "Correo electrónico *"
      name: "Email Address" # This is crucial. Its indicate under which name you want to receive this field data
      required: true
      type: "email"
      halfWidth: true
      defaultValue: ""
    - label: ""
      placeholder: "Asunto *"
      name: "Subject" # This is crucial. Its indicate under which name you want to receive this field data
      required: false
      halfWidth: true
      dropdown:
        type: "" # select | search - default is select
        search:
          placeholder: ""
        items:
          - label: "Consulta general"
            value: "General Inquiry"
            selected: false
          - label: "Oportunidad de colaboración"
            value: "Partnership Opportunity"
            selected: false
          - label: "Oportunidad de inversión"
            value: "Investment Opportunity"
            selected: false
    - label: ""
      placeholder: "Asunto con búsqueda *"
      name: "Subject With Search" # This is crucial. Its indicate under which name you want to receive this field data
      required: false
      halfWidth: true
      dropdown:
        type: "search"
        search:
          placeholder: "Asunto con búsqueda"
        items:
          - label: "Consulta general"
            value: "General Inquiry"
            selected: false
          - label: "Oportunidad de colaboración"
            value: "Partnership Opportunity"
            selected: false
          - label: "Oportunidad de carrera"
            value: "Career Opportunity"
            selected: false
          - label: "Oportunidad de inversión"
            value: "Investment Opportunity"
            selected: false
          - label: "Consulta de medios"
            value: "Media Inquiry"
            selected: false
    - label: ""
      tag: "textarea"
      defaultValue: ""
      rows: "2" # Only work if tag is textarea
      placeholder: "¿Cómo podemos ayudarte? *"
      name: "Message" # This is crucial. Its indicate under which name you want to receive this field data
      required: true
      halfWidth: false
    - label: "Google Search" # only valid for type="checkbox" & type === "radio"
      checked: false
      name: "User Source"
      required: true
      groupLabel: "¿Cómo te enteraste de nosotros?"
      group: "source"
      type: "radio"
      halfWidth: true
      defaultValue: ""
    - label: "Redes Sociales" # only valid for type="checkbox" & type === "radio"
      name: "User Source"
      required: true
      groupLabel: ""
      group: "source"
      type: "radio"
      halfWidth: true
      defaultValue: ""
    # - label: "Referral"
    #   name: "User Source"
    #   required: true
    #   groupLabel: ""
    #   group: "source"
    #   type: "radio"
    #   halfWidth: true
    #   defaultValue: ""
    # - label: "Other"
    #   name: "User Source"
    #   required: true
    #   groupLabel: ""
    #   group: "source"
    #   type: "radio"
    #   halfWidth: true
    #   defaultValue: ""
    - label: "Acepto los términos y condiciones." # only valid for type="checkbox" & type === "radio"
      id: "privacy-policy"
      name: "Agreed Privacy"
      value: "Agreed"
      checked: false
      required: true
      type: "checkbox"
      halfWidth: false
      defaultValue: ""
    - note: success
      parentClass: "hidden text-sm message success"
      content: "¡Hemos recibido tu mensaje! Te responderemos lo antes posible."
    - note: deprecated
      parentClass: "hidden text-sm message error"
      content: "¡Algo salió mal!"
---
