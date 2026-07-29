🎬 MovieBuff — GenAI Movie Recommendation Engine

An end-to-end movie recommendation system built entirely on Databricks, combining data engineering with generative AI. Ask for a genre, mood, or a movie you liked, and get personalized recommendations — along with exactly which streaming platform to watch it on, based on your country.

Currently supports: India 🇮🇳 and Ireland 🇮🇪 (easily extensible to more countries)

Features
🤖 Conversational chatbot interface — ask in plain English ("top 3 popular romance movies," "something like Inception," "best-rated horror films in Hindi")
🧠 Semantic recommendations powered by vector embeddings (Databricks Foundation Model APIs) — goes beyond simple genre-matching to understand mood and theme
📺 Country-specific OTT availability — real-time streaming platform data (Netflix, Prime Video, JioHotstar, MUBI, and more) normalized and deduplicated across ad-tiers and channel bundles
🌍 Language-aware filtering — defaults to English, supports filtering by original language
📊 Full medallion architecture (Bronze → Silver → Gold) built on Delta Lake for clean, scalable data pipelines
🔄 Resumable, checkpointed ingestion — handles 50,000+ movies from TMDB without data loss on interruption
Tech Stack
Platform: Databricks (Community Edition)
Data: TMDB API (movies, genres, watch providers)
Storage: Delta Lake
AI/ML: Databricks Foundation Model APIs (embeddings + LLM-based intent parsing)
Language: PySpark, Python