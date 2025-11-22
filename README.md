# TravelGenie-AI
TravelGenie AI is an intelligent multi-agent travel planning system that automates the entire process of researching destinations, building day-wise itineraries, estimating budgets, recommending hotels &amp; food spots, and generating a beautifully formatted travel booklet.


#  🚩 Problem Statement

Modern trip planning is time‑consuming, fragmented, and overwhelming. Travelers must switch between dozens of websites, compare conflicting information, and manually assemble itineraries, budgets, and logistics.
     1. This results in:
     2. Information overload
     3. Poorly optimized itineraries
     4. Hidden costs
     5. Missed opportunities
     6. High cognitive load

### 💡 Solution

TravelGenie AI solves these challenges by using a coordinated team of agents that automatically research, analyze, generate, and refine a complete trip plan. Each agent specializes in a single responsibility, ensuring accuracy, depth, and consistency.
The output is a personalized, end‑to‑end itinerary ready for booking.

## 🌍✨ TravelGenie AI — Multi-Agent Intelligent Travel Planner
### 🧳 Overview

TravelGenie AI is an intelligent multi-agent travel planning system that automates the entire process of researching destinations, building day-wise itineraries, estimating budgets, recommending hotels & food spots, and generating a beautifully formatted travel booklet.
It acts as your personal travel concierge — researching, planning, comparing, and writing everything as if a professional travel agent did it for you.

The goal is to remove the friction of travel planning so anyone can get a high-quality, personalized trip plan within seconds.


### ✨ Motivation
Planning a trip today is time-consuming:

📌 Too many blogs to read

📌 Confusing hotel choices

📌 Hard to estimate budgets

📌 Managing dates, routes & timings manually

📌 Writing everything neatly is even harder

TravelGenie AI solves this by using LLM-powered agents and tool-augmented intelligence to completely automate the process.

You simply type:

➡️ “Goa 5” → Generate a 5-day Goa travel booklet
➡️ “Tokyo 7” → 7-day Japan experience plan

…and everything is instantly prepared.



### 🤖 System Highlights
TravelGenie AI includes at least three (3) of the required concepts from the course:

✔ Multi-Agent System
TravelGenie AI uses multiple specialized agents working together:

1. Research Agent
             Gathers destination info
             Uses search + curated sources
             Extracts best attractions, culture & travel rules
   
2. Itinerary Agent
             Converts raw research into structured plans
             Builds day-wise schedules
             Plans timings, travel modes & sequencing

3. Food & Stays Agent
             Recommends hotels
             Suggests must-try restaurants
             Adapts to travel preferences

4. Budgeting Agent
              Estimates total cost (stay + food + travel)
              Provides cost tiers

5. Booklet Writer Agent
              Formats the final plan
              Creates a polished travel booklet
              Adds narrative, tips & readability

All agents coordinate via the Coordinator Engine.



### 🧰 Tools & APIs Integrated
TravelGenie AI uses tool-augmented operations:

✔ Gemini 2.5 Flash Lite
For:
      reasoning
      structured writing
      final booklet generation
      itinerary planning logic

✔ Wikipedia Tool
For:
      destination facts
      cultural background
      notable landmarks

✔ Custom Code Tools
      date calculations
      metrics snapshot
      debugging logs



### 🧠 Memory & Context Engineering
TravelGenie AI uses:
✔ Session state (InMemorySessionService-style)
To recall:
           last topic typed
           user’s preferred travel style
           number of nights
           last generated cities

✔ Lightweight long-term memory
Stored in mem["user_prefs"].
This enables personalization:
            food type preferences
            budget sensitivity
            activity interests
            writing style preferences

✔ Context Compaction
          Before agent calls, context is filtered so only relevant facts are sent.
          This keeps generations fast and reduces API load.


### 📊 Observability
The system tracks:
          request count
          average response time
          failure logs
          agent-level metrics
With a snapshot_metrics() utility, the notebook displays a mini observability panel after each generation.


### 🧩 Architecture Overview
At a high level, TravelGenie AI follows this flow:

User Input → Topic Parser → Coordinator →  
    ├── Research Agent  
    ├── Itinerary Agent  
    ├── Meals & Stays Agent  
    ├── Budget Agent  
    └── Booklet Writer  
→ Final Travel Booklet + Booking Summary + Metrics
The system integrates API keys, libraries, and toolchains through a Config Engine similar to the diagram you provided (clean, minimal illustration style).


### 🏗 Technical Implementation
The user interacts through a simple UI built with:
          - ipywidgets (Text, Button)
          - IPython display tools
          - Try/except error pipeline
          - Live output window

The logic works like this:
1. The user types a topic:
     “Goa 5”
2. Input is parsed into:
     city="Goa"
     nights=5
3. A Coordinator orchestrates sequential agent calls.
4. Each agent returns structured JSON segments:
          - research_data
          - itinerary_data
          - hotel_recommendations
          - cost_breakdown

5. A final agent composes the booklet text.
6. Output is displayed + metrics snapshot printed.


### 📘 Example Output (Short Preview)

A TravelGenie booklet looks like this:

🌴 Welcome to Goa — Your 5-Day Tropical Escape!

Day 1 — Arrival + Candolim Exploration
         - Check-in
         - Dinner at Fisherman’s Wharf
         - Beach walk

Day 2 — North Goa Highlights
         - Fort Aguada
         - Calangute Beach
         - Nightlife in Baga

Day 3 — Island Adventures
         - Grande Island Snorkeling
         - Seafood lunch
         - Sunset cruise
          … and so on.

Booklet includes:

✔ day plans

✔ timings

✔ travel tips

✔ cultural notes

✔ weather expectations

✔ packing checklist

✔ safety guidance


### 🌟 Features That Make This Project Unique

✨ 1. Fully Automated End-to-End Travel Planning

No manual research.
No searching through 20 blogs.
Everything is generated in one click.

✨ 2. Clean, Aesthetic Architecture Visualization
             A custom-designed system architecture diagram
            (simple, colorful flat-style illustration) is included.

✨ 3. Customizable by User Input
           Just change the topic.
           Even dynamic names can be applied directly.

✨ 4. Multi-Agent Collaboration
          Agents specialize, communicate, and merge results logically.

✨ 5. Professional Travel Booklet Output
          Readable, polished, human-quality writing.

✨ 6. Built to Demonstrate Course Concepts
           - This project demonstrates mastery of:
           - Multi-agent pipelines
           - Tools with LLMs
           - Context engineering
           - State + session management
           - Observability metrics
           - Error handling
           - Notebook-based deployment


### 💡 Real World Value
TravelGenie AI is useful for:
           - Travel creators
           - Travel agencies
           - Frequent travelers
           - Trip planning apps
           - Students & families
           - Anyone overwhelmed by travel planning!

It can be extended into a commercial agent for:
           - PDF booklet export
           - Hotel API integration
           - Flight comparison tools
           - Real-time weather system
           - Group travel planning



### 🏆 Conclusion
TravelGenie AI transforms a traditionally manual, confusing, time-consuming task into a fully automated, intelligent, and enjoyable travel-planning experience.

✔ Multi-Agent

✔ Tool-Augmented

✔ Memory-Enabled

✔ Beautifully Designed

✔ Professional Travel Output

It embodies everything taught in the 5-Day AI Agents Intensive Course with Google, packaged into a real, practical, delightful project.
