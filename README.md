## 🧠 Grok API

This lightweight Node.js API serves as a proxy to the [`flex-chat-api`](https://flex-chat-api.vercel.app/) for accessing Grok AI completions. It provides a simple `q`-based GET endpoint that returns AI-generated responses.

## 🚀 Features

- ⚡ Fast and minimal Express server.
- 🔁 Proxies requests to `https://flex-chat-api.vercel.app/grok`.
- ✅ Simple query interface via `q` parameter.
- 🧩 Easily integrable into web apps or bots.

## 📦 Requirements

- Node.js 14+
- npm package: `axios`

## 📡 Usage

**1. Endpoint**  
Send a GET request to the deployed or local endpoint:  
`GET /?q=your+question+here`

**2. Query Parameters**

| Parameter | Required | Description                       |
|-----------|----------|-----------------------------------|
| `q`       | ✅        | The prompt to be sent to Grok AI. |

**✅ Example Request**
```bash
curl "http://localhost:3000/?q=Who+is+Elon+Musk"
```

**✅ Example Response**
```json
{
  "response": "Elon Musk is a technology entrepreneur..."
}
```

**❌ Error Response**
```json
{
  "error": "Missing q parameter"
}
```

## 🔍 Code Explanation

- `GET /`: Accepts a `q` query parameter.
- Sends request to:  
  `https://flex-chat-api.vercel.app/grok?q=YOUR_QUERY`
- Returns the external API's response.

## ⚠️ Error Handling

- 🛑 `400 Bad Request`: Returned when `q` is missing.
- 💥 `500 Internal Server Error`: Triggered if proxy request fails.

## 🛠️ Setup & Run

```bash
git clone https://github.com/your-username/grok-proxy-api.git
cd grok-proxy-api
npm install
node index.js
```

> The app will run at `http://localhost:3000/` by default.

## 🧪 Test It Online

You can deploy this project using **Render**, **Vercel**, **Glitch**, or **Replit** for free hosting.

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](https://github.com/NotFlexCoder/NotFlexCoder/blob/main/LICENSE) for details.
