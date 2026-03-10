# PyIRC 💬

A minimal IRC client written in Python that connects to IRC servers, joins channels, and lets you chat in real time — all from your terminal.

---

## 📁 Project Structure

```
├── IRC_Client.py    # Main client — connection, input handling, message parsing
└── README.md        # Project documentation
```

---

## ⚙️ Requirements

- Python 3.8+
- No external libraries — uses only the Python standard library (`socket`, `threading`)

---

## 🛠️ Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd <project-folder>
   ```

2. **Configure your nickname and server** (in `IRC_Client.py`)
   ```python
   SERVER = "irc.libera.chat"   # IRC server to connect to
   PORT   = 6667                 # Default IRC port
   NICK   = "Patro"              # Your nickname
   ```

---

## ▶️ Running the Client

```bash
python IRC_Client.py
```

Once running, you'll be connected to the server and can use the commands below.

---

## 💬 Commands

| Command              | Description                                        |
|----------------------|----------------------------------------------------|
| `/join <channel>`    | Join an IRC channel (e.g. `/join #python`)         |
| `/quit`              | Disconnect from the server and exit                |
| *(any other text)*   | Send a message to your current channel             |

---

## ✨ Features

- Connects to any IRC server over TCP
- Registers with a nickname and user info automatically
- Handles `PING`/`PONG` keepalives to stay connected
- Parses and displays incoming `PRIVMSG` messages cleanly (`<sender> message`)
- Threaded input so you can send and receive messages simultaneously
- Graceful disconnect on `/quit`

---

## 📌 Notes

- You must `/join` a channel before sending messages
- The client defaults to `irc.libera.chat` on port `6667` (unencrypted). For SSL, port `6697` would require additional setup
- This is a personal/learning project — a fun way to explore sockets and threading in Python!

---

## 📄 License

[MIT](https://choosealicense.com/licenses/mit/)
