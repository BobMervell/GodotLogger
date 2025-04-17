# 📘 Godot Logger

Godot Logger is a lightweight, customizable logging plugin for Godot 4.4 (should work but untested for Godot 4.x)  that brings structured, formatted, and configurable log output to your development workflow. 

With support for multiple log levels (Info, Debug, Warning, Error, Fatal), rich text output, it helps developers keep track of what really matters — from debugging to critical failures.

---

## ✨ Features

✔️ **Configurable Log Levels** – Toggle each log type (`info`, `debug`, `warn`, `error`, `fatal`) in the bottom panel.  
✔️ **Rich Console Output** – Uses color-coded and formatted logs directly in the Godot console.  
✔️ **Structured Logging** – Attach optional dictionaries to enrich logs with contextual data.  
✔️ **Built-in Formatting** – Logs are serialized as JSON strings for easier parsing and readability.  
✔️ **Errors and Warnings push** – Push errors and warnings to the editor for warn, error and fatal logs.  
✔️ **No Setup Required** – Just drop the plugin and start logging.

---

## 🔧 Installation

1. **Clone or Download** this repository.
2. Place the `Godot_logger` folder in your `res://addons/` directory.
  
---

## 🛠️ Usage Guide

### 🧩 Enabling the Plugin

This plugin is autoloaded through GDScript.

You can call the following functions from your script after enabling the plugin:

```gdscript
LoggerAutoload.log_info("Something happened!", {"context": "player_spawn"})
LoggerAutoload.log_debug("Debugging this weird behavior", {"velocity": Vector2(10, 5)})
LoggerAutoload.log_warn("Something might go wrong", {"area": "UI"})
LoggerAutoload.log_error("Something went wrong!", {"code": 403})
LoggerAutoload.log_fatal("Critical crash", {"scene": "BattleArena"})
```

All log functions accept:
- A required message `String`
- An optional `Dictionary` for additional structured data

### 🧠 Log Output Example

```gdscript
LoggerAutoload.log_info("Player connected", {"player_id": 42})
```

Output in console:
```
INFO: {
..."Message": "Player connected",
..."Timestamp": 1527,
..."Details": {
......"player_id": 42
...}
}

```

Color-coded and bolded depending on the log level.

| Method         | Description                            |
|----------------|----------------------------------------|
| `log_info()`   | Standard information logs              |
| `log_debug()`  | Dev-level debugging information        |
| `log_warn()`   | Warning messages `push_warning()`      |
| `log_error()`  | Error messages with `push_error()`     |
| `log_fatal()`  | Fatal errors with `push_error()`       |


## 📝 License

This project is released under **MIT License** — feel free to use and modify it.  

---

## 💬 Support

If you encounter issues, feel free to open a GitHub issue or ping me directly. I'm happy to help!
