# 🔒 File Integrity Monitoring System

A Python-based **File Integrity Monitoring (FIM)** tool that uses **SHA-256 hashing** to detect unauthorized changes to files. The program creates a baseline of file hashes and continuously monitors a target directory to identify newly created, modified, or deleted files.

## ✨ Features

* Generate SHA-256 hashes for files
* Create a baseline of file hashes
* Detect file modifications
* Detect newly created files
* Detect deleted files
* Continuous real-time monitoring
* Store baseline hashes in a JSON file

## 🛠️ Technologies Used

* Python 3
* `os`
* `hashlib`
* `json`
* `time`

## 📁 Project Structure

```
.
├── project.py          # Main monitoring script
├── hashfile.json       # Stores baseline file hashes
└── README.md
```

## ⚙️ How It Works

1. Scans the target directory recursively.
2. Calculates the SHA-256 hash of every file.
3. Stores the hashes in `hashfile.json`.
4. Continuously rescans the directory every 5 seconds.
5. Compares the current hashes with the baseline.
6. Reports:

   * ✅ New files
   * ✏️ Modified files
   * ❌ Deleted files

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/your-username/file-integrity-monitor.git
```

Move into the project directory:

```bash
cd file-integrity-monitor
```

## ▶️ Usage

Update the target directory in `project.py`:

```python
os.walk("/path/to/your/directory")
```

Run the program:

```bash
python project.py
```

The program will create a baseline hash database and begin monitoring the directory for changes.

## 📌 Example Output

```
new file created : /home/user/Documents/test.txt

file modified : /home/user/Documents/report.pdf

file deleted : /home/user/Documents/notes.txt
```

## 🎯 Learning Objectives

This project demonstrates:

* File Integrity Monitoring (FIM)
* SHA-256 hashing
* File system traversal
* JSON data storage
* Continuous directory monitoring
* Basic Host-Based Intrusion Detection concepts

## 🔮 Future Improvements

* Monitor multiple directories
* Ignore specific files or folders
* Email or desktop notifications
* Logging to a file
* Command-line arguments
* Configuration file support
* GUI dashboard
* Multi-threaded scanning

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repository, create a feature branch, and submit a pull request.

## 📄 License

This project is licensed under the MIT License.

