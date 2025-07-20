# Employee-Salary-Prediction
# Employee Salary Prediction Application
  education: "Bachelor's Degree",
  location: "San Francisco",
  department: "Engineering",
  skills: ["JavaScript", "React", "Node.js", "AWS"]
};
```

**Prediction Output:**
```typescript
{
  predictedSalary: 142750,
  confidenceLevel: 93,
  salaryRange: {
    min: 121338,
    max: 164163
  },
  factors: {
    experience: 9,
    education: 16,
    location: 31,
    department: 21,
    skills: 13
  }
}
```

## 🎯 Prediction Factors

### Base Salary Configuration

```typescript
const BASE_SALARY = 45000;

// Experience bonus: $2,500 per year (capped at 10 years)
const experienceBonus = Math.min(experience * 2500, 25000);
```

### Education Multipliers

```typescript
const EDUCATION_MULTIPLIERS = {
  'High School': 1.0,        // No change
  'Associate Degree': 1.15,  // +15%
  'Bachelor\'s Degree': 1.35, // +35%
  'Master\'s Degree': 1.65,  // +65%
  'PhD': 1.9,               // +90%
};
```

### Location Multipliers

```typescript
const LOCATION_MULTIPLIERS = {
  'San Francisco': 1.45,     // +45% (highest)
  'New York': 1.4,          // +40%
  'Seattle': 1.35,          // +35%
  'Boston': 1.3,            // +30%
  'Los Angeles': 1.35,      // +35%
  'Austin': 1.25,           // +25%
  'Chicago': 1.2,           // +20%
  'Denver': 1.15,           // +15%
  'Atlanta': 1.1,           // +10%
  'Remote': 1.05,           // +5%
  'Other': 1.0,             // No change
};
```

### Department Multipliers

```typescript
const DEPARTMENT_MULTIPLIERS = {
  'Data Science': 1.35,      // +35% (highest)
  'Engineering': 1.3,        // +30%
  'Product Management': 1.25, // +25%
  'Finance': 1.2,            // +20%
  'Design': 1.15,            // +15%
  'Sales': 1.15,             // +15%
  'Marketing': 1.1,          // +10%
  'Operations': 1.08,        // +8%
  'Human Resources': 1.05,   // +5%
  'Customer Support': 0.95,  // -5%
};
```

### Skills & Technology Bonuses

```typescript
const SKILL_BONUSES = {
  'Machine Learning': 8000,  // Highest bonus
  'AWS': 7000,
  'Python': 6000,
dist/asse
