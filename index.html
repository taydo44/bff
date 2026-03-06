import { useState, useEffect, useRef, useCallback } from "react";

// ─── Icons ────────────────────────────────────────────────────────────────────
const Icon = ({ d, size = 20, stroke = "currentColor", fill = "none", strokeWidth = 1.8 }) => (
  <svg width={size} height={size} viewBox="0 0 24 24" fill={fill} stroke={stroke} strokeWidth={strokeWidth} strokeLinecap="round" strokeLinejoin="round">
    {Array.isArray(d) ? d.map((p, i) => <path key={i} d={p} />) : <path d={d} />}
  </svg>
);

const Icons = {
  dashboard: "M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z",
  planner: "M8 6h13M8 12h13M8 18h13M3 6h.01M3 12h.01M3 18h.01",
  todo: "M9 11l3 3L22 4M21 12v7a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11",
  journal: "M2 3h6a4 4 0 0 1 4 4v14a3 3 0 0 0-3-3H2zM22 3h-6a4 4 0 0 0-4 4v14a3 3 0 0 1 3-3h7z",
  analytics: "M18 20V10M12 20V4M6 20v-6",
  settings: "M12 15a3 3 0 1 0 0-6 3 3 0 0 0 0 6z M19.4 15a1.65 1.65 0 0 0 .33 1.82l.06.06a2 2 0 0 1-2.83 2.83l-.06-.06a1.65 1.65 0 0 0-1.82-.33 1.65 1.65 0 0 0-1 1.51V21a2 2 0 0 1-4 0v-.09A1.65 1.65 0 0 0 9 19.4a1.65 1.65 0 0 0-1.82.33l-.06.06a2 2 0 0 1-2.83-2.83l.06-.06A1.65 1.65 0 0 0 4.68 15a1.65 1.65 0 0 0-1.51-1H3a2 2 0 0 1 0-4h.09A1.65 1.65 0 0 0 4.6 9a1.65 1.65 0 0 0-.33-1.82l-.06-.06a2 2 0 0 1 2.83-2.83l.06.06A1.65 1.65 0 0 0 9 4.68a1.65 1.65 0 0 0 1-1.51V3a2 2 0 0 1 4 0v.09a1.65 1.65 0 0 0 1 1.51 1.65 1.65 0 0 0 1.82-.33l.06-.06a2 2 0 0 1 2.83 2.83l-.06.06A1.65 1.65 0 0 0 19.4 9a1.65 1.65 0 0 0 1.51 1H21a2 2 0 0 1 0 4h-.09a1.65 1.65 0 0 0-1.51 1z",
  plus: "M12 5v14M5 12h14",
  check: "M20 6L9 17l-5-5",
  trash: "M3 6h18M8 6V4h8v2M19 6l-1 14a2 2 0 0 1-2 2H8a2 2 0 0 1-2-2L5 6",
  edit: "M11 4H4a2 2 0 0 0-2 2v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2v-7M18.5 2.5a2.121 2.121 0 0 1 3 3L12 15l-4 1 1-4 9.5-9.5z",
  sun: "M12 1v2M12 21v2M4.22 4.22l1.42 1.42M18.36 18.36l1.42 1.42M1 12h2M21 12h2M4.22 19.78l1.42-1.42M18.36 5.64l1.42-1.42M12 17a5 5 0 1 0 0-10 5 5 0 0 0 0 10z",
  moon: "M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z",
  flame: "M8.5 14.5A2.5 2.5 0 0 0 11 12c0-1.38-.5-2-1-3-1.072-2.143-.224-4.054 2-6 .5 2.5 2 4.9 4 6.5 2 1.6 3 3.5 3 5.5a7 7 0 1 1-14 0c0-1.153.433-2.294 1-3a2.5 2.5 0 0 0 2.5 2.5z",
  chevronLeft: "M15 18l-6-6 6-6",
  chevronRight: "M9 18l6-6-6-6",
  star: "M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z",
  tag: "M20.59 13.41l-7.17 7.17a2 2 0 0 1-2.83 0L2 12V2h10l8.59 8.59a2 2 0 0 1 0 2.82zM7 7h.01",
  calendar: "M3 9h18M16 3v6M8 3v6M3 6a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V6z",
  smile: "M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10zM8 14s1.5 2 4 2 4-2 4-2M9 9h.01M15 9h.01",
  meh: "M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10zM8 15h8M9 9h.01M15 9h.01",
  frown: "M12 22c5.523 0 10-4.477 10-10S17.523 2 12 2 2 6.477 2 12s4.477 10 10 10zM16 16s-1.5-2-4-2-4 2-4 2M9 9h.01M15 9h.01",
  x: "M18 6L6 18M6 6l12 12",
  save: "M19 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11l5 5v11a2 2 0 0 1-2 2zM17 21v-8H7v8M7 3v5h8",
  menu: "M3 12h18M3 6h18M3 18h18",
  zap: "M13 2L3 14h9l-1 8 10-12h-9l1-8z",
};

// ─── Utilities ────────────────────────────────────────────────────────────────
const today = () => new Date().toISOString().split("T")[0];
const fmtDate = (d) => new Date(d + "T00:00:00").toLocaleDateString("en-US", { weekday: "short", month: "short", day: "numeric" });
const DAYS = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
const MONTHS = ["January", "February", "March", "April", "May", "June", "July", "August", "September", "October", "November", "December"];

function useLocalStorage(key, init) {
  const [val, setVal] = useState(() => {
    try { const s = localStorage.getItem(key); return s ? JSON.parse(s) : init; } catch { return init; }
  });
  useEffect(() => { try { localStorage.setItem(key, JSON.stringify(val)); } catch {} }, [key, val]);
  return [val, setVal];
}

const uid = () => Math.random().toString(36).slice(2, 10);

// ─── Theme tokens ─────────────────────────────────────────────────────────────
const ACCENT_OPTIONS = [
  { label: "Iris", h: "263" },
  { label: "Violet", h: "250" },
  { label: "Mauve", h: "280" },
  { label: "Plum", h: "295" },
  { label: "Rose", h: "320" },
];

function buildCSS(dark, hue) {
  return dark ? `
    --bg: #0f0d14;
    --bg2: #1a1625;
    --bg3: #231e32;
    --card: #1e1a2e;
    --card2: #261f3a;
    --border: rgba(${hue === "263" ? "139,92,246" : "120,80,220"},0.18);
    --text: #e8e0f5;
    --text2: #a89dc8;
    --text3: #6b5f8a;
    --accent: hsl(${hue},80%,65%);
    --accent2: hsl(${hue},60%,45%);
    --accent-glow: hsl(${hue},80%,65%,0.25);
    --sidebar-bg: #130f1e;
    --success: #4ade80;
    --warn: #fbbf24;
    --danger: #f87171;
  ` : `
    --bg: #f5f3ff;
    --bg2: #ede9fe;
    --bg3: #e5dffd;
    --card: #ffffff;
    --card2: #faf8ff;
    --border: rgba(109,40,217,0.12);
    --text: #1e1433;
    --text2: #5b4e7e;
    --text3: #9585b8;
    --accent: hsl(${hue},70%,52%);
    --accent2: hsl(${hue},55%,38%);
    --accent-glow: hsl(${hue},70%,52%,0.2);
    --sidebar-bg: #fff;
    --success: #16a34a;
    --warn: #d97706;
    --danger: #dc2626;
  `;
}

// ─── Main App ─────────────────────────────────────────────────────────────────
export default function BabyFocusFlow() {
  const [dark, setDark] = useLocalStorage("bff-dark", true);
  const [hue, setHue] = useLocalStorage("bff-hue", "263");
  const [page, setPage] = useState("dashboard");
  const [sidebarOpen, setSidebarOpen] = useState(false);
  const [todos, setTodos] = useLocalStorage("bff-todos", []);
  const [events, setEvents] = useLocalStorage("bff-events", []);
  const [journals, setJournals] = useLocalStorage("bff-journals", {});

  const css = buildCSS(dark, hue);

  const navItems = [
    { id: "dashboard", label: "Dashboard", icon: Icons.dashboard },
    { id: "planner", label: "Planner", icon: Icons.planner },
    { id: "todo", label: "To-Do List", icon: Icons.todo },
    { id: "journal", label: "Journal", icon: Icons.journal },
    { id: "analytics", label: "Analytics", icon: Icons.analytics },
    { id: "settings", label: "Settings", icon: Icons.settings },
  ];

  return (
    <>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700;1,9..40,300&family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,400;0,9..144,600;1,9..144,300&display=swap');
        *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
        :root { ${css} }
        body { font-family: 'DM Sans', sans-serif; background: var(--bg); color: var(--text); min-height: 100vh; transition: background 0.3s, color 0.3s; }
        .app { display: flex; min-height: 100vh; }

        /* Sidebar */
        .sidebar {
          width: 240px; background: var(--sidebar-bg); border-right: 1px solid var(--border);
          display: flex; flex-direction: column; padding: 24px 16px;
          position: fixed; top: 0; left: 0; height: 100vh; z-index: 100;
          transition: transform 0.3s cubic-bezier(.4,0,.2,1), background 0.3s;
          box-shadow: 4px 0 30px rgba(0,0,0,0.08);
        }
        .sidebar.closed { transform: translateX(-100%); }
        .logo { font-family: 'Fraunces', serif; font-size: 20px; font-weight: 600;
          background: linear-gradient(135deg, var(--accent), var(--accent2));
          -webkit-background-clip: text; -webkit-text-fill-color: transparent;
          padding: 0 8px 24px; letter-spacing: -0.5px; }
        .logo span { font-style: italic; }
        .nav-item { display: flex; align-items: center; gap: 10px; padding: 10px 12px;
          border-radius: 12px; cursor: pointer; font-size: 14px; font-weight: 500;
          color: var(--text2); transition: all 0.2s; margin-bottom: 2px; }
        .nav-item:hover { background: var(--bg2); color: var(--text); }
        .nav-item.active { background: linear-gradient(135deg, var(--accent-glow), transparent);
          color: var(--accent); box-shadow: inset 0 0 0 1px var(--border); }
        .nav-icon { flex-shrink: 0; opacity: 0.8; }
        .sidebar-footer { margin-top: auto; padding-top: 16px; border-top: 1px solid var(--border); }
        .streak-badge { display: flex; align-items: center; gap: 8px; padding: 10px 12px;
          background: var(--bg2); border-radius: 12px; font-size: 13px; color: var(--text2); }
        .streak-num { font-weight: 700; color: var(--accent); font-size: 16px; }

        /* Content */
        .main { margin-left: 240px; flex: 1; padding: 32px; min-height: 100vh;
          transition: margin 0.3s; }
        .topbar { display: flex; align-items: center; justify-content: space-between;
          margin-bottom: 32px; }
        .page-title { font-family: 'Fraunces', serif; font-size: 28px; font-weight: 600;
          letter-spacing: -0.5px; }
        .page-subtitle { font-size: 14px; color: var(--text3); margin-top: 2px; }
        .menu-btn { display: none; background: var(--card); border: 1px solid var(--border);
          border-radius: 10px; padding: 8px; cursor: pointer; color: var(--text2);
          transition: all 0.2s; }
        .menu-btn:hover { background: var(--bg2); }

        /* Cards */
        .card { background: var(--card); border: 1px solid var(--border); border-radius: 18px;
          padding: 20px; transition: all 0.3s; }
        .card:hover { box-shadow: 0 8px 32px rgba(0,0,0,0.08); }
        .card-title { font-size: 12px; font-weight: 600; text-transform: uppercase;
          letter-spacing: 1px; color: var(--text3); margin-bottom: 12px; }

        /* Grid layouts */
        .grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
        .grid-3 { display: grid; grid-template-columns: repeat(3,1fr); gap: 16px; }
        .grid-auto { display: grid; grid-template-columns: repeat(auto-fill, minmax(280px,1fr)); gap: 16px; }
        .stack { display: flex; flex-direction: column; gap: 16px; }
        .row { display: flex; align-items: center; gap: 10px; }
        .spacer { flex: 1; }

        /* Buttons */
        .btn { display: inline-flex; align-items: center; gap: 6px; padding: 9px 16px;
          border-radius: 10px; font-size: 14px; font-weight: 500; cursor: pointer;
          border: none; transition: all 0.2s; font-family: inherit; }
        .btn-primary { background: linear-gradient(135deg, var(--accent), var(--accent2));
          color: #fff; box-shadow: 0 4px 12px var(--accent-glow); }
        .btn-primary:hover { transform: translateY(-1px); box-shadow: 0 6px 20px var(--accent-glow); }
        .btn-ghost { background: var(--bg2); color: var(--text2); }
        .btn-ghost:hover { background: var(--bg3); color: var(--text); }
        .btn-danger { background: rgba(248,113,113,0.15); color: var(--danger); }
        .btn-danger:hover { background: rgba(248,113,113,0.25); }
        .btn-icon { padding: 7px; border-radius: 8px; }
        .btn-sm { padding: 6px 12px; font-size: 13px; }

        /* Inputs */
        input, textarea, select {
          background: var(--bg2); border: 1px solid var(--border); border-radius: 10px;
          padding: 10px 14px; font-size: 14px; color: var(--text); font-family: inherit;
          transition: all 0.2s; outline: none; width: 100%; }
        input:focus, textarea:focus, select:focus {
          border-color: var(--accent); box-shadow: 0 0 0 3px var(--accent-glow); }
        select option { background: var(--card); }

        /* Todo items */
        .todo-item { display: flex; align-items: center; gap: 12px; padding: 14px 16px;
          background: var(--card); border: 1px solid var(--border); border-radius: 14px;
          transition: all 0.2s; }
        .todo-item:hover { box-shadow: 0 4px 16px rgba(0,0,0,0.06); }
        .todo-item.done { opacity: 0.55; }
        .check-box { width: 20px; height: 20px; border-radius: 6px; border: 2px solid var(--border);
          flex-shrink: 0; cursor: pointer; display: flex; align-items: center; justify-content: center;
          transition: all 0.2s; }
        .check-box.checked { background: var(--accent); border-color: var(--accent); }
        .todo-text { flex: 1; font-size: 14px; }
        .todo-text.done { text-decoration: line-through; color: var(--text3); }
        .priority-badge { font-size: 11px; font-weight: 600; padding: 3px 8px; border-radius: 6px; }
        .pri-high { background: rgba(248,113,113,0.15); color: var(--danger); }
        .pri-med { background: rgba(251,191,36,0.15); color: var(--warn); }
        .pri-low { background: rgba(74,222,128,0.15); color: var(--success); }
        .tag-pill { font-size: 11px; padding: 3px 8px; border-radius: 20px;
          background: var(--accent-glow); color: var(--accent); font-weight: 500; }

        /* Progress bar */
        .progress-bar { background: var(--bg2); border-radius: 100px; height: 8px; overflow: hidden; }
        .progress-fill { height: 100%; border-radius: 100px;
          background: linear-gradient(90deg, var(--accent), var(--accent2));
          transition: width 0.6s cubic-bezier(.4,0,.2,1); }

        /* Calendar */
        .cal-grid { display: grid; grid-template-columns: repeat(7,1fr); gap: 4px; }
        .cal-day { aspect-ratio: 1; display: flex; align-items: center; justify-content: center;
          border-radius: 8px; font-size: 13px; cursor: pointer; transition: all 0.15s; }
        .cal-day:hover { background: var(--bg2); }
        .cal-day.today { background: var(--accent); color: #fff; font-weight: 700; }
        .cal-day.has-event::after { content: ''; display: block; width: 4px; height: 4px;
          border-radius: 50%; background: var(--accent); position: absolute; bottom: 2px; }
        .cal-day { position: relative; }
        .cal-day.other-month { color: var(--text3); }
        .cal-header { display: flex; align-items: center; justify-content: space-between; margin-bottom: 12px; }

        /* Journal */
        .mood-btn { display: flex; flex-direction: column; align-items: center; gap: 4px;
          padding: 12px 16px; border-radius: 14px; border: 2px solid var(--border);
          background: var(--bg2); cursor: pointer; transition: all 0.2s; font-size: 12px;
          color: var(--text2); font-family: inherit; }
        .mood-btn.selected { border-color: var(--accent); background: var(--accent-glow);
          color: var(--accent); }
        .mood-btn:hover { border-color: var(--accent); }
        textarea.journal-editor { min-height: 200px; resize: vertical; line-height: 1.7;
          font-size: 15px; }

        /* Stat card */
        .stat-card { display: flex; flex-direction: column; gap: 6px; }
        .stat-num { font-size: 32px; font-weight: 700; font-family: 'Fraunces', serif;
          background: linear-gradient(135deg, var(--accent), var(--accent2));
          -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .stat-label { font-size: 13px; color: var(--text2); }

        /* Weekly chart */
        .chart-bars { display: flex; align-items: flex-end; gap: 8px; height: 100px; }
        .chart-bar-wrap { flex: 1; display: flex; flex-direction: column; align-items: center; gap: 6px; }
        .chart-bar { width: 100%; border-radius: 6px 6px 0 0;
          background: linear-gradient(180deg, var(--accent), var(--accent2));
          transition: height 0.6s cubic-bezier(.4,0,.2,1); min-height: 4px; }
        .chart-label { font-size: 11px; color: var(--text3); }

        /* Planner week */
        .week-grid { display: grid; grid-template-columns: repeat(7,1fr); gap: 8px; }
        .day-col { background: var(--card); border: 1px solid var(--border); border-radius: 14px;
          padding: 12px 8px; min-height: 200px; }
        .day-col-header { text-align: center; margin-bottom: 10px; }
        .day-col-name { font-size: 11px; color: var(--text3); font-weight: 600; text-transform: uppercase; }
        .day-col-num { font-size: 18px; font-weight: 700; font-family: 'Fraunces', serif; }
        .day-col.today-col { border-color: var(--accent); box-shadow: 0 0 0 1px var(--accent); }
        .event-chip { background: var(--accent-glow); border-left: 3px solid var(--accent);
          border-radius: 6px; padding: 6px 8px; font-size: 12px; margin-bottom: 4px;
          color: var(--text); cursor: pointer; transition: all 0.15s; }
        .event-chip:hover { background: var(--bg3); }

        /* Modal */
        .overlay { position: fixed; inset: 0; background: rgba(0,0,0,0.5);
          z-index: 200; display: flex; align-items: center; justify-content: center;
          backdrop-filter: blur(4px); animation: fadeIn 0.2s; }
        .modal { background: var(--card); border-radius: 20px; padding: 28px;
          width: min(480px, 90vw); border: 1px solid var(--border);
          box-shadow: 0 24px 64px rgba(0,0,0,0.2); animation: slideUp 0.25s cubic-bezier(.4,0,.2,1); }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes slideUp { from { transform: translateY(20px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        .modal-title { font-family: 'Fraunces', serif; font-size: 20px; font-weight: 600; margin-bottom: 20px; }
        .form-group { display: flex; flex-direction: column; gap: 6px; margin-bottom: 14px; }
        .form-label { font-size: 12px; font-weight: 600; color: var(--text2); text-transform: uppercase; letter-spacing: 0.5px; }

        /* Settings toggle */
        .toggle { width: 44px; height: 24px; border-radius: 100px; cursor: pointer;
          background: var(--bg3); border: 2px solid var(--border); transition: all 0.25s;
          position: relative; flex-shrink: 0; }
        .toggle.on { background: var(--accent); border-color: var(--accent); }
        .toggle::after { content: ''; position: absolute; width: 16px; height: 16px;
          border-radius: 50%; background: #fff; top: 2px; left: 2px; transition: all 0.25s;
          box-shadow: 0 2px 4px rgba(0,0,0,0.2); }
        .toggle.on::after { left: calc(100% - 18px); }
        .settings-row { display: flex; align-items: center; justify-content: space-between;
          padding: 14px 0; border-bottom: 1px solid var(--border); }
        .settings-row:last-child { border-bottom: none; }
        .accent-swatch { width: 32px; height: 32px; border-radius: 50%; cursor: pointer;
          border: 3px solid transparent; transition: all 0.2s; }
        .accent-swatch.active { border-color: var(--text); }

        /* Journal entries list */
        .entry-card { padding: 14px; background: var(--card2); border: 1px solid var(--border);
          border-radius: 12px; cursor: pointer; transition: all 0.2s; }
        .entry-card:hover { box-shadow: 0 4px 12px rgba(0,0,0,0.06); border-color: var(--accent); }
        .entry-date { font-size: 12px; color: var(--text3); margin-bottom: 4px; }
        .entry-preview { font-size: 13px; color: var(--text2); white-space: nowrap;
          overflow: hidden; text-overflow: ellipsis; }

        /* Responsive */
        @media (max-width: 768px) {
          .main { margin-left: 0; padding: 20px 16px; }
          .sidebar { transform: translateX(-100%); }
          .sidebar.open { transform: none; }
          .menu-btn { display: flex; }
          .grid-2, .grid-3 { grid-template-columns: 1fr; }
          .week-grid { grid-template-columns: repeat(3,1fr); }
        }

        /* Divider */
        .divider { height: 1px; background: var(--border); margin: 16px 0; }
        .empty-state { text-align: center; padding: 48px 16px; color: var(--text3); }
        .empty-state svg { margin-bottom: 12px; opacity: 0.4; }

        /* Overlay close on mobile */
        .sidebar-overlay { display: none; position: fixed; inset: 0; z-index: 99; background: rgba(0,0,0,0.4); }
        .sidebar-overlay.visible { display: block; }
      `}</style>

      <div className="app" style={{ background: "var(--bg)", color: "var(--text)" }}>
        {/* Mobile sidebar overlay */}
        <div className={`sidebar-overlay ${sidebarOpen ? "visible" : ""}`} onClick={() => setSidebarOpen(false)} />

        {/* Sidebar */}
        <aside className={`sidebar ${sidebarOpen ? "open" : "closed"}`}>
          <div className="logo">Baby<span>Focus</span>Flow</div>
          <nav>
            {navItems.map(n => (
              <div key={n.id} className={`nav-item ${page === n.id ? "active" : ""}`}
                onClick={() => { setPage(n.id); setSidebarOpen(false); }}>
                <span className="nav-icon"><Icon d={n.icon} size={16} /></span>
                {n.label}
              </div>
            ))}
          </nav>
          <div className="sidebar-footer">
            <JournalStreak journals={journals} />
          </div>
        </aside>

        {/* Main */}
        <main className="main">
          <div className="topbar">
            <button className="menu-btn btn" onClick={() => setSidebarOpen(o => !o)}>
              <Icon d={Icons.menu} size={18} />
            </button>
            <div>
              <div className="page-title">{navItems.find(n => n.id === page)?.label}</div>
              <div className="page-subtitle">{new Date().toLocaleDateString("en-US", { weekday: "long", month: "long", day: "numeric", year: "numeric" })}</div>
            </div>
            <button className="btn btn-ghost btn-icon" onClick={() => setDark(d => !d)}>
              <Icon d={dark ? Icons.sun : Icons.moon} size={18} />
            </button>
          </div>

          {page === "dashboard" && <Dashboard todos={todos} events={events} journals={journals} setPage={setPage} />}
          {page === "planner" && <Planner events={events} setEvents={setEvents} todos={todos} setTodos={setTodos} />}
          {page === "todo" && <TodoList todos={todos} setTodos={setTodos} />}
          {page === "journal" && <Journal journals={journals} setJournals={setJournals} />}
          {page === "analytics" && <Analytics todos={todos} journals={journals} />}
          {page === "settings" && <Settings dark={dark} setDark={setDark} hue={hue} setHue={setHue} />}
        </main>
      </div>
    </>
  );
}

// ─── Journal Streak ────────────────────────────────────────────────────────────
function JournalStreak({ journals }) {
  const streak = (() => {
    let s = 0, d = new Date();
    while (true) {
      const k = d.toISOString().split("T")[0];
      if (journals[k]) { s++; d.setDate(d.getDate() - 1); } else break;
    }
    return s;
  })();
  return (
    <div className="streak-badge">
      <Icon d={Icons.flame} size={16} style={{ color: "#f97316" }} />
      <span><span className="streak-num">{streak}</span> day streak</span>
    </div>
  );
}

// ─── Dashboard ────────────────────────────────────────────────────────────────
function Dashboard({ todos, events, journals, setPage }) {
  const todayStr = today();
  const todayTodos = todos.filter(t => !t.date || t.date === todayStr);
  const done = todayTodos.filter(t => t.done).length;
  const total = todayTodos.length;
  const pct = total ? Math.round((done / total) * 100) : 0;

  const streak = (() => {
    let s = 0, d = new Date();
    while (true) {
      const k = d.toISOString().split("T")[0];
      if (journals[k]) { s++; d.setDate(d.getDate() - 1); } else break;
    }
    return s;
  })();

  const todayEvents = events.filter(e => e.date === todayStr);

  return (
    <div className="stack">
      {/* Stats row */}
      <div className="grid-3">
        <div className="card stat-card">
          <div className="stat-num">{done}/{total}</div>
          <div className="stat-label">Tasks completed today</div>
        </div>
        <div className="card stat-card">
          <div className="stat-num">{streak}</div>
          <div className="stat-label">Journal streak (days)</div>
        </div>
        <div className="card stat-card">
          <div className="stat-num">{todayEvents.length}</div>
          <div className="stat-label">Events today</div>
        </div>
      </div>

      <div className="grid-2">
        {/* Today's tasks */}
        <div className="card">
          <div className="card-title">Today's Tasks</div>
          <div style={{ marginBottom: 12 }}>
            <div style={{ display: "flex", justifyContent: "space-between", fontSize: 13, color: "var(--text2)", marginBottom: 6 }}>
              <span>{done} of {total} done</span><span>{pct}%</span>
            </div>
            <div className="progress-bar"><div className="progress-fill" style={{ width: pct + "%" }} /></div>
          </div>
          <div className="stack">
            {todayTodos.slice(0, 4).map(t => (
              <div key={t.id} className="row" style={{ fontSize: 14 }}>
                <div style={{ width: 8, height: 8, borderRadius: "50%", background: t.done ? "var(--success)" : "var(--border)", flexShrink: 0 }} />
                <span style={{ textDecoration: t.done ? "line-through" : "none", color: t.done ? "var(--text3)" : "var(--text)" }}>{t.text}</span>
              </div>
            ))}
            {total === 0 && <div style={{ color: "var(--text3)", fontSize: 13 }}>No tasks for today. Add some!</div>}
          </div>
          <button className="btn btn-ghost btn-sm" style={{ marginTop: 12 }} onClick={() => setPage("todo")}>
            View all tasks →
          </button>
        </div>

        {/* Mini calendar */}
        <div className="card">
          <MiniCalendar events={events} />
        </div>
      </div>

      {/* Today's events */}
      {todayEvents.length > 0 && (
        <div className="card">
          <div className="card-title">Today's Events</div>
          <div className="stack">
            {todayEvents.map(e => (
              <div key={e.id} className="event-chip">{e.title} {e.time && <span style={{ opacity: 0.7 }}>· {e.time}</span>}</div>
            ))}
          </div>
        </div>
      )}

      {/* Recent journal */}
      <div className="card">
        <div className="card-title">Recent Journal</div>
        {journals[todayStr] ? (
          <div>
            <div style={{ fontSize: 14, color: "var(--text2)", marginBottom: 8 }}>
              {journals[todayStr].mood && <span style={{ marginRight: 8 }}>{journals[todayStr].mood === "happy" ? "😊" : journals[todayStr].mood === "neutral" ? "😐" : "😔"}</span>}
              Today's entry
            </div>
            <div style={{ fontSize: 14, color: "var(--text3)", fontStyle: "italic" }}>
              {journals[todayStr].text?.slice(0, 120)}{journals[todayStr].text?.length > 120 ? "…" : ""}
            </div>
          </div>
        ) : (
          <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
            <span style={{ fontSize: 13, color: "var(--text3)" }}>No entry yet today.</span>
            <button className="btn btn-primary btn-sm" onClick={() => setPage("journal")}>Write now</button>
          </div>
        )}
      </div>
    </div>
  );
}

// ─── Mini Calendar ─────────────────────────────────────────────────────────────
function MiniCalendar({ events }) {
  const [cur, setCur] = useState(new Date());
  const year = cur.getFullYear(), month = cur.getMonth();
  const first = new Date(year, month, 1).getDay();
  const days = new Date(year, month + 1, 0).getDate();
  const todayStr = today();
  const eventDates = new Set(events.map(e => e.date));

  const cells = [];
  for (let i = 0; i < first; i++) cells.push(null);
  for (let d = 1; d <= days; d++) cells.push(d);

  return (
    <div>
      <div className="cal-header">
        <button className="btn btn-ghost btn-icon btn-sm" onClick={() => setCur(new Date(year, month - 1))}>
          <Icon d={Icons.chevronLeft} size={14} />
        </button>
        <span style={{ fontSize: 14, fontWeight: 600 }}>{MONTHS[month]} {year}</span>
        <button className="btn btn-ghost btn-icon btn-sm" onClick={() => setCur(new Date(year, month + 1))}>
          <Icon d={Icons.chevronRight} size={14} />
        </button>
      </div>
      <div className="cal-grid" style={{ marginBottom: 6 }}>
        {DAYS.map(d => <div key={d} style={{ textAlign: "center", fontSize: 11, color: "var(--text3)", fontWeight: 600, padding: "4px 0" }}>{d[0]}</div>)}
      </div>
      <div className="cal-grid">
        {cells.map((d, i) => {
          if (!d) return <div key={`e${i}`} />;
          const ds = `${year}-${String(month + 1).padStart(2, "0")}-${String(d).padStart(2, "0")}`;
          const isToday = ds === todayStr;
          const hasEv = eventDates.has(ds);
          return (
            <div key={i} className={`cal-day${isToday ? " today" : ""}${hasEv ? " has-event" : ""}`} style={{ fontSize: 12 }}>
              {d}
              {hasEv && !isToday && <span style={{ position: "absolute", bottom: 2, left: "50%", transform: "translateX(-50%)", width: 4, height: 4, borderRadius: "50%", background: "var(--accent)", display: "block" }} />}
            </div>
          );
        })}
      </div>
    </div>
  );
}

// ─── Planner ──────────────────────────────────────────────────────────────────
function Planner({ events, setEvents }) {
  const [weekOffset, setWeekOffset] = useState(0);
  const [showModal, setShowModal] = useState(false);
  const [editEvent, setEditEvent] = useState(null);
  const [dragId, setDragId] = useState(null);

  const getWeekDays = (offset) => {
    const now = new Date();
    const monday = new Date(now);
    monday.setDate(now.getDate() - now.getDay() + 1 + offset * 7);
    return Array.from({ length: 7 }, (_, i) => {
      const d = new Date(monday);
      d.setDate(monday.getDate() + i);
      return d;
    });
  };

  const weekDays = getWeekDays(weekOffset);
  const todayStr = today();

  const handleDrop = (dateStr, e) => {
    e.preventDefault();
    if (!dragId) return;
    setEvents(ev => ev.map(ev2 => ev2.id === dragId ? { ...ev2, date: dateStr } : ev2));
    setDragId(null);
  };

  return (
    <div className="stack">
      <div className="row">
        <button className="btn btn-ghost btn-sm" onClick={() => setWeekOffset(o => o - 1)}>
          <Icon d={Icons.chevronLeft} size={14} /> Prev
        </button>
        <button className="btn btn-ghost btn-sm" onClick={() => setWeekOffset(0)}>Today</button>
        <button className="btn btn-ghost btn-sm" onClick={() => setWeekOffset(o => o + 1)}>
          Next <Icon d={Icons.chevronRight} size={14} />
        </button>
        <div className="spacer" />
        <button className="btn btn-primary btn-sm" onClick={() => { setEditEvent(null); setShowModal(true); }}>
          <Icon d={Icons.plus} size={14} /> Add Event
        </button>
      </div>

      <div className="week-grid">
        {weekDays.map(date => {
          const ds = date.toISOString().split("T")[0];
          const dayEvents = events.filter(e => e.date === ds);
          const isToday = ds === todayStr;
          return (
            <div key={ds} className={`day-col${isToday ? " today-col" : ""}`}
              onDragOver={e => e.preventDefault()}
              onDrop={e => handleDrop(ds, e)}>
              <div className="day-col-header">
                <div className="day-col-name">{DAYS[date.getDay()]}</div>
                <div className="day-col-num" style={{ color: isToday ? "var(--accent)" : "var(--text)" }}>{date.getDate()}</div>
              </div>
              {dayEvents.map(ev => (
                <div key={ev.id} className="event-chip"
                  draggable onDragStart={() => setDragId(ev.id)}
                  onClick={() => { setEditEvent(ev); setShowModal(true); }}>
                  <div style={{ fontWeight: 500 }}>{ev.title}</div>
                  {ev.time && <div style={{ opacity: 0.7, fontSize: 11 }}>{ev.time}</div>}
                </div>
              ))}
              <button className="btn btn-ghost" style={{ width: "100%", fontSize: 12, padding: "6px", opacity: 0.5, marginTop: 4 }}
                onClick={() => { setEditEvent({ date: ds }); setShowModal(true); }}>
                <Icon d={Icons.plus} size={12} />
              </button>
            </div>
          );
        })}
      </div>

      {showModal && (
        <EventModal
          initial={editEvent}
          onSave={(ev) => {
            if (ev.id) setEvents(evs => evs.map(e => e.id === ev.id ? ev : e));
            else setEvents(evs => [...evs, { ...ev, id: uid() }]);
            setShowModal(false);
          }}
          onDelete={(id) => { setEvents(evs => evs.filter(e => e.id !== id)); setShowModal(false); }}
          onClose={() => setShowModal(false)}
        />
      )}
    </div>
  );
}

function EventModal({ initial, onSave, onDelete, onClose }) {
  const [form, setForm] = useState({ title: "", date: today(), time: "", notes: "", ...initial });
  const set = (k, v) => setForm(f => ({ ...f, [k]: v }));
  return (
    <div className="overlay" onClick={e => e.target === e.currentTarget && onClose()}>
      <div className="modal">
        <div className="row">
          <div className="modal-title">{form.id ? "Edit Event" : "Add Event"}</div>
          <div className="spacer" />
          <button className="btn btn-ghost btn-icon" onClick={onClose}><Icon d={Icons.x} size={16} /></button>
        </div>
        <div className="form-group"><div className="form-label">Title</div>
          <input value={form.title} onChange={e => set("title", e.target.value)} placeholder="Event title" /></div>
        <div className="grid-2">
          <div className="form-group"><div className="form-label">Date</div>
            <input type="date" value={form.date} onChange={e => set("date", e.target.value)} /></div>
          <div className="form-group"><div className="form-label">Time</div>
            <input type="time" value={form.time} onChange={e => set("time", e.target.value)} /></div>
        </div>
        <div className="form-group"><div className="form-label">Notes</div>
          <textarea value={form.notes} onChange={e => set("notes", e.target.value)} rows={3} placeholder="Optional notes…" /></div>
        <div className="row" style={{ marginTop: 8 }}>
          {form.id && <button className="btn btn-danger btn-sm" onClick={() => onDelete(form.id)}>Delete</button>}
          <div className="spacer" />
          <button className="btn btn-ghost btn-sm" onClick={onClose}>Cancel</button>
          <button className="btn btn-primary btn-sm" onClick={() => form.title && onSave(form)}>Save</button>
        </div>
      </div>
    </div>
  );
}

// ─── To-Do List ───────────────────────────────────────────────────────────────
const PRIORITIES = ["low", "medium", "high"];
const TAGS = ["Work", "Personal", "Health", "Learning", "Home"];

function TodoList({ todos, setTodos }) {
  const [showModal, setShowModal] = useState(false);
  const [editTodo, setEditTodo] = useState(null);
  const [filter, setFilter] = useState("all");
  const [tagFilter, setTagFilter] = useState("all");

  const toggle = (id) => setTodos(ts => ts.map(t => t.id === id ? { ...t, done: !t.done } : t));
  const del = (id) => setTodos(ts => ts.filter(t => t.id !== id));

  const filtered = todos
    .filter(t => filter === "all" ? true : filter === "done" ? t.done : !t.done)
    .filter(t => tagFilter === "all" ? true : t.tags?.includes(tagFilter))
    .sort((a, b) => { const p = { high: 0, medium: 1, low: 2 }; return (p[a.priority] ?? 1) - (p[b.priority] ?? 1); });

  const done = todos.filter(t => t.done).length;
  const pct = todos.length ? Math.round((done / todos.length) * 100) : 0;

  return (
    <div className="stack">
      <div className="card">
        <div className="row" style={{ marginBottom: 10 }}>
          <span style={{ fontSize: 13, color: "var(--text2)" }}>{done} of {todos.length} completed</span>
          <div className="spacer" />
          <span style={{ fontSize: 13, fontWeight: 600, color: "var(--accent)" }}>{pct}%</span>
        </div>
        <div className="progress-bar"><div className="progress-fill" style={{ width: pct + "%" }} /></div>
      </div>

      <div className="row" style={{ flexWrap: "wrap", gap: 8 }}>
        {["all", "active", "done"].map(f => (
          <button key={f} className={`btn btn-sm ${filter === f ? "btn-primary" : "btn-ghost"}`}
            onClick={() => setFilter(f)} style={{ textTransform: "capitalize" }}>{f}</button>
        ))}
        <div className="spacer" />
        <button className="btn btn-primary btn-sm" onClick={() => { setEditTodo(null); setShowModal(true); }}>
          <Icon d={Icons.plus} size={14} /> New Task
        </button>
      </div>

      <div className="row" style={{ flexWrap: "wrap", gap: 6 }}>
        <button className={`btn btn-sm ${tagFilter === "all" ? "btn-primary" : "btn-ghost"}`} onClick={() => setTagFilter("all")}>All</button>
        {TAGS.map(t => (
          <button key={t} className={`btn btn-sm ${tagFilter === t ? "btn-primary" : "btn-ghost"}`} onClick={() => setTagFilter(t)}>{t}</button>
        ))}
      </div>

      {filtered.length === 0 && (
        <div className="empty-state">
          <Icon d={Icons.todo} size={40} />
          <div>No tasks here. Add one!</div>
        </div>
      )}

      <div className="stack">
        {filtered.map(t => (
          <div key={t.id} className={`todo-item${t.done ? " done" : ""}`}>
            <div className={`check-box${t.done ? " checked" : ""}`} onClick={() => toggle(t.id)}>
              {t.done && <Icon d={Icons.check} size={12} stroke="#fff" strokeWidth={2.5} />}
            </div>
            <div style={{ flex: 1, minWidth: 0 }}>
              <div className={`todo-text${t.done ? " done" : ""}`}>{t.text}</div>
              <div className="row" style={{ flexWrap: "wrap", gap: 6, marginTop: 6 }}>
                {t.priority && <span className={`priority-badge pri-${t.priority.slice(0, 3) === "med" ? "med" : t.priority.slice(0, 3)}`}>{t.priority}</span>}
                {t.due && <span style={{ fontSize: 11, color: "var(--text3)" }}>{fmtDate(t.due)}</span>}
                {t.tags?.map(tag => <span key={tag} className="tag-pill">{tag}</span>)}
              </div>
            </div>
            <button className="btn btn-ghost btn-icon btn-sm" onClick={() => { setEditTodo(t); setShowModal(true); }}>
              <Icon d={Icons.edit} size={14} />
            </button>
            <button className="btn btn-danger btn-icon btn-sm" onClick={() => del(t.id)}>
              <Icon d={Icons.trash} size={14} />
            </button>
          </div>
        ))}
      </div>

      {showModal && (
        <TodoModal
          initial={editTodo}
          onSave={(t) => {
            if (t.id) setTodos(ts => ts.map(x => x.id === t.id ? t : x));
            else setTodos(ts => [...ts, { ...t, id: uid(), done: false }]);
            setShowModal(false);
          }}
          onClose={() => setShowModal(false)}
        />
      )}
    </div>
  );
}

function TodoModal({ initial, onSave, onClose }) {
  const [form, setForm] = useState({ text: "", priority: "medium", due: "", tags: [], ...initial });
  const set = (k, v) => setForm(f => ({ ...f, [k]: v }));
  const toggleTag = (t) => set("tags", form.tags?.includes(t) ? form.tags.filter(x => x !== t) : [...(form.tags || []), t]);
  return (
    <div className="overlay" onClick={e => e.target === e.currentTarget && onClose()}>
      <div className="modal">
        <div className="row">
          <div className="modal-title">{form.id ? "Edit Task" : "New Task"}</div>
          <div className="spacer" />
          <button className="btn btn-ghost btn-icon" onClick={onClose}><Icon d={Icons.x} size={16} /></button>
        </div>
        <div className="form-group"><div className="form-label">Task</div>
          <input value={form.text} onChange={e => set("text", e.target.value)} placeholder="What needs to be done?" autoFocus /></div>
        <div className="grid-2">
          <div className="form-group"><div className="form-label">Priority</div>
            <select value={form.priority} onChange={e => set("priority", e.target.value)}>
              {PRIORITIES.map(p => <option key={p} value={p} style={{ textTransform: "capitalize" }}>{p.charAt(0).toUpperCase() + p.slice(1)}</option>)}
            </select></div>
          <div className="form-group"><div className="form-label">Due Date</div>
            <input type="date" value={form.due} onChange={e => set("due", e.target.value)} /></div>
        </div>
        <div className="form-group">
          <div className="form-label">Tags</div>
          <div className="row" style={{ flexWrap: "wrap", gap: 6 }}>
            {TAGS.map(t => (
              <button key={t} onClick={() => toggleTag(t)}
                className={`btn btn-sm ${form.tags?.includes(t) ? "btn-primary" : "btn-ghost"}`}>{t}</button>
            ))}
          </div>
        </div>
        <div className="row" style={{ marginTop: 8 }}>
          <div className="spacer" />
          <button className="btn btn-ghost btn-sm" onClick={onClose}>Cancel</button>
          <button className="btn btn-primary btn-sm" onClick={() => form.text && onSave(form)}>Save</button>
        </div>
      </div>
    </div>
  );
}

// ─── Journal ──────────────────────────────────────────────────────────────────
const MOODS = [
  { id: "happy", emoji: "😊", label: "Happy" },
  { id: "neutral", emoji: "😐", label: "Neutral" },
  { id: "sad", emoji: "😔", label: "Sad" },
];

function Journal({ journals, setJournals }) {
  const [selectedDate, setSelectedDate] = useState(today());
  const [draft, setDraft] = useState("");
  const [mood, setMood] = useState("");
  const [saved, setSaved] = useState(false);
  const [view, setView] = useState("write"); // write | entries

  useEffect(() => {
    const entry = journals[selectedDate];
    setDraft(entry?.text || "");
    setMood(entry?.mood || "");
    setSaved(!!entry);
  }, [selectedDate, journals]);

  const save = () => {
    setJournals(j => ({ ...j, [selectedDate]: { text: draft, mood, updatedAt: new Date().toISOString() } }));
    setSaved(true);
  };

  const entries = Object.entries(journals).sort((a, b) => b[0].localeCompare(a[0]));

  return (
    <div className="stack">
      <div className="row">
        <button className={`btn btn-sm ${view === "write" ? "btn-primary" : "btn-ghost"}`} onClick={() => setView("write")}>
          <Icon d={Icons.edit} size={14} /> Write
        </button>
        <button className={`btn btn-sm ${view === "entries" ? "btn-primary" : "btn-ghost"}`} onClick={() => setView("entries")}>
          <Icon d={Icons.journal} size={14} /> All Entries
        </button>
        <div className="spacer" />
        <input type="date" value={selectedDate} onChange={e => setSelectedDate(e.target.value)}
          style={{ width: "auto", padding: "6px 10px", fontSize: 13 }} />
      </div>

      {view === "write" && (
        <div className="card stack">
          <div>
            <div className="card-title">How are you feeling?</div>
            <div className="row" style={{ gap: 12 }}>
              {MOODS.map(m => (
                <button key={m.id} className={`mood-btn${mood === m.id ? " selected" : ""}`} onClick={() => setMood(m.id)}>
                  <span style={{ fontSize: 24 }}>{m.emoji}</span>
                  <span>{m.label}</span>
                </button>
              ))}
            </div>
          </div>
          <div className="divider" />
          <div>
            <div className="card-title">{fmtDate(selectedDate)}</div>
            <textarea
              className="journal-editor"
              value={draft}
              onChange={e => { setDraft(e.target.value); setSaved(false); }}
              placeholder="What's on your mind today? Reflect on your thoughts, feelings, and experiences…"
            />
          </div>
          <div className="row">
            <span style={{ fontSize: 12, color: "var(--text3)" }}>
              {saved ? "✓ Saved" : draft ? "Unsaved changes" : ""}
            </span>
            <div className="spacer" />
            <button className="btn btn-primary" onClick={save}>
              <Icon d={Icons.save} size={15} /> Save Entry
            </button>
          </div>
        </div>
      )}

      {view === "entries" && (
        <div className="stack">
          {entries.length === 0 && (
            <div className="empty-state">
              <Icon d={Icons.journal} size={40} />
              <div>No journal entries yet. Start writing!</div>
            </div>
          )}
          {entries.map(([date, entry]) => (
            <div key={date} className="entry-card"
              onClick={() => { setSelectedDate(date); setView("write"); }}>
              <div className="row">
                <div className="entry-date">{fmtDate(date)}</div>
                {entry.mood && <span style={{ fontSize: 16 }}>{MOODS.find(m => m.id === entry.mood)?.emoji}</span>}
              </div>
              <div className="entry-preview">{entry.text || "(empty)"}</div>
            </div>
          ))}
        </div>
      )}
    </div>
  );
}

// ─── Analytics ────────────────────────────────────────────────────────────────
function Analytics({ todos, journals }) {
  const last7 = Array.from({ length: 7 }, (_, i) => {
    const d = new Date(); d.setDate(d.getDate() - (6 - i));
    const ds = d.toISOString().split("T")[0];
    const dayTodos = todos.filter(t => t.date === ds);
    return {
      label: DAYS[d.getDay()],
      total: dayTodos.length,
      done: dayTodos.filter(t => t.done).length,
      hasJournal: !!journals[ds],
    };
  });

  const totalDone = todos.filter(t => t.done).length;
  const totalTasks = todos.length;
  const completionRate = totalTasks ? Math.round((totalDone / totalTasks) * 100) : 0;

  const streak = (() => {
    let s = 0, d = new Date();
    while (true) {
      const k = d.toISOString().split("T")[0];
      if (journals[k]) { s++; d.setDate(d.getDate() - 1); } else break;
    }
    return s;
  })();

  const byPriority = { high: 0, medium: 0, low: 0 };
  todos.forEach(t => { if (byPriority[t.priority] !== undefined) byPriority[t.priority]++; });

  const maxBar = Math.max(...last7.map(d => d.total), 1);

  return (
    <div className="stack">
      <div className="grid-3">
        <div className="card stat-card">
          <div className="stat-num">{completionRate}%</div>
          <div className="stat-label">Overall completion rate</div>
        </div>
        <div className="card stat-card">
          <div className="stat-num">{streak}</div>
          <div className="stat-label">Current journal streak</div>
        </div>
        <div className="card stat-card">
          <div className="stat-num">{Object.keys(journals).length}</div>
          <div className="stat-label">Total journal entries</div>
        </div>
      </div>

      <div className="card">
        <div className="card-title">7-Day Task Activity</div>
        <div className="chart-bars">
          {last7.map((d, i) => (
            <div key={i} className="chart-bar-wrap">
              <div className="chart-bar" style={{ height: `${(d.total / maxBar) * 80}px` }} title={`${d.done}/${d.total} tasks`} />
              <div className="chart-label">{d.label}</div>
            </div>
          ))}
        </div>
        <div className="row" style={{ marginTop: 12, gap: 16 }}>
          {last7.map((d, i) => (
            <div key={i} style={{ flex: 1, textAlign: "center" }}>
              <div style={{ fontSize: 11, color: d.hasJournal ? "var(--accent)" : "var(--text3)" }}>
                {d.hasJournal ? "📔" : "·"}
              </div>
            </div>
          ))}
        </div>
        <div style={{ fontSize: 12, color: "var(--text3)", marginTop: 4 }}>📔 = journal entry written</div>
      </div>

      <div className="card">
        <div className="card-title">Tasks by Priority</div>
        {["high", "medium", "low"].map(p => {
          const count = byPriority[p];
          const pct = totalTasks ? Math.round((count / totalTasks) * 100) : 0;
          return (
            <div key={p} style={{ marginBottom: 12 }}>
              <div className="row" style={{ marginBottom: 6 }}>
                <span className={`priority-badge pri-${p === "medium" ? "med" : p}`}>{p}</span>
                <div className="spacer" />
                <span style={{ fontSize: 13, color: "var(--text2)" }}>{count} tasks</span>
              </div>
              <div className="progress-bar"><div className="progress-fill" style={{ width: pct + "%" }} /></div>
            </div>
          );
        })}
      </div>

      <div className="card">
        <div className="card-title">Journal Mood History</div>
        <div className="row" style={{ flexWrap: "wrap", gap: 8 }}>
          {Object.entries(journals).slice(-14).map(([date, entry]) => (
            <div key={date} title={date} style={{ textAlign: "center" }}>
              <div style={{ fontSize: 20 }}>{MOODS.find(m => m.id === entry.mood)?.emoji || "📝"}</div>
              <div style={{ fontSize: 10, color: "var(--text3)" }}>{new Date(date + "T00:00:00").getDate()}</div>
            </div>
          ))}
          {Object.keys(journals).length === 0 && <div style={{ color: "var(--text3)", fontSize: 13 }}>No entries yet.</div>}
        </div>
      </div>
    </div>
  );
}

// ─── Settings ─────────────────────────────────────────────────────────────────
function Settings({ dark, setDark, hue, setHue }) {
  return (
    <div className="stack">
      <div className="card">
        <div className="card-title">Appearance</div>
        <div className="settings-row">
          <div>
            <div style={{ fontWeight: 500 }}>Dark Mode</div>
            <div style={{ fontSize: 13, color: "var(--text3)" }}>Use the dark purple theme</div>
          </div>
          <div className={`toggle${dark ? " on" : ""}`} onClick={() => setDark(d => !d)} />
        </div>
        <div className="settings-row">
          <div>
            <div style={{ fontWeight: 500 }}>Accent Color</div>
            <div style={{ fontSize: 13, color: "var(--text3)" }}>Choose your purple shade</div>
          </div>
          <div className="row" style={{ gap: 8 }}>
            {ACCENT_OPTIONS.map(a => (
              <div key={a.h} title={a.label}
                className={`accent-swatch${hue === a.h ? " active" : ""}`}
                style={{ background: `hsl(${a.h},70%,55%)` }}
                onClick={() => setHue(a.h)} />
            ))}
          </div>
        </div>
      </div>

      <div className="card">
        <div className="card-title">About</div>
        <div className="settings-row">
          <div>
            <div style={{ fontWeight: 500 }}>BabyFocusFlow</div>
            <div style={{ fontSize: 13, color: "var(--text3)" }}>Your mindful productivity companion</div>
          </div>
          <span style={{ fontSize: 13, color: "var(--accent)", fontWeight: 600 }}>v1.0</span>
        </div>
        <div className="settings-row">
          <div>
            <div style={{ fontWeight: 500 }}>Data Storage</div>
            <div style={{ fontSize: 13, color: "var(--text3)" }}>All data saved locally in your browser</div>
          </div>
          <Icon d={Icons.save} size={16} style={{ color: "var(--text3)" }} />
        </div>
      </div>

      <div className="card">
        <div className="card-title">Tips</div>
        {[
          { icon: Icons.zap, tip: "Use the Planner to drag tasks between days" },
          { icon: Icons.flame, tip: "Build your journal streak by writing daily" },
          { icon: Icons.star, tip: "Tag your to-dos to stay organized by category" },
          { icon: Icons.analytics, tip: "Check Analytics to see your weekly patterns" },
        ].map((t, i) => (
          <div key={i} className="row" style={{ padding: "10px 0", borderBottom: i < 3 ? "1px solid var(--border)" : "none" }}>
            <Icon d={t.icon} size={16} style={{ color: "var(--accent)", flexShrink: 0 }} />
            <span style={{ fontSize: 14, color: "var(--text2)" }}>{t.tip}</span>
          </div>
        ))}
      </div>
    </div>
  );
}
