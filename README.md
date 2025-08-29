import random
from datetime import date

topics = [
    "skincare tips",
    "makeup trends",
    "daily motivation",
    "healthy lifestyle",
    "special offer for customers",
    "new product launch",
]

styles = [
    "professional",
    "friendly",
    "funny",
    "motivational",
    "short & catchy",
]

templates = [
    "✨ {topic.capitalize()} ✨\nStay tuned! #beauty #lifestyle",
    "💡 Did you know? {topic.capitalize()} can change your day! 🚀",
    "📣 Attention! Today we talk about {topic} — don't miss it!",
    "🌸 Simple trick for {topic}: always stay consistent 💖",
    "🔥 Special content on {topic}! Available now. #trending",
]

def generate_content():
    topic = random.choice(topics)
    style = random.choice(styles)
    template = random.choice(templates)
    text = template.format(topic=topic)
    return f"[{style.upper()} STYLE - {date.today()}]\n{text}"

if __name__ == "__main__":
    print("=== CONTENT GENERATOR ===")
    for _ in range(3):
        print("\n" + generate_content())
