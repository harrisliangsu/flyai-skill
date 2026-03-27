# FlyAI Skill - Travel Assistant

[![Version](https://img.shields.io/badge/version-1.1.0-blue.svg)](https://github.com/alibaba-flyai/flyai-skill)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

> 🌍 Travel assistant skill based on Fliggy MCP, providing one-stop travel services including hotel booking, flight search, attraction recommendations and more.

**[🇨🇳 中文版本](README.zh-CN.md)**

## ✨ Core Features

- **🏨 Hotel Search**: Multi-dimensional filtering by destination, star rating, price, bed type and more
- **✈️ Flight Query**: Real-time flight search with support for round-trip, cabin class selection, time slot filtering
- **🎯 Attraction Recommendations**: Coverage of attractions in major cities nationwide, with filtering by level and type
- **🔍 Smart Search**: Natural language queries to get comprehensive results for hotels, flights, and attractions in one click
- **📅 Time-Aware**: Supports check-in/check-out dates, departure/return dates and other time parameters
- **💰 Price Comparison**: Price range filtering and sorting to help you find the best deals

## 🚀 Quick Start

### Option 1: Install via ClawHub

```bash
clawhub install flyai
```

### Option 2: Install via NPX

```bash
npx skills add alibaba-flyai/flyai-skill
```

### Verify Installation

```bash
flyai --help
```

## 📖 Usage Examples

### 1. Natural Language Search (Recommended)

```bash
# Search for hotels in Sanya
flyai fliggy-fast-search --query "Sanya Yalong Bay 5-star hotel"

# Query flights from Beijing to Shanghai
flyai fliggy-fast-search --query "Tomorrow's flights from Beijing to Shanghai"

# Find attractions near West Lake in Hangzhou
flyai fliggy-fast-search --query "What's fun around Hangzhou West Lake"

# Search for Japan visa services
flyai fliggy-fast-search --query "Japan individual tourist visa"
```

### 2. Structured Hotel Search

```bash
# Basic search
flyai search-hotels --dest-name "Hangzhou"

# Search with date and attraction filtering
flyai search-hotels --dest-name "Hangzhou" --poi-name "West Lake" \
  --check-in-date YYYY-MM-DD --check-out-date YYYY-MM-DD

# Luxury hotel filtering
flyai search-hotels --dest-name "Sanya" --hotel-stars "4,5" \
  --sort rate_desc --max-price 1000
```

### 3. Flight Query

```bash
# One-way flight
flyai search-flight --origin "Beijing" --destination "Shanghai" \
  --dep-date YYYY-MM-DD

# Round-trip flight
flyai search-flight --origin "Shanghai" --destination "Tokyo" \
  --dep-date YYYY-MM-DD --back-date YYYY-MM-DD

# Sort by lowest price
flyai search-flight --origin "Beijing" --destination "Guangzhou" \
  --dep-date YYYY-MM-DD --sort-type 3
```

### 4. Attraction Search

```bash
# Search attractions in a specific city
flyai search-poi --city-name "Xi'an" --category "Historical Sites"

# Search attractions by level
flyai search-poi --city-name "Beijing" --poi-level 5

# Keyword search
flyai search-poi --city-name "Hangzhou" --keyword "West Lake" \
  --category "Mountain & Lake Gardens"
```

## 🛠️ Configuration

The tool can be used without any API key. For enhanced result quality, you can configure optional APIs:

```bash
flyai config set FLYAI_API_KEY "your-api-key"
```

## 📚 Detailed Documentation

| Command | Description | Documentation |
|---------|-------------|---------------|
| `fliggy-fast-search` | Natural language quick search | [View Docs](skills/flyai/references/fliggy-fast-search.md) |
| `search-hotels` | Structured hotel search | [View Docs](skills/flyai/references/search-hotels.md) |
| `search-flight` | Flight query | [View Docs](skills/flyai/references/search-flight.md) |
| `search-poi` | Attraction search | [View Docs](skills/flyai/references/search-poi.md) |

## 📋 Output Format

All commands output **single-line JSON** to `stdout`, with errors and hints going to `stderr` for easy integration with tools like `jq` or Python.

### Friendly Display Requirements

- ✅ **Image Display**: Use `![]({imageUrl})` format on a separate line
- ✅ **Booking Link**: Use `[Click to book]({url})` format on a separate line
- ✅ **Hierarchy**: Use Markdown headings (#, ##, ###) and lists
- ✅ **Table Comparison**: Use Markdown tables for multi-option comparisons
- ✅ **Chronological Order**: Arrange itinerary items in time sequence
- ✅ **Key Emphasis**: Bold critical information such as dates, locations, prices, and constraints

## 🤝 Contributing

Issues and Pull Requests are welcome!

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Related Links

- [FlyAI Open Platform](https://open.fly.ai/)
- [Fliggy Travel](https://www.fliggy.com/)
- [ClawHub Skill Market](https://github.com/claw-lang/clawhub)

---

<div align="center">
  <sub>Built with ❤️ by Alibaba Fliggy Team</sub>
</div>
