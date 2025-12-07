# Health Goals Tracker

> **Version:** 1.0.0 | **Last Updated:** December 2024

## Overview

The Health Goals Tracker helps you build healthy habits by tracking daily water intake, exercise minutes, and sleep hours. Set personalized goals, monitor your progress, build streaks, and get AI-powered health tips to stay motivated.

## Features

### Daily Tracking
- **Water Intake:** Track glasses of water consumed daily
- **Exercise:** Log minutes of physical activity
- **Sleep:** Record hours of sleep each night

### Progress Visualization
- Real-time progress bars for each goal
- Weekly progress charts
- Streak tracking with visual badges
- Completion rate statistics

### AI-Powered Tips
- Personalized health recommendations
- Context-aware suggestions based on your goals
- Multilingual support for tips

## How It Works

### Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Goal Cards    │ -> │   Backend API   │ -> │   In-Memory     │
│   (Frontend)    │    │   /api/health   │    │   Storage       │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                      │                      │
         v                      v                      v
    Track Progress        CRUD Operations        Goal & Entry
    Set Targets           Statistics             Data Models
```

## Getting Started

### Step 1: Access Health Goals
Click the target icon in the main application header to open the Health Goals Tracker.

### Step 2: Set Your Targets
Each goal type has a default target:
- **Water:** 8 glasses per day
- **Exercise:** 30 minutes per day
- **Sleep:** 8 hours per night

Click the settings icon on any goal card to customize your target.

### Step 3: Track Daily Progress
Use the + and - buttons to log your daily values:
- Increment when you drink a glass of water
- Add exercise minutes after workouts
- Log your sleep hours in the morning

### Step 4: View Statistics
Each goal card shows:
- Current day streak
- Weekly average
- Completion percentage
- Best day performance

## Goal Types

### Water Tracking

| Setting | Default | Unit |
|---------|---------|------|
| Daily Target | 8 | glasses |

**Benefits of proper hydration:**
- Improved energy levels
- Better cognitive function
- Enhanced physical performance
- Healthy skin

### Exercise Tracking

| Setting | Default | Unit |
|---------|---------|------|
| Daily Target | 30 | minutes |

**Exercise categories include:**
- Walking
- Running
- Gym workouts
- Sports activities
- Yoga/stretching

### Sleep Tracking

| Setting | Default | Unit |
|---------|---------|------|
| Daily Target | 8 | hours |

**Quality sleep supports:**
- Memory consolidation
- Physical recovery
- Immune function
- Emotional regulation

## Streaks & Achievements

### How Streaks Work
A streak represents consecutive days of meeting your goal:
- Meet or exceed your daily target to maintain your streak
- Missing a day resets the streak to zero
- Streaks are displayed with a flame icon badge

### Statistics Tracked
- **Weekly Average:** Average value over the past 7 days
- **Completion Rate:** Percentage of days you met your goal
- **Best Day:** Highest value recorded
- **Total Days Tracked:** Number of days with logged entries

## AI Health Tips

### Built-in Tips
Each goal type includes curated health tips:

**Water Tips:**
- Start your day with a glass of water
- Keep a water bottle at your desk
- Add natural flavors like lemon

**Exercise Tips:**
- Take the stairs instead of elevator
- A 10-minute walk after meals helps digestion
- Find activities you enjoy for consistency

**Sleep Tips:**
- Keep a consistent sleep schedule
- Avoid screens before bedtime
- Keep your bedroom cool and dark

### AI-Powered Recommendations
Click "Get AI Tip" to receive personalized recommendations based on:
- Your current goal type
- Progress statistics
- General health best practices

## API Reference

### Endpoints

#### Get All Goals
```
GET /api/health-goals
```

Returns all health goals with current settings.

#### Update Goal Target
```
PATCH /api/health-goals/:type
```

| Parameter | Type | Description |
|-----------|------|-------------|
| type | string | Goal type: water, exercise, or sleep |

**Request Body:**
```json
{
  "targetValue": 10,
  "unit": "glasses"
}
```

#### Get Entries for Goal
```
GET /api/health-goals/:type/entries
```

Returns logged entries for a specific goal type.

#### Log Entry
```
POST /api/health-goals/:type/entries
```

**Request Body:**
```json
{
  "date": "2024-12-07",
  "value": 8
}
```

#### Get Statistics
```
GET /api/health-goals/:type/stats
```

Returns statistics for a specific goal type.

#### Get AI Recommendation
```
POST /api/health-goals/:type/recommendation
```

Returns an AI-generated health tip.

## Data Model

### Health Goal
```typescript
{
  id: number;
  type: "water" | "exercise" | "sleep";
  targetValue: number;
  unit: string;
}
```

### Health Goal Entry
```typescript
{
  id: number;
  goalType: "water" | "exercise" | "sleep";
  date: string;  // YYYY-MM-DD format
  value: number;
}
```

### Goal Statistics
```typescript
{
  weeklyAverage: number;
  streak: number;
  completionRate: number;
  bestDay: number;
  totalDaysTracked: number;
}
```

## Multilingual Support

The Health Goals Tracker supports 11 languages:
- English
- Spanish (Espa\u00f1ol)
- French (Fran\u00e7ais)
- German (Deutsch)
- Chinese Simplified (\u7b80\u4f53\u4e2d\u6587)
- Japanese (\u65e5\u672c\u8a9e)
- Korean (\ud55c\uad6d\uc5b4)
- Russian (\u0420\u0443\u0441\u0441\u043a\u0438\u0439)
- Portuguese (Portugu\u00eas)
- Hindi (\u0939\u093f\u0902\u0926\u0940)
- Arabic (\u0627\u0644\u0639\u0631\u0628\u064a\u0629)

## Tips for Success

1. **Start small:** Begin with achievable targets and increase gradually
2. **Be consistent:** Log your progress at the same time each day
3. **Use reminders:** Set phone alarms for water breaks and exercise
4. **Celebrate streaks:** Take pride in maintaining healthy habits
5. **Don't give up:** Missing one day doesn't erase your progress

## Privacy

- All health data is stored locally in the application
- No personal health information is shared with third parties
- Data is not transmitted unless using AI recommendation features

## Troubleshooting

### Progress not saving
- Ensure you're connected to the internet
- Refresh the page and try again
- Check browser console for errors

### Streak reset unexpectedly
- Verify you met your target on the previous day
- Check that entries are logged with the correct date

### AI tips not loading
- Check internet connection
- Verify API credentials are configured
- Try again after a few moments

## Future Enhancements

- [ ] Custom goal types
- [ ] Goal reminders and notifications
- [ ] Social sharing and challenges
- [ ] Integration with fitness trackers
- [ ] Historical data export
- [ ] Progress graphs and trends

## Support

For issues or feedback regarding the Health Goals Tracker, please open an issue on GitHub or contact support.

---

*Build healthy habits one day at a time.*
