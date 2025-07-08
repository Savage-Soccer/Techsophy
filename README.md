# Mental Health Mood Tracker with Insights

An intelligent Python system that analyzes daily mood patterns and provides actionable mental health insights with professional care recommendations.

## Problem Statement

Create a system that analyzes daily mood entries and identifies patterns or concerning trends.

## Skills Demonstrated

**AI/ML**: Time series analysis, pattern recognition, anomaly detection for mood patterns

**Critical Thinking**: Understanding mental health indicators, recognizing when to suggest professional help

**Problem Solving**: Handling subjective data, missing entries, seasonal patterns, privacy concerns

**Modular Structure**: Separate data collection, trend analysis, pattern detection, and recommendation modules

**Clear Architecture**: Pipeline from mood entries → trend analysis → pattern recognition → actionable insights

## System Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Data Layer    │    │  Analysis Core  │    │ Insights Engine │
├─────────────────┤    ├─────────────────┤    ├─────────────────┤
│ • CSV Import    │───▶│ • Time Series   │───▶│ • Pattern Detect│
│ • Live Input    │    │ • Anomaly Detect│    │ • Risk Assessment│
│ • Data Cleaning │    │ • Statistical   │    │ • Recommendations│
│ • Validation    │    │   Processing    │    │ • Care Guidance │
└─────────────────┘    └─────────────────┘    └─────────────────┘
                                 │
                                 ▼
                    ┌─────────────────┐
                    │ Visualization   │
                    │ Dashboard       │
                    ├─────────────────┤
                    │ • Mood Timeline │
                    │ • Pattern Charts│
                    │ • Activity Plots│
                    │ • Anomaly Alerts│
                    └─────────────────┘
```

## Key Features

### Advanced Analytics
- **Time Series Analysis**: 7-day and 30-day rolling averages with trend detection
- **Anomaly Detection**: Statistical outlier identification using Z-scores
- **Pattern Recognition**: Weekly/monthly patterns, seasonal variations
- **Activity Correlation**: Mood-activity relationship analysis

### Mental Health Intelligence
- **Risk Assessment**: Automated detection of concerning patterns
- **Professional Care Triggers**: Smart alerts for when to suggest professional help
- **Personalized Recommendations**: Activity-based mood improvement strategies
- **Crisis Pattern Detection**: Consecutive low mood days, significant drops

### Interactive System
- **Live Mood Entry**: Real-time mood tracking with activity logging
- **Comprehensive Dashboard**: Multi-panel visualization system
- **Data Export**: Updated CSV export functionality
- **Weekly Analysis**: Recent pattern focused insights

## Technical Implementation

### Core Classes
```python
MoodTracker()           # Main analysis engine
LiveMoodTracker()       # Real-time data collection
MentalHealthAnalyzer()  # Risk assessment & recommendations
```

### Mental Health Indicators
- **Consecutive Low Mood**: 3+ days with mood ≤ 2/5
- **Significant Drops**: >1 point average decrease
- **Sustained Low Periods**: Average <2.5/5 over 2 weeks
- **High Variability**: Standard deviation >1.5 (instability)

### Automated Care Recommendations
- Professional help suggestions based on pattern severity
- Activity-based mood improvement strategies
- Lifestyle and wellness recommendations
- Crisis resource guidance when appropriate

## Quick Start

```python
# Initialize and analyze existing data
import pandas as pd
from mood_tracker import MoodTracker, LiveMoodTracker, MentalHealthAnalyzer

# Load Daylio CSV export
daylio = pd.read_csv("Daylio_Export.csv")

# Generate comprehensive analysis
tracker = MoodTracker(daylio)
report = tracker.generate_report()

# Add new mood entries
live_tracker = LiveMoodTracker(daylio)
updated_data = live_tracker.add_mood_entry()

# Mental health insights
analyzer = MentalHealthAnalyzer(updated_data)
concerns = analyzer.detect_concerning_patterns()
recommendations = analyzer.generate_recommendations()
```

## Visualizations

- **Mood Timeline**: Daily patterns with trend lines and anomaly markers
- **Pattern Analysis**: Weekly/monthly mood distributions
- **Activity Correlation**: Heatmaps showing mood-activity relationships
- **Risk Dashboard**: Visual alerts for concerning patterns

## Privacy & Ethics

- **Local Processing**: All data stays on your machine
- **No External Transmission**: Complete privacy protection
- **Professional Guidance**: Clear recommendations for seeking help
- **Ethical AI**: Responsible mental health pattern recognition

## Installation

```bash
pip install pandas numpy matplotlib scipy seaborn
python mood_tracker.py
```

## Deliverable

A complete system that demonstrates AI/ML implementation, critical thinking about mental health indicators, and modular problem-solving architecture - delivering actionable insights with appropriate professional care recommendations.

---

*This project showcases advanced data science skills applied to mental health awareness, combining technical expertise with ethical responsibility in AI-driven healthcare applications.*
