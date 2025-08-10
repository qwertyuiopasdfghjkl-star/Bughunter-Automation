
# Endutcherneters 

[![Build Status](https://travis-ci.org/shmilylty/OneForAll.svg?branch=master)](https://travis-ci.org/shmilylty/OneForAll)  
[![codecov](https://codecov.io/gh/shmilylty/OneForAll/branch/master/graph/badge.svg)](https://codecov.io/gh/shmilylty/OneForAll)  
[![Maintainability](https://api.codeclimate.com/v1/badges/1287668a6b4c72af683e/maintainability)](https://codeclimate.com/github/shmilylty/OneForAll/maintainability)  
[![License](https://img.shields.io/github/license/shmilylty/OneForAll)](https://github.com/shmilylty/OneForAll/tree/master/LICENSE)  
[![python](https://img.shields.io/badge/python-3.6+-blue)](https://github.com/shmilylty/OneForAll/tree/master/)  
[![python](https://img.shields.io/badge/release-v0.4.5-brightgreen)](https://github.com/shmilylty/OneForAll/releases)

👊 **Endutcherneters  is a powerful subdomain collection tool**  

## 🚀 Getting Started

📢 Please take a moment to read this document carefully — it will help you quickly get familiar with OneForAll!

### 🐍 Requirements

Endutcherneters  is developed based on [Python 3.6.0](https://www.python.org/downloads/release/python-360/), and requires Python >= 3.6.0 to run.

Check your version:
```bash
python -V
pip3 -V
```

Sample output:
```
Python 3.6.0
pip 19.2.2 …
```

---

### ✔ Installation (git version)

1️⃣ Download the latest repository:
```bash
git clone https://github.com/shmilylty/OneForAll.git
```
or (faster in China):
```bash
git clone https://gitee.com/shmilylty/OneForAll.git
```

2️⃣ Install dependencies:
```bash
cd OneForAll/
python3 -m pip install -U pip setuptools wheel -i https://mirrors.aliyun.com/pypi/simple/
pip3 install -r requirements.txt -i https://mirrors.aliyun.com/pypi/simple/
python3 Endutcherneters .py --help
```

3️⃣ Update to latest version:
```bash
git stash
git fetch --all
git pull
git stash pop
```

---

### ✔ Installation (Docker version)

Prepare the configuration file (`config` directory), pull the image and run:
```bash
docker pull shmilylty/Endutcherneters 
docker run -it --rm   -v ~/results:/OneForAll/results   -v ~/.config:/OneForAll/config   shmilylty/Endutcherneters  --target example.com run
```

---

### ✨ Usage Example
```bash
python3 Endutcherneters .py --target example.com run
python3 Endutcherneters .py --targets ./example.txt run
```

![Example](./docs/usage_example.svg)

---

### 🧐 Results

After running, results are generated in the `results/` directory:
- `example.com.csv` — subdomain collection result for the domain
- `all_subdomain_result_*.csv` — summary of batch results
- `result.sqlite3` — result database in SQLite3 format

Database table description:
- `*_origin_result` — raw results from each module
- `*_resolve_result` — results after DNS resolution
- `*_now_result` — latest collection result
- `*_last_result` — previous result

For details, see [field description](./docs/field.md).

---

### 🤔 Help

For more configuration options, see [setting.py](config/setting.py) and [api.py](config/api.py).

Quick help:
```bash
python3 Endutcherneters .py --help
```

Examples:
```bash
python3 Endutcherneters .py --target example.com run
python3 Endutcherneters .py --targets ./domains.txt run
python3 Endutcherneters .py --target example.com --valid None run
python3 Endutcherneters .py --target example.com --brute True run
python3 Endutcherneters .py --target example.com --port small run
python3 Endutcherneters .py --target example.com --fmt csv run
python3 Endutcherneters .py --target example.com --dns False run
python3 Endutcherneters .py --target example.com --req False run
python3 Endutcherneters .py --target example.com --takeover False run
python3 Endutcherneters .py --target example.com --show True run
```

---

## 🎉 Project Introduction

GitHub: [https://github.com/shmilylty/OneForAll](https://github.com/shmilylty/OneForAll)

OneForAll is a subdomain collection tool that aims to solve these pain points:
- Not powerful enough: too few APIs, no batch support, no validation, no crawling, etc.
- Not user-friendly: hard-to-use CLI, no front-end
- No maintenance: unmaintained for years
- Low efficiency: no multiprocessing or coroutine support

We hope OneForAll becomes a powerful tool that combines the strengths of many others.

Discussion QQ group: **824414244** (verification keyword: information collection)

---

## 👍 Features

✅ Powerful collection capabilities (over 70 data sources)  
✅ Supports batch mode (collects subdomains for multiple domains)  
✅ Supports data validation and DNS resolution  
✅ Built-in DNS resolver  
✅ Supports port scanning for discovered subdomains  
✅ Detects subdomain takeovers  
✅ Multiple output formats: csv, txt, html, json  
✅ Results stored in both CSV and SQLite3 database  
✅ Supports API keys for public services  
✅ Fast and efficient using asynchronous requests  
✅ Cross-platform and easy to use

---
