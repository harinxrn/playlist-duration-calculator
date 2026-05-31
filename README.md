[README.md](https://github.com/user-attachments/files/28433522/README.md)
# 🎵 Playlist Duration Calculator

A Python CLI tool that analyzes music playlists — calculating total duration, average song length, and identifying the longest and shortest tracks from MM:SS formatted input.

---

## 📋 Features

- Parses song durations in `MM:SS` format
- Calculates total playlist duration in `HH:MM:SS`
- Computes average song length (truncated to whole seconds)
- Identifies the longest and shortest tracks
- Handles ties by picking the first occurrence
- Clean error handling for invalid input

---

## 🚀 Usage

```bash
python script.py < input.txt
```

Or pipe input directly:

```bash
echo "4
Sunrise 03:45
Midnight 05:12
Echo 02:30
Dawn 04:18" | python script.py
```

---

## 📥 Input Format

```
N
song_name MM:SS
song_name MM:SS
...
```

- First line: integer `N` — number of songs
- Next `N` lines: `song_name` and `duration` separated by a space
- Song names are single word, alphanumeric
- Duration is in `MM:SS` format

---

## 📤 Output Format

```
PLAYLIST STATS
Total Songs: N
Total Duration: HH:MM:SS
Average Duration: MM:SS
Longest: song_name (MM:SS)
Shortest: song_name (MM:SS)
```

---

## 🧪 Example

**Input:**
```
4
Sunrise 03:45
Midnight 05:12
Echo 02:30
Dawn 04:18
```

**Output:**
```
PLAYLIST STATS
Total Songs: 4
Total Duration: 00:15:45
Average Duration: 03:56
Longest: Midnight (05:12)
Shortest: Echo (02:30)
```

---

## ⚙️ Constraints

| Parameter | Constraint              |
|-----------|-------------------------|
| N         | 1 ≤ N ≤ 500             |
| Duration  | 00:01 ≤ MM:SS ≤ 99:59  |
| Names     | Single word, alphanumeric |

---

## 🛠️ Requirements

- Python 3.10+
- No external libraries — standard library only

---

## 📁 Project Structure

```
playlist-duration-calculator/
│
├── script.py       # Main script
└── README.md       # Project documentation
```

---

## 📝 How It Works

1. Reads `N` songs from stdin
2. Converts each `MM:SS` duration to total seconds
3. Computes total, average, longest, and shortest
4. Formats and prints the stats in the required format

Average is **truncated** (not rounded) to whole seconds — e.g. `236.25s → 03:56`.

---

## 👤 Author

**Hari**  
[github.com/hari](https://github.com/hari)
