---
title: "微服務：優勢與挑戰 &ensp; Microservices: Benefits and Drawbacks"
date: 2023-10-17T09:00:00+08:00
draft: false
tags: ["System Design"]
---

| **Summary 摘要** | **Content 內容** | **Keywords 關鍵字** |
| --- | --- | --- |
| Microservices Definition <br>微服務架構定義 | Microservices architecture allows large teams to build scalable applications composed of many loosely coupled services. <br>微服務架構允許大團隊建立由許多松散耦合的服務組成的可擴展應用程序。 | Microservices, Loosely Coupled, Large Teams <br>微服務、松散耦合、大團隊 |
| Functional Domains <br>功能領域 | For instance, shopping cart, billing, user profile, push notifications can be separate microservices, sometimes referred to as domains. <br>例如，購物車、帳單、用戶資料、推送通知等都可以是單獨的微服務，這些功能區域有時被稱為域。 | Shopping Cart, User Profile, Domains <br>購物車、用戶資料、域 |
| Communication Methods <br>通信方式 | Microservices communicate through a mix of remote procedure calls (RPC), event streaming, or message brokers. <br>微服務之間通過遠程過程調用（RPC）、事件流或消息代理進行通信。 | RPC, Event Streaming, Message Brokers <br>RPC、事件流、消息代理 |
| Deployment & Scaling <br>部署和規模 | Microservices can be deployed separately, offering flexibility to independently scale each microservice. <br>微服務可以獨立部署，且提供更多的靈活性以獨立放大各個微服務。 | Independent Deployment, Scale, Flexibility <br>獨立部署、放大、靈活性 |
| Data Hiding <br>數據隱藏 | Well-designed microservices segment a monolithic database into its logical components, keeping each logical component concealed within its respective microservice. <br>良好的微服務架構會將單體數據庫分解為它的邏輯組件，並保持每個邏輯組件在其對應的微服務內隱藏。 | Data Concealment, Logical Components, Monolithic Database <br>數據隱藏、邏輯組件、單體數據庫 |
| Data Integrity Issues <br>數據完整性問題 | With the segmentation of the database, it can no longer maintain foreign key relationships or ensure referential integrity among these units. This burden is now shifted to the application layer. <br>由於數據庫的分解，數據庫不再能保持外鍵關係和實施這些單位之間的引用完整性，這負擔現在轉移到了應用程序層。 | Database, Foreign Key Relationships, Application Layer <br>數據庫、外鍵關係、應用程序層 |
| Microservices Components <br>微服務組件 | Key elements in microservices architecture include API gateways, identity validation services, and service registration and discovery services, among others. <br>微服務架構中的重要組件包括API網關、身份驗證服務、服務註冊和發現服務等。 | API Gateway, Identity Verification, Service Registration <br>API網關、身份驗證、服務註冊 |
| When to Use Microservices <br>使用微服務的時機 | The cost of microservices is high and makes sense primarily for large teams. While it promotes team independence, the overhead for a robust implementation is typically too substantial for small startups. <br>微服務的成本很高，只有對於大團隊才有意義，它使團隊獨立。但對小初創企業而言，通常不是一個好選擇。 | Large Teams, Independence, Startups <br>大團隊、獨立、初創企業 |
