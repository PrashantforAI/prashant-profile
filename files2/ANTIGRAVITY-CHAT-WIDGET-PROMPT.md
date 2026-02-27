# Antigravity Prompt — AI Prashant Chat Widget

Add a floating chat widget to the existing page. This should feel like a premium live chat widget, dark themed, minimal, and on-brand.

---

## WIDGET BEHAVIOUR

- A floating button sits fixed at bottom-right of the page: 24px from bottom, 24px from right
- Button: 56px circle, background #A8E6CF, color #0A0A0A, contains a small chat bubble icon (use this SVG inline or a Unicode equivalent like 💬 or a clean custom SVG)
- On click: a chat panel slides up from the bottom-right with a smooth translateY animation (0.3s ease)
- Panel stays open until user clicks the × close button or clicks the floating button again

---

## CHAT PANEL DESIGN

Dimensions: 360px wide, 520px tall (on desktop). On mobile: full width minus 16px margin each side, height 70vh.

Structure top to bottom:

### Header
- Background: #111111
- Border-bottom: 1px solid #1A1A1A
- Left side: small circular avatar (24px) in #A8E6CF with initials "PM" in #0A0A0A, font-size 10px, font-weight 700
- Next to avatar: 
  - "Prashant Mishra" in 14px, font-weight 600, #F0F0F0
  - "AI version · usually instant" in 11px, #555555 below it
- Right side: × close button, color #555555, hover #F0F0F0, font-size 18px, background none, border none

### Messages Area
- Background: #0A0A0A
- Scrollable, flex-column, gap 12px, padding 16px
- Scrolls to bottom automatically on new message

Message bubbles:
- User messages: background #1A1A1A, color #F0F0F0, border-radius 12px 12px 4px 12px, align right, max-width 80%, padding 10px 14px, font-size 14px
- AI messages: background #111111, border 1px solid #1A1A1A, color #CCCCCC, border-radius 12px 12px 12px 4px, align left, max-width 85%, padding 10px 14px, font-size 14px

Typing indicator (show while waiting for response):
- Three dots animating (opacity pulse), same style as AI message bubble
- Label: "Prashant is thinking..."  in 12px #555555

### Opening Message
When the panel first opens, show this message automatically as an AI bubble (no API call needed, just render it):
"Hey 👋 I'm an AI version of Prashant — ask me anything about my work, projects, or what I'm looking for. I'll give you straight answers."

### Suggested Questions
Below the opening message, show 3 clickable pill buttons that auto-fill and send the question on click:
- "What have you built?"
- "What roles are you open to?"
- "How do you use AI in your work?"

Style: background #1A1A1A, border 1px solid #1A1A1A, color #A8E6CF, font-size 12px, padding 6px 12px, border-radius 100px, hover border-color #A8E6CF. Hide these pills once any message is sent.

### Input Area
- Background: #111111
- Border-top: 1px solid #1A1A1A
- Text input: background #0A0A0A, border 1px solid #1A1A1A, border-radius 4px, color #F0F0F0, font-size 14px, padding 10px 12px, flex-grow 1, focus border-color #A8E6CF, outline none
- Send button: background #A8E6CF, color #0A0A0A, border none, border-radius 4px, padding 10px 14px, font-weight 600, font-size 13px, cursor pointer, text "Send"
- Send on Enter key (without shift)
- Disable input and button while waiting for response

### Footer label inside panel
Very bottom of panel, centered, 10px, color #333333:
"AI · Powered by Gemini · Not the real Prashant"

---

## JAVASCRIPT LOGIC

Maintain a conversation history array in memory (resets when panel is closed and reopened):
```javascript
let chatHistory = [];
```

On each message send:
1. Add user message to chatHistory and render it
2. Show typing indicator
3. POST to /api/chat with body: { message: userInput, history: chatHistory }
4. On response: remove typing indicator, render AI reply bubble, add to chatHistory
5. Scroll messages to bottom
6. On error: show "Something went wrong — reach out at 735prashant@gmail.com" as an AI bubble

History format to send:
```javascript
chatHistory = [
  { role: "user", content: "What have you built?" },
  { role: "assistant", content: "I've built three live AI products..." }
]
```

---

## FLOATING BUTTON EXTRA DETAIL
- After 8 seconds on page, show a small tooltip above the button: "Ask me anything →" — background #111111, border 1px solid #1A1A1A, color #A8E6CF, font-size 12px, padding 6px 10px, border-radius 4px, fade in smoothly, auto-hides after 4 seconds or when chat opens

---

## IMPORTANT
- Do not use any external libraries for the chat — pure vanilla JS and CSS only
- Keep all existing page styles and functionality completely intact
- Add the widget HTML just before the closing </body> tag
- Add the widget CSS inside a new <style> block just before </body>
- Add the widget JS inside a new <script> block just before </body>
