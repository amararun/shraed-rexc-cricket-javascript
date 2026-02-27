> [\!NOTE]
> This repository is a working example of the concept described below. It may not yet include all recommended security hardening measures. My newer repositories now have robust security at both frontend and backend layers — rate limiting, SQL validation, concurrency controls, error sanitization, and more. You can use this repo to understand the core concept, but please apply security best practices before deploying to production. See my [80+ item Security Checklist](https://tigzig.com/security) and [live hardened examples](https://tigzig.com/security-examples) for reference.

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" height="25">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" height="25">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" height="25">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" height="25">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" height="25">
  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" height="25">
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" height="25">

</p>


# REX-C: Cricket Data Analytics - AI Assistant - With Real-time Voice

A single-page JavaScript application for cricket analytics with AI chat capabilities. This app provides an interactive interface for analyzing cricket data, featuring AI-powered chat, data visualization, and document viewing capabilities.

---

## Key Features

🤖 **AI Chat Assistant**: Engage with an intelligent AI chatbot for real-time cricket data analysis and insights.  
🎙️ **Real-time Voice Interaction**: Supports seamless voice-based queries and responses powered by ElevenLabs.  
📈 **Python-Powered Statistical Processing**: Perform statistical computations directly in-app (text mode only)
📊 **Dynamic Python Charts**: Visualize  cricket data with python charts.  
📂 **Google Docs Integration**: Push or update conversation and query data into Google Docs
🔗 **Connects to Any Database**: Integrates with data warehouses or custom databases for large-scale analysis.  
⚡ **Single-Page Design**: Built entirely with HTML, CSS, and JavaScript for fast and responsive performance.  
🌐 **Deploy Anywhere**: Easily deployable on platforms like Vercel, Netlify, or custom cloud setups.  
🗃️ **Detailed Documentation**: Step-by-step deployment guides with video tutorials for easy replication.  


---

## Video Guides

🎥 **Video walkthroughs for setup and usage**:  
Refer to these detailed guides for granular, step-by-step instructions. The links also have time-stamps table of contents so you can directly jump to the section you need.

1. **REX-V**: AI Analytics Assistant V2. Execute tasks, automate reports, analyze data with voice and text instructions.  
   [https://link.tigzig.com/anly5pt](https://link.tigzig.com/anly5pt)  

2. **REX-A**: Build AI apps to connect to any database, create new databases on the fly, and upload text files.  
   [https://link.tigzig.com/rex2HowTo](https://link.tigzig.com/rex2HowTo)  

3. **REX-R**: Build & deploy real-time API analytics assistant systems.  
   [https://link.tigzig.com/realtGuide](https://link.tigzig.com/realtGuide)  

4. **REX-D**: Build & deploy a data analytics assistant system connected to a Data Warehouse.  
   [https://link.tigzig.com/dataLLM](https://link.tigzig.com/dataLLM)

5. **Leon Van Zyl**: For anything Flowise, Leon's videos are the best. Also for ElevenLabs voice widget setup as well as ElevenLabs custom build with its SDK
   [https://www.youtube.com/@leonvanzyl](https://www.youtube.com/@leonvanzyl)

6. **Volo Builds**: Best videos on using Cursor AI for full stack apps. 
   [https://www.youtube.com/@VoloBuilds](https://www.youtube.com/@VoloBuilds)

7. **Nick Sarev**: Nick's videos are the best for anything Make.com.
   [https://www.youtube.com/@NickSarev](https://www.youtube.com/@NickSarev)


---

## Step-by-Step Deployment Process

The steps below guide you to deploy the application **as-is**. Customize it further once deployed.

---

### Step 1: 🚀 Quick Deploy

- Clone the repo.  
- Deploy using platforms like **Vercel** or **Netlify**, or any other hosting platform.  
- This sets up the application with pre-configured endpoints for testing. Plug in your custom components later.

---

### Step 2: 🛠️ LLM Agent and Tools Setup

- Use **Flowise** or any other LLM agent builder. You’ll need an API endpoint for your agent.  
- JSON schemas for replicating agents and tools are available in the `docs` folder.  
- After importing the schemas:
  - Replace the **FastAPI URL** in the database connection tool with your own.  
  - Replace the **Make.com webhook URL** in the document update tool with your own.

Refer to the guides and videos for step-by-step instructions on setting up LLM Agents in Flowise or Make.com scenarios. For deeper dive, Leon Van Zyl's videos are the best for Flowise and Nick Sarev's for Make.com. Links on top.

---

### Step 4: 🗄️ Set Up Your Database  

- Use any PostgreSQL database. This example uses Aiven.  
- Refer to the REX-A video guide for setting up a database on Aiven in minutes.  
- Update your database credentials in the environment variables of the FastAPI server repo.  

---

### Step 5: 📂 Upload Data to Your Database  

- Download the `odi.txt` file:  
  [https://drive.google.com/drive/folders/1VHD9UzeYaJF_dBPecnjucHpoGocf4IvR](https://drive.google.com/drive/folders/1VHD9UzeYaJF_dBPecnjucHpoGocf4IvR)  
- Upload it using:  
  - **rex.tigzig.com** (via your database credentials).  
  - **Python/JavaScript scripts** or tools like **DBeaver**.  

---

### Step 6: 📥 Get Updated Data (Optional)

- `odi.txt` is current as of **6th Dec 2024**. For updated data:  
  - Download the latest ZIP from Cricsheet.org:  
    [https://cricsheet.org/downloads/#experimental](https://cricsheet.org/downloads/#experimental)  
  - The ZIP contains thousands of match files that must be merged into a single file.  
  - Use Python/JavaScript or visit **rex.tigzig.com** -> **Automation for AI Apps** -> **Cricsheet.org CSV-ZIP File Processor**.  
  - Upload the ZIP to get a ready-to-upload single text file.  
  - Here is the repo for the Cricsheet.org CSV-ZIP File Processor if you would like to customize it:  
  [https://github.com/amararun/shared-cricket-data-flask](https://github.com/amararun/shared-cricket-data-flask)  

---

### Step 7: 🖥️ FastAPI Backend Setup

- The FastAPI server repo is here:  
  [https://github.com/amararun/shared-rexc-cricket-fastapi](https://github.com/amararun/shared-rexc-cricket-fastapi)  
- Deploy the server on **Render**, **Railway**, or **AWS Lambda**.  
- Follow the deployment instructions in the repo.  

---


### Step 8: 🎙️ ElevenLabs Voice Widget Setup

Check out Leon's video for ElevenLabs voice widget setup.Superbly explained.
[https://www.youtube.com/watch?v=iL0zMDUKt6w](https://www.youtube.com/watch?v=iL0zMDUKt6w)

1. **Login** at [https://elevenlabs.io](https://elevenlabs.io).
2. Navigate to **Apps > Agents > Create An AI Agent**.
3. Configure the following:

   - **First Message**:  
     ```
     Hello, How are you doing this wonderful day? This is Rexie, your ODI cricket data assistant designed by Amar Harolikar. How can I help you?
     ```

  ### 📝 System Prompt

-----*** **system prompt starts here** ***-----

You are **Rexie**, a virtual assistant designed by Amar Harolikar to answer questions exclusively based on a PostgreSQL database containing **One Day International (ODI) cricket data**. Your primary task is to interpret user queries and generate PostgreSQL-compliant SQL queries to fetch the required data from the database using the **cricket_database_query_tool**If the user requests for query results or data to be pushed into their docs, use the `document_update_tool` for the same.

#### Database Context
- The database contains **ODI cricket data** stored in a virtual **Postgres warehouse**.
- The data resides in the `public` schema under a single table with the structure illustrated below. The table contains **one row per ball bowled** in ODIs.
- **Table name**: `odi`  
- **Schema.Table**: `public.odi`

#### Example Rows:
| match_id | season  | start_date | venue             | innings | ball | batting_team  | bowling_team  | striker     | non_striker  | bowler     | runs_off_bat | extras | wides | noballs | byes | legbyes | penalty | wicket_type | player_dismissed | other_wicket_type | other_player_dismissed |
|----------|---------|------------|-------------------|---------|------|---------------|---------------|-------------|--------------|------------|--------------|--------|-------|---------|------|---------|---------|-------------|-----------------|------------------|-----------------------|
| 366711   | 2008/09 | 2009-01-07 | Westpac Stadium   | 1       | 0.1  | West Indies   | New Zealand   | CH Gayle    | XM Marshall  | KD Mills   | 1            | 0      | 0     | 0       | 0    | 0       | 0       |             |                 |                  |                       |
| 366711   | 2008/09 | 2009-01-07 | Westpac Stadium   | 1       | 0.2  | West Indies   | New Zealand   | XM Marshall | CH Gayle     | KD Mills   | 0            | 0      | 0     | 0       | 0    | 0       | 0       |             |                 |                  |                       |
| 366711   | 2008/09 | 2009-01-07 | Westpac Stadium   | 1       | 0.4  | West Indies   | New Zealand   | XM Marshall | CH Gayle     | KD Mills   | 0            | 0      | 0     | 0       | 0    | 0       | 0       | caught      | XM Marshall      |                  |                       |

#### Critical Details:

1. **Focus**:
   - Answer **only** questions related to ODI cricket data from this database.
   - **Do not make up data** or use external sources like web search.

2. **Ball Counting**:
   - The `ball` field (e.g., `0.1`, `7.5`) is an identifier for the **over and ball number**, not a count of total balls.
   - Use a `COUNT(*)` query to calculate the number of balls bowled.

3. **Run Calculation**:
   - If the user specifies "runs" or "runs off bat," prioritize the `runs_off_bat` field.
   - Otherwise, interpret the query context and use appropriate fields like `extras` or **total runs** as required.

4. **Judgment**:
   - Users may not explicitly specify the **schema, table name, or field names**.
   - Use the sample rows to infer the structure and intelligently map user queries to database fields.

5. **Context**:
   - The table includes critical fields such as:
     - **Match details**: `match_id`, `season`, `start_date`, `venue`.
     - **Inning and ball information**: `innings`, `ball`.
     - **Teams and players**: `batting_team`, `bowling_team`, `striker`, `non_striker`, `bowler`.
     - **Outcome**: `runs_off_bat`, `extras`, `wicket_type`, `player_dismissed`.

6. **Player Name Queries**:
   - If a query is made regarding a player's name and the agent knows the name from previous messages, **use that exact name string** in the query.
   - If the agent does not know the name and needs to find out about a player, use **only the surname**. Wrap the surname in `%` wildcard characters (e.g., `%surname%`) to account for variations in case and ensure it can match anywhere in the relevant fields.

#### Your Responsibilities:
- Respond **concisely** to user questions with **factual answers** derived exclusively from the database.
- Convert user questions into **PostgreSQL queries** while ensuring they comply with the database schema.
- Avoid **speculating**, making up data, or performing tasks outside your scope.

-----*** **system prompt starts here** ***-----

### Setup Tools for the Agent:

#### 🛠️ **1. cricket_database_query_tool**
**Description**: Executes PostgreSQL-compliant SQL queries on a cloud database (Aiven).  
- **Method**: `GET`  
- **URL**: `https://cricket-fastapi.hosting.tigzig.com/sqlquery/`  
   *(Replace with your own FastAPI URL)*  

**Query Parameters**:
- `String | sqlquery`  
   - **Required**  
   - The PostgreSQL-compliant SQL query string generated from the user's input. Ensure proper URI encoding for special characters.  
- `String | cloud`  
   - **Required**  
   - The cloud database provider. Always set to `'aiven'`.  
   *(Replace with your own cloud database identifier if different)*  


#### 📤 **2. document_update_tool**
Pushes text or table data requested by the user to their Google Docs backend.  
- **Method**: `POST`  
- **URL**: `https://hook.us1.make.com/tteu9366w8j76cg987b9nzbcqjkhfswl4nuw`  
   *(Replace with your Make.com, n8n, Flowise, or any other document update endpoint if applicable)*  

**Query Parameters**:
- `String | data`  
   - The text data that the user has requested to be pushed to their docs.

***  

### Step 9: 🖋️ Modify the `index.html` File

### 1. 🔄 Update ElevenLabs Widget embed code

Replace the ElevenLabs widget code with your own. Locate this section in index.html:

```html
<elevenlabs-convai
agent-id="OHD9JQ3OoinJByncSRkS"
style="all: unset; width: auto; height: 100%;"
></elevenlabs-convai>
```
Replace with your own widget code from ElevenLabs.

### 2. 🤖 AI Chat Backend
The app currently uses a Flowise AI agent. Locate and modify this configuration in index.html:
```javascript
const chatflowId = '5e61fc5e-a2d9-410d-b1a4-1519fa0c3b4d';
const baseUrl = 'https://flowise-coolify.hosting.tigzig.com';
// Replace with your own Flowise chatflowId and baseUrl or alternative AI backend
```

### 3. 📄 Document Links

The document viewer section currently points to specific document URLs. Locate and modify this configuration in index.html:

```javascript
const DOCUMENT_URLS = {
    excel: {
        view: 'https://harolikar-my.sharepoint.com/personal/amar_harolikar_com/_layouts/15/Doc.aspx?sourcedoc={371a2aba-3da4-4966-8d5a-e02eb2038845}&action=embedview&wdAllowInteractivity=False&wdHideGridlines=True&wdHideHeaders=True&wdDownloadButton=True&wdInConfigurator=True&wdInConfigurator=True',
        edit: 'https://harolikar-my.sharepoint.com/personal/amar_harolikar_com/_layouts/15/Doc.aspx?sourcedoc={371a2aba-3da4-4966-8d5a-e02eb2038845}&action=edit'
    },
    google: {
        view: 'https://docs.google.com/spreadsheets/d/e/2PACX-1vT-ASVIfFJ4HdqIjq-2fSar4taGxlUutrZCeH1dFgfT6o-baBFQHLtJcGwgretrT2NmqtbQe7FbmxiS/pubhtml?widget=true&headers=false',
        edit: 'https://docs.google.com/spreadsheets/d/e/2PACX-1vT-ASVIfFJ4HdqIjq-2fSar4taGxlUutrZCeH1dFgfT6o-baBFQHLtJcGwgretrT2NmqtbQe7FbmxiS/pubhtml?widget=true&headers=false'
    },
    docs: {
        view: 'https://docs.google.com/document/d/e/2PACX-1vQ2z_n6-egJOrvFLMXsIBWvhxoPg01fS2XMchIJ-993uqD9YbaNbw9H1ZTD09CzeZ-VetsRNML2p3qF/pub?embedded=true',
        edit: 'https://docs.google.com/document/d/1v8BQURR8F6yoVlxGMmjPE9hEJAsLyx7cjtjiNLiXkhk/edit?usp=sharing'
    }
};
```

Replace these URLs with links to your own documents. You can use:
- SharePoint links for Excel files
- Google Sheets/Docs public sharing links
- Any other document service that provides embed URLs

### 4. 🖼️ Image URLs

The chart images are served from the Flowise backend. The image URLs are constructed using this pattern in index.html:

```javascript
const imageUrl = `${baseUrl}/api/v1/get-upload-file?chatflowId=${chatflowId}&chatId=${data.chatId}&fileName=${fileName}`;
```

When setting up your own instance:
- Replace `baseUrl` with your Flowise server URL
- Use your own `chatflowId`
- The `chatId` and `fileName` are dynamically generated by Flowise

Example URL structure:
```
https://your-flowise-server.com/api/v1/get-upload-file?chatflowId=your-chatflow-id&chatId=generated-chat-id&fileName=chart.png
```

Note: The image URLs are generated automatically when Flowise creates charts. 

### Step 9: 🎙️ Security  

Adding security to your app is **critical**, especially for API endpoints. Here are a few approaches:  
- **API Keys**  
- **IP Whitelisting**  
- **Authentication**  
- **Backend-Frontend Segregation** (requires a separate build).  

For this app, I implemented **IP-Domain Whitelisting** for my domain `tigzig.com`:  

#### Implementations:
- **Flowise Agent**:  
  `Configuration -> Allowed Domain -> Add your domain.`  

- **ElevenLabs**:  
  `Security -> Allowed List -> Add your domain.`  
  *(Removed this as it wasn’t working reliably)*  

- **FastAPI Server**:  
  Added the domain to the **CORS middleware configuration**.  
  *(Details available in the repo)*  

⚡ **Tip**: Do this **last**, once everything else is up and running. Debugging becomes easier.  

***  

## 📝Important Notes
- All styling is contained within the HTML file for easy modification
- The application uses DOMPurify for sanitizing markdown content
- Mobile view includes a tab-based interface for better user experience

***

## 🎉 That's it!

***  

## 📜 License

MIT License - Feel free to use and modify as needed.

## Author

Built by [Amar Harolikar](https://www.linkedin.com/in/amarharolikar/)

Explore 30+ open source AI tools for analytics, databases & automation at [tigzig.com](https://tigzig.com)
