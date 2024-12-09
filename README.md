import streamlit as st
from streamlit_lottie import st_lottie
import requests

# Find more emojis here: https://www.webfx.com/tools/emoji-cheat-sheet/
st.set_page_config(page_title="Programming Journey", page_icon=":computer:", layout="wide")

# Lottie animation function
def load_lottie_url(url: str):
    r = requests.get(url)
    if r.status_code != 200:
        return None
    return r.json()

# ---- HEADER SECTION ----
st.title("The Programming Journey 💻")
st.subheader("Exploring the World of Code and Software Development 🖥️")

# Lottie animation for welcome message
lottie_url = "https://assets3.lottiefiles.com/packages/lf20_o9x2ajqk.json"  # Lottie animation of coding (you can replace this URL)
lottie_animation = load_lottie_url(lottie_url)
if lottie_animation:
    st_lottie(lottie_animation, speed=1, width=700, height=400, key="welcome")

# Introduction
st.markdown("""
Welcome to the **Programming Journey**! 🎉  
Programming is a fascinating and rewarding skill, but it comes with its own challenges and learning curves. Whether you're just starting or a seasoned developer, the road to mastering programming is full of discovery and growth. Let’s dive into some aspects of learning to code and becoming a successful programmer! 👨‍💻
""")


st.markdown("""
## 🚀 The World of Programming

Programming is the art of writing instructions that a computer can understand and execute. Whether you're building websites, mobile apps, or artificial intelligence systems, programming is at the heart of it all. Here's what every programmer should know.

### 1. 💡 Learning the Basics

As a beginner, learning the fundamentals is key. Start with understanding basic concepts such as variables, loops, functions, and data types. Once you get the hang of these basics, you'll have a strong foundation to build upon. Don't worry if it seems overwhelming at first—every coder has been there! 😅

### 2. 🔄 Debugging and Problem-Solving

One of the most important skills in programming is debugging. Errors are inevitable, and learning how to troubleshoot and solve problems is essential. Debugging teaches you to be patient, creative, and systematic. Remember, every bug fixed is a step closer to being a better developer! 🐞🔧

### 3. 🌐 Exploring New Languages and Tools

There are many programming languages out there, such as Python, JavaScript, Java, and C++. Each language has its strengths, and learning different ones broadens your perspective. It's important to also explore libraries, frameworks, and tools that can make development easier and faster. Keep experimenting! 🚀

### 4. 🧠 The Power of Practice

Programming is a skill that improves with practice. The more you code, the better you'll get. Try building small projects, solving coding challenges, and contributing to open-source projects. Consistency is key! And don't forget to keep learning—new technologies and techniques are always emerging. 🏗️

### 5. 👥 Collaboration and Networking

Software development is rarely a solo activity. As a programmer, you'll often work in teams, collaborate with designers, product managers, and other developers. Networking with fellow coders can also help you stay up-to-date on the latest trends and find new opportunities. 💬🤝

## 🎯 Conclusion

Programming is a journey of continuous learning and improvement. It's okay to face challenges along the way—every setback is an opportunity to grow. Keep coding, keep building, and stay curious! 💻✨

Best of luck to all the future developers out there! 🍀
""")

# Lottie animation for conclusion 
lottie_url_end = "https://assets8.lottiefiles.com/packages/lf20_rikjpqjf.json"  # Lottie animation for conclusion (can be replaced)
lottie_animation_end = load_lottie_url(lottie_url_end)
if lottie_animation_end:
    st_lottie(lottie_animation_end, speed=1, width=700, height=400, key="conclusion")


st.markdown("---")


st.markdown("""
**Thanks for reading!** 😊  
Feel free to connect with me for any questions, collaborations, or discussions about programming. Let’s code the future together! 💡👨‍💻
""")
