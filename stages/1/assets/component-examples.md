# React Component Examples for Stage 1

This guide provides examples of React components with TypeScript to help you build the "Interactive Welcome Board" project.

## Example 1: Simple Greeting Component

```tsx
// src/components/Greeting.tsx
interface GreetingProps {
  name: string;
  message?: string; // Optional prop
}

function Greeting({ name, message = "Welcome to Bikini Bottom!" }: GreetingProps) {
  return (
    <div>
      <h1>Hello, {name}!</h1>
      <p>{message}</p>
    </div>
  );
}

export default Greeting;
```

**Usage:**
```tsx
<Greeting name="SpongeBob" />
<Greeting name="Patrick" message="Hey, buddy!" />
```

## Example 2: Resident Card Component

```tsx
// src/components/types.ts
export interface Resident {
  id: string;
  name: string;
  role: string;
  description: string;
  imageUrl: string;
}

// src/components/ResidentCard.tsx
import { Resident } from './types';

interface ResidentCardProps {
  resident: Resident;
  onFavorite?: (id: string) => void;
  isFavorite?: boolean;
}

function ResidentCard({ 
  resident, 
  onFavorite, 
  isFavorite = false 
}: ResidentCardProps) {
  const handleClick = () => {
    if (onFavorite) {
      onFavorite(resident.id);
    }
  };

  return (
    <div className="resident-card">
      <img src={resident.imageUrl} alt={resident.name} />
      <h2>{resident.name}</h2>
      <p className="role">{resident.role}</p>
      <p>{resident.description}</p>
      {onFavorite && (
        <button onClick={handleClick}>
          {isFavorite ? '⭐ Favorite' : '☆ Add to Favorites'}
        </button>
      )}
    </div>
  );
}

export default ResidentCard;
```

## Example 3: Welcome Board (Container Component)

```tsx
// src/components/WelcomeBoard.tsx
import { useState } from 'react';
import ResidentCard from './ResidentCard';
import { Resident } from './types';

// Sample data
const residents: Resident[] = [
  {
    id: '1',
    name: 'SpongeBob SquarePants',
    role: 'Fry Cook',
    description: 'Optimistic sea sponge who loves his job at the Krusty Krab.',
    imageUrl: '/images/spongebob.png'
  },
  {
    id: '2',
    name: 'Patrick Star',
    role: 'Best Friend',
    description: 'SpongeBob\'s best friend and neighbor.',
    imageUrl: '/images/patrick.png'
  },
  {
    id: '3',
    name: 'Squidward Tentacles',
    role: 'Cashier',
    description: 'Grumpy octopus who works at the Krusty Krab.',
    imageUrl: '/images/squidward.png'
  }
];

function WelcomeBoard() {
  const [favorites, setFavorites] = useState<string[]>([]);

  const handleFavorite = (id: string) => {
    setFavorites(prev => 
      prev.includes(id) 
        ? prev.filter(favId => favId !== id)
        : [...prev, id]
    );
  };

  return (
    <div className="welcome-board">
      <h1>Welcome to Bikini Bottom!</h1>
      <p>Meet the residents:</p>
      <div className="residents-grid">
        {residents.map(resident => (
          <ResidentCard
            key={resident.id}
            resident={resident}
            onFavorite={handleFavorite}
            isFavorite={favorites.includes(resident.id)}
          />
        ))}
      </div>
      {favorites.length > 0 && (
        <p>You have {favorites.length} favorite{favorites.length > 1 ? 's' : ''}!</p>
      )}
    </div>
  );
}

export default WelcomeBoard;
```

## Example 4: Using the Components in App.tsx

```tsx
// src/App.tsx
import WelcomeBoard from './components/WelcomeBoard';
import './App.css';

function App() {
  return (
    <div className="App">
      <WelcomeBoard />
    </div>
  );
}

export default App;
```

## TypeScript Best Practices

### 1. Define Types in Separate File
```tsx
// src/components/types.ts
export interface ResidentCardProps {
  name: string;
  role: string;
  // ... other props
}
```

### 2. Use Type Inference for Event Handlers
```tsx
// Good - TypeScript infers the type
const handleClick = () => {
  console.log('clicked');
};

// Also good - Explicit typing for complex handlers
const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
  console.log(e.target.value);
};
```

### 3. Optional Props with Default Values
```tsx
interface ButtonProps {
  label: string;
  variant?: 'primary' | 'secondary'; // Optional with union type
  onClick?: () => void;
}

function Button({ 
  label, 
  variant = 'primary', // Default value
  onClick 
}: ButtonProps) {
  return (
    <button 
      className={`btn btn-${variant}`}
      onClick={onClick}
    >
      {label}
    </button>
  );
}
```

## Component Organization

Recommended folder structure:

```
src/
├── components/
│   ├── ResidentCard/
│   │   ├── ResidentCard.tsx
│   │   ├── ResidentCard.css
│   │   └── index.ts
│   ├── WelcomeBoard/
│   │   ├── WelcomeBoard.tsx
│   │   ├── WelcomeBoard.css
│   │   └── index.ts
│   └── types.ts
├── App.tsx
└── main.tsx
```

**index.ts pattern:**
```tsx
// src/components/ResidentCard/index.ts
export { default } from './ResidentCard';
export type { ResidentCardProps } from './ResidentCard';
```

## Styling Options

### Option 1: CSS Modules
```tsx
// ResidentCard.module.css
.residentCard {
  border: 1px solid #ccc;
  padding: 1rem;
  border-radius: 8px;
}

// ResidentCard.tsx
import styles from './ResidentCard.module.css';

function ResidentCard() {
  return <div className={styles.residentCard}>...</div>;
}
```

### Option 2: Tailwind CSS
```tsx
function ResidentCard() {
  return (
    <div className="border border-gray-300 p-4 rounded-lg">
      ...
    </div>
  );
}
```

## Common Patterns

### Conditional Rendering
```tsx
{isFavorite && <span>⭐</span>}
{error ? <ErrorMessage /> : <SuccessMessage />}
```

### Rendering Lists
```tsx
{residents.map(resident => (
  <ResidentCard key={resident.id} resident={resident} />
))}
```

### Event Handlers
```tsx
const handleClick = (id: string) => {
  console.log('Clicked:', id);
};

<button onClick={() => handleClick(resident.id)}>Click me</button>
```

---

**Related Task:** [Stage 1 Task Brief](../../tasks.md)

