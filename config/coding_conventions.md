# 📏 Coding Conventions

## 1. General Rules
- **Language**: JavaScript (ES6+) for both Frontend and Backend.
- **Indentation**: 2 Spaces.
- **Quotes**: Single quotes (`'`) preferred, double quotes (`"`) for JSON or JSX attributes.
- **Semicolons**: Always use semicolons.
- **Commits**: Follow Conventional Commits.
  - `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`, `chore:`

## 2. Naming Conventions

| Category | Case Type | Example |
|----------|-----------|---------|
| Variables | camelCase | `userName`, `isLoggedIn` |
| Functions | camelCase | `getUserData()`, `handleSubmit()` |
| Classes | PascalCase | `User`, `AuthService` |
| Constants | UPPER_SNAKE_CASE | `MAX_RETRY`, `API_URL` |
| Files | kebab-case / PascalCase | `user-service.js` / `UserProfile.jsx` |
| Directories| kebab-case | `components`, `api-routes` |

---

## 3. Frontend (React) Rules
- **Components**: Functional Components with Hooks.
- **File Name**: PascalCase for components (e.g., `Header.jsx`), camelCase for logic/hooks (e.g., `useAuth.js`).
- **Props**: Destructure props in function arguments.
- **State**: Use `useState` for local state, Context API for global state (if needed).
- **CSS**: Use styled-components or CSS Modules (avoid global CSS pollution).

**Example:**
```jsx
// Good
const UserProfile = ({ user }) => {
  const [isActive, setIsActive] = useState(false);
  return <div>{user.name}</div>;
};
```

---

## 4. Backend (Express) Rules
- **Architecture**: Separated into Routes (`routes/`), Controllers (`controllers/`), and Services (`services/`).
- **Async/Await**: Use `async/await` instead of Promises/Callbacks.
- **Error Handling**: Use a central error handling middleware.
- **Environment**: Use `.env` for sensitive data (DB credentials, API keys).

**Example:**
```javascript
// Good
exports.getUser = async (req, res, next) => {
  try {
    const user = await userService.findById(req.params.id);
    res.json(user);
  } catch (error) {
    next(error);
  }
};
```

---

## 5. Database (PostgreSQL) Rules
- **Table Names**: snake_case, plural (e.g., `users`, `posts`, `comments`).
- **Column Names**: snake_case (e.g., `created_at`, `user_id`).
- **Primary Key**: `id` (Serial/UUID).
- **Foreign Key**: `target_table_id` (e.g., `user_id`).

**SQL Example:**
```sql
CREATE TABLE posts (
  id SERIAL PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  author_id INTEGER REFERENCES users(id),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
