# Elevenlabs conversational voice agent

## Description

This is a frontend for a Elevenlabs conversational voice agent implemented in react +vite and deployed on vercel.

The agentId is specified as an environment variable VITE_ELEVENLABS_AGENT_ID in .env.

The current agent Miriam uses a n8n webhook tool to access the n8n-ai-notebook index of a Pinecone Vector Database 
in order to retrieve information about ai agent development, tools, techniques and frameworks.
The vector database will be loaded by n8n google drive trigger workflow listening for events on the folder n8n-ai-notebook on google drive.

Optionally the elevenlabs voice agent could access this workflow using mcp to have it also available for for example Claude Desktop.

If you would like to use another knowledge base be aware to
- check the system prompt of your elevenlabs agent
- the description of the elevenlabs agent tools or mcp interfaces
- check the instructions for the n8n knowledge base nodes

## Documentation

[https://elevenlabs.io/docs/conversational-ai/guides/quickstarts/java-script](https://elevenlabs.io/docs/conversational-ai/guides/quickstarts/java-script)

## Requirements

- node.js
- npm

## Implementation

Follow the documentation:
- Build the scaffold

```
mkdir elevenlabs-conversational-ai-vite
cd elevenlabs-conversational-ai-vite
npm init -y
npm install vite @elevenlabs/client

add this to package.json:
{
    "scripts": {
        ...
        "dev:frontend": "vite"
    }
}

create the following file structure:

elevenlabs-conversational-ai/
├── index.html
├── script.js
├── package-lock.json
├── package.json
└── node_modules

```
- edit index.html
- edit index.js
- create .env and .env.example and set VITE_ELEVENLABS_AGENT_ID
- edit index.js in order to set agentId using the environment variable

- add .gitignore for git and github
- create github repo
- activate git
```
git init
git remote add origin https://github.com/jk-github-dotcom/elevenlabs-conversational-agent-vite.git
git add .
git commit -m "Initial commit: react + vite frontend for an elevenlabs conversational agent"
git branch -M main
git push -u origin main
```

## start the frontend server locally

```
npm run dev:frontend
```

Open http://localhost:5371 with your browser.

