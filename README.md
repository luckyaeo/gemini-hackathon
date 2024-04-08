# LET GIVE IT A GOOD NAME

## Motivation
Empower individuals and organizations with the necessary insights and management capabilities to make informed investment decisions. 

(1) Enhance financial literacy by providing users with insights into the workings of the stock market, investment strategies, and the implications of various financial decisions. 

(2) By making complex financial information more accessible and structured, demystify investing for the general public, potentially leading to greater financial inclusion. 

(3) On a personal level, effective portfolio management can lead to better financial outcomes for individuals, enabling them to achieve their financial goals, such as saving for retirement, education, or other personal projects that contribute to their well-being and that of their families.

(4) Incorporate environmental, social, and governance (ESG) criteria, enabling investors to make decisions that align with their ethical beliefs and contribute to sustainable development goals.

## Features

- Bot, Conversation Summary,
- Equity Research Report Generator
    - Analyze companies and projects for ESG performance.
    - **Investment Recommendations**: Suggest investments based on ESG scores and investor values.
- Portfolio Analysis Report Generator
    - **Impact Reporting**: Generate reports on the social and environmental impact of portfolios.
- PDF Uploader and Summarizer
    - Financial Report or News uploader

## Workflows

1. Portfolio construction workflow
    1. Understand User’s financial goals, risk preference and investment criteria. 
2. Equity research workflow. 
    1. Give user 5 categories to choose from: Qualitative, Quantitative, Financial Report, Sentiment, Framework. 
    2. The financial report category will allow user to upload PDF -  we will tokenize it and save to FAISS DB, which could be saved as a pickle file. 
    3. Generate informative content for investors, such as investment reports, company profiles, or sustainability impact assessments
    4. Enable users to ask questions such as "What are the environmental initiatives of Company X?" or "How does Project Y address social impact?"

## Tech Stack

1. Streamlit - fast prototyping
    1. For a more scalable solution, we might want to choose FastAPI + React + Tailwind.
2. Conversation memory: use application memory
    1. For a more scalable solution, we might want to choose Redis or CosmosDB
3. Vector Database: in memory database ChromaDB.
    1. For a more scalable solutoon, we might want to choose pgvector, Pinecone, CosmosDB(MongoDB API), Azure AI Search
4. Monitoring / Debugging: LangSmith
5. Tracing: Langfuse
6. Prompt Engineering: CoT, ReAct, RAG