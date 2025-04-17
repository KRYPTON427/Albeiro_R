### Hi 👋! My name is Albeiro Ramos and I'm a tech education enthusiast and future technology teacher, from Bogotá, Colombia 🇨🇴

[![Python](https://img.shields.io/badge/Python-3.12+-yellow?style=for-the-badge&logo=python&logoColor=white&labelColor=101010)](https://python.org)
[![Made with ChatGPT](https://img.shields.io/badge/Made_with-ChatGPT-10a37f?style=for-the-badge&logo=openai&logoColor=white&labelColor=101010)](https://openai.com/chatgpt)
[![Bogotá](https://img.shields.io/badge/Based_in-Bogotá-ff5733?style=for-the-badge&logo=googlemaps&logoColor=white&labelColor=101010)](https://www.google.com/maps/place/Bogotá)
[![Reflex](https://img.shields.io/badge/Reflex-0.7.2+-5646ED?style=for-the-badge&logo=reflex&logoColor=white&labelColor=101010)](https://reflex.dev)

🚀 I'm passionate about using **technology and artificial intelligence** to transform education and inspire young minds.  
💡 Currently working on: An **OVA to teach Python and AI** to students in an engaging and accessible way.  
📚 Always learning: **Programming, AI, animation, drawing, and personal development**.  
💬 Ask me about: **EdTech, Python, AI for education, creative projects, and teaching strategies**.  
📫 How to reach me: rsalbeiro02@gmail.com  
⚡ Fun fact: I believe technology can change lives, and I dream of becoming a **recognized and inspiring teacher** who leaves a mark on students’ hearts.

> "La creatividad es la inteligencia divirtiéndose." – Albert Einstein
```yaml
FROM python:3.11

WORKDIR /app
COPY . .

ENV VIRTUAL_ENV=/app/.venv_docker
ENV PATH="$VIRTUAL_ENV/bin:$PATH"
RUN python3.11 -m venv $VIRTUAL_ENV

RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

CMD reflex run --env prod --backend-only
```
