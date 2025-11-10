# Week 3 — Dashboard Data Flow Notes

```
┌─────────────────────────────────────────────┐
│ AppShell                                    │
│ ├── TopNav                                  │
│ ├── Sidebar                                 │
│ └── <Outlet /> (React Router)               │
└─────────────────────────────────────────────┘
        │
        ▼
┌───────────────┐       ┌────────────────────┐
│ Global State  │◀────▶│ MealDB Service      │
│ (Context/Store)│     │ (fetch + cache)     │
└───────────────┘       └────────────────────┘
        │
        ├─────────────┐
        │             │
        ▼             ▼
┌──────────────┐  ┌──────────────┐
│ Tasks Module │  │ Menu Module  │
│ useState +   │  │ uses MealDB  │
│ useEffect    │  │ results +    │
│ localStorage │  │ favorites    │
└──────────────┘  └──────────────┘
        │             │
        ▼             ▼
┌──────────────┐  ┌──────────────┐
│ Tasks Page   │  │ Menu Page    │
└──────────────┘  └──────────────┘
        │             │
        └─────────┬───┘
                  ▼
           Home Dashboard
           (highlights tasks,
            favorites, alerts)
```

### Key Decisions
- **Caching:** Store the latest MealDB responses in context to avoid duplicate fetches across routes.
- **Error Recovery:** Surface toast notifications when API calls fail and fall back to cached data.
- **Persistence:** Tasks write to `localStorage` or your mock API; favorites can share the same persistence layer.
- **Routing Map:** `"/"` → Home, `"/tasks"` → Tasks Module, `"/menu"` → Menu Module, optional `"/settings"` for environment details.

---

**Related Task:** [Week 3 Task Brief — Sail to the Surface](../../materials/week3-tasks.md)

