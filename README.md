# About:

Created an end to end personalised linkedin post generator based on FewShot prompt startegy to make authentic content around individual's niche along with parameters such as language, tag and size of the post.

## ARCHITECTURE:

**preprocess.py**:
Created a function that extract the content length, related tags, engagement and line count for each post using LLM and return the output in a structured JSON format.

**few_shots.py**:
Built a FewShot class that stores and categorise each post into its length, tag and language in a dataframe such that it automatically reterieve the post from df based on language, tag and length given.

**post_generator.py**:
It takes input from the user and give prompt along with example which automatically retreived from the previous posts based on given parameters passed by the user giving llm not only instruction but also increasing its
accuracy by giving related examples.
GroqAPI key is used and "llama-3.1-8b-instant" model is used.

**main.py**:
It is responsible for the UI design and streamlit is used to interact with user and generate the reqired linkedin post that is trained on users' own linkedin posts revolving around user's own unique style.
