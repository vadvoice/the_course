# Stage 2 — `ResidentCard` Component Contract

Use this contract for the props/TypeScript interface while building the components lab or porting the card into the main app.

```ts
type ResidentRole = "fry-cook" | "best-friend" | "scientist";

type ResidentVibe = "optimistic" | "goofy" | "strategic";

type ResidentCardProps = {
  /** Character display name (e.g., "SpongeBob SquarePants") */
  name: string;
  /** URL to the character avatar art */
  avatarUrl: string;
  /** Job title or role within the Krusty Krab crew */
  role: ResidentRole;
  /** Short personality description shown under the name */
  vibe: ResidentVibe;
  /** Fun fact bullet points (<=3 recommended for layout) */
  facts: string[];
  /** Optional callback when “Ping” button is pressed */
  onPing?: (name: string) => void;
};
```

If you are using PropTypes instead of TypeScript, mirror the same constraints:

```js
ResidentCard.propTypes = {
  name: PropTypes.string.isRequired,
  avatarUrl: PropTypes.string.isRequired,
  role: PropTypes.oneOf(["fry-cook", "best-friend", "scientist"]).isRequired,
  vibe: PropTypes.oneOf(["optimistic", "goofy", "strategic"]).isRequired,
  facts: PropTypes.arrayOf(PropTypes.string).isRequired,
  onPing: PropTypes.func
};
```

Pair the contract with a small JSON seed file for local data or fetch character data from your own API.

---

**Related Task:** [Stage 2 Task Brief](../../tasks.md)

