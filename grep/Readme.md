## Grep comands 
Here are some common daily use cases of the `grep` command in Linux with useful options:

### 1\. **Basic Search in a File**

Search for a pattern in a file:

```bash
bashgrep "pattern" filename
```

### 2\. **Search Recursively in Directories**

Search through all files in a directory:

```bash
bashgrep -r "pattern" /path/to/directory
```

### 3\. **Search with Case Insensitivity**

Ignore case while searching:

```bash
bashgrep -i "pattern" filename
```

### 4\. **Display Line Numbers**

Show the line number of matching patterns:

```bash
bashgrep -n "pattern" filename
```

### 5\. **Search for Exact Word**

Search for the exact word match (not part of other words):

```bash
bashgrep -w "word" filename
```

### 6\. **Display Only Matching Part**

Show only the part of the line that matches the pattern:

```bash
bashgrep -o "pattern" filename
```

### 7\. **Search for Multiple Patterns**

Use the `-e` option to search for multiple patterns:

```bash
bashgrep -e "pattern1" -e "pattern2" filename
```

### 8\. **Count Occurrences**

Count the number of lines that match the pattern:

```bash
bashgrep -c "pattern" filename
```

### 9\. **Invert Match**

Show lines that do not match the pattern:

```bash
bashgrep -v "pattern" filename
```

### 10\. **Show Context Lines**

Show lines before and after the matching pattern:

```bash
bashgrep -A 3 -B 2 "pattern" filename   # 3 lines after, 2 lines before
```

### 11\. **Show Only File Names**

List only the names of files that contain the match:

```bash
bashgrep -l "pattern" /path/to/directory/*
```

### 12\. **Using with Pipelines**

Grep can be used with other commands to filter outputs:

```bash
bashls -l | grep "pattern"
```

### 13\. **Exclude Certain Files**

Exclude specific files when searching:

```bash
bashgrep --exclude="*.log" -r "pattern" /path/to/directory
```

### 14\. **Using Regular Expressions**

You can use extended regex with `-E`:

```bash
bashgrep -E "pattern1|pattern2" filename
```

These options and use cases will help you handle most of your daily tasks efficiently with `grep`.

