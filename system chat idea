

<!DOCTYPE html>
<html lang="en">
<head>
   <meta charset="UTF-8
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>My Website</title>
</head>
<body>
   <h1>Hello World, this is my first web page.</h1>
</body>
</html>
  <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Chat Idea – AI Chat</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    :root {
      --bg-main: #050816;
      --bg-elevated: #0b1020;
      --bg-input: #050816;
      --accent: #4f46e5;
      --accent-soft: rgba(79, 70, 229, 0.2);
      --accent-strong: #818cf8;
      --text-main: #f9fafb;
      --text-muted: #9ca3af;
      --border-subtle: #1f2933;
      --danger: #f97373;
      --radius-lg: 18px;
      --radius-md: 12px;
      --radius-pill: 999px;
      --shadow-soft: 0 18px 45px rgba(0, 0, 0, 0.55);
      --shadow-glow: 0 0 40px rgba(79, 70, 229, 0.45);
      --transition-fast: 0.18s ease-out;
      --font-sans: system-ui, -apple-system, BlinkMacSystemFont, "SF Pro Text",
        "Segoe UI", sans-serif;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html,
    body {
      height: 100%;
      background: radial-gradient(circle at top, #111827 0, #020617 45%, #000 100%);
      color: var(--text-main);
      font-family: var(--font-sans);
      -webkit-font-smoothing: antialiased;
    }

    body {
      display: flex;
      align-items: stretch;
      justify-content: center;
      padding: 16px;
    }

    .app-shell {
      display: grid;
      grid-template-columns: 260px minmax(0, 1fr);
      gap: 16px;
      width: 100%;
      max-width: 1240px;
      height: 100%;
      max-height: 760px;
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.96), rgba(2, 6, 23, 0.98));
      border-radius: 28px;
      border: 1px solid rgba(148, 163, 184, 0.18);
      box-shadow: var(--shadow-soft);
      overflow: hidden;
      position: relative;
    }

    /* Subtle glow orbs */
    .orb {
      position: absolute;
      border-radius: 999px;
      filter: blur(40px);
      opacity: 0.7;
      pointer-events: none;
      mix-blend-mode: screen;
    }

    .orb.orb-1 {
      width: 260px;
      height: 260px;
      background: radial-gradient(circle, rgba(79, 70, 229, 0.9), transparent 60%);
      top: -80px;
      left: -40px;
    }

    .orb.orb-2 {
      width: 220px;
      height: 220px;
      background: radial-gradient(circle, rgba(14, 165, 233, 0.9), transparent 60%);
      bottom: -60px;
      right: 40px;
    }

    .sidebar {
      position: relative;
      z-index: 1;
      border-right: 1px solid rgba(31, 41, 55, 0.9);
      background: radial-gradient(circle at top left, #020617 0, #020617 40%, #020617 100%);
      padding: 18px 16px 16px;
      display: flex;
      flex-direction: column;
      gap: 18px;
    }

    .brand {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 10px;
      margin-bottom: 4px;
    }

    .brand-left {
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .brand-logo {
      width: 34px;
      height: 34px;
      border-radius: 14px;
      background: conic-gradient(from 210deg, #4f46e5, #22d3ee, #a855f7, #4f46e5);
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: var(--shadow-glow);
      position: relative;
      overflow: hidden;
    }

    .brand-logo-inner {
      width: 26px;
      height: 26px;
      border-radius: 11px;
      background: radial-gradient(circle at 30% 0, #1f2937, #020617 70%);
      border: 1px solid rgba(148, 163, 184, 0.4);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--accent-strong);
      font-size: 14px;
      font-weight: 700;
      letter-spacing: 0.04em;
    }

    .brand-text {
      display: flex;
      flex-direction: column;
      gap: 2px;
    }

    .brand-name {
      font-size: 17px;
      font-weight: 600;
      letter-spacing: 0.03em;
      display: flex;
      align-items: baseline;
      gap: 4px;
    }

    .brand-name span.highlight {
      background: linear-gradient(120deg, #a5b4fc, #38bdf8, #f97316);
      -webkit-background-clip: text;
      color: transparent;
    }

    .brand-tagline {
      font-size: 11px;
      color: var(--text-muted);
    }

    .brand-pill {
      padding: 4px 10px;
      border-radius: 999px;
      border: 1px solid rgba(148, 163, 184, 0.4);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.9), rgba(15, 23, 42, 0.4));
      font-size: 11px;
      color: var(--accent-strong);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      white-space: nowrap;
    }

    .brand-pill-dot {
      width: 7px;
      height: 7px;
      border-radius: 999px;
      background: radial-gradient(circle, #22c55e, #16a34a);
      box-shadow: 0 0 10px rgba(34, 197, 94, 0.9);
    }

    .sidebar-section-title {
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: #6b7280;
      margin-bottom: 6px;
    }

    .new-chat-btn {
      width: 100%;
      border-radius: var(--radius-md);
      border: 1px solid rgba(79, 70, 229, 0.7);
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.3), rgba(15, 23, 42, 0.9));
      color: var(--text-main);
      padding: 10px 12px;
      font-size: 13px;
      font-weight: 500;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      cursor: pointer;
      transition: background var(--transition-fast), transform var(--transition-fast),
        box-shadow var(--transition-fast), border-color var(--transition-fast);
      box-shadow: 0 12px 30px rgba(79, 70, 229, 0.35);
    }

    .new-chat-btn span.icon {
      width: 20px;
      height: 20px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 14px;
      color: var(--accent-strong);
    }

    .new-chat-btn:hover {
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.45), rgba(15, 23, 42, 0.9));
      transform: translateY(-1px);
      box-shadow: 0 16px 40px rgba(79, 70, 229, 0.55);
      border-color: rgba(129, 140, 248, 0.9);
    }

    .new-chat-btn:active {
      transform: translateY(0);
      box-shadow: 0 8px 20px rgba(79, 70, 229, 0.4);
    }

    .sidebar-card {
      border-radius: var(--radius-md);
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.9));
      padding: 10px 10px 10px;
      display: flex;
      flex-direction: column;
      gap: 8px;
    }

    .sidebar-card-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
    }

    .sidebar-card-title {
      font-size: 12px;
      font-weight: 500;
      color: #e5e7eb;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .sidebar-card-title-pill {
      font-size: 10px;
      padding: 2px 8px;
      border-radius: 999px;
      background: rgba(55, 65, 81, 0.7);
      color: #e5e7eb;
    }

    .sidebar-card-link {
      font-size: 11px;
      color: var(--accent-strong);
      cursor: pointer;
      opacity: 0.9;
    }

    .sidebar-card-link:hover {
      text-decoration: underline;
    }

    .sidebar-list {
      display: flex;
      flex-direction: column;
      gap: 4px;
      margin-top: 2px;
    }

    .sidebar-item {
      border-radius: 10px;
      padding: 7px 8px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
      cursor: pointer;
      transition: background var(--transition-fast), transform var(--transition-fast),
        border-color var(--transition-fast);
      border: 1px solid transparent;
    }

    .sidebar-item:hover {
      background: rgba(15, 23, 42, 0.9);
      border-color: rgba(55, 65, 81, 0.9);
      transform: translateY(-0.5px);
    }

    .sidebar-item-main {
      display: flex;
      align-items: center;
      gap: 8px;
      min-width: 0;
    }

    .sidebar-item-icon {
      width: 22px;
      height: 22px;
      border-radius: 999px;
      background: rgba(31, 41, 55, 0.9);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 13px;
      color: var(--accent-strong);
    }

    .sidebar-item-text {
      display: flex;
      flex-direction: column;
      gap: 1px;
      min-width: 0;
    }

    .sidebar-item-title {
      font-size: 12px;
      color: #e5e7eb;
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
    }

    .sidebar-item-subtitle {
      font-size: 11px;
      color: var(--text-muted);
      white-space: nowrap;
      text-overflow: ellipsis;
      overflow: hidden;
    }

    .sidebar-item-badge {
      font-size: 10px;
      padding: 2px 7px;
      border-radius: 999px;
      background: rgba(31, 41, 55, 0.9);
      color: #9ca3af;
      white-space: nowrap;
    }

    .sidebar-footer {
      margin-top: auto;
      display: flex;
      flex-direction: column;
      gap: 10px;
      font-size: 11px;
      color: var(--text-muted);
    }

    .sidebar-footer-top {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
    }

    .sidebar-footer-pill {
      padding: 4px 8px;
      border-radius: 999px;
      border: 1px solid rgba(55, 65, 81, 0.9);
      background: rgba(15, 23, 42, 0.9);
      display: inline-flex;
      align-items: center;
      gap: 6px;
      color: #e5e7eb;
    }

    .sidebar-footer-pill span.key {
      padding: 2px 6px;
      border-radius: 6px;
      background: rgba(31, 41, 55, 0.9);
      font-size: 10px;
      color: #9ca3af;
    }

    .sidebar-footer-links {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;
      font-size: 11px;
    }

    .sidebar-footer-links a {
      color: var(--text-muted);
      text-decoration: none;
      opacity: 0.9;
    }

    .sidebar-footer-links a:hover {
      color: var(--accent-strong);
    }

    .sidebar-footer-usage {
      font-size: 10px;
      color: #6b7280;
    }

    .sidebar-footer-usage span {
      color: var(--accent-strong);
    }

    /* Main chat area */

    .main {
      position: relative;
      z-index: 1;
      display: flex;
      flex-direction: column;
      padding: 18px 18px 16px;
      gap: 12px;
    }

    .main-header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
    }

    .main-header-left {
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .main-title-row {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .main-title {
      font-size: 18px;
      font-weight: 600;
      letter-spacing: 0.02em;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .main-title-gradient {
      background: linear-gradient(120deg, #e5e7eb, #a5b4fc, #38bdf8);
      -webkit-background-clip: text;
      color: transparent;
    }

    .main-title-chip {
      font-size: 11px;
      padding: 3px 8px;
      border-radius: 999px;
      background: rgba(31, 41, 55, 0.9);
      color: #9ca3af;
      border: 1px solid rgba(55, 65, 81, 0.9);
    }

    .main-subtitle {
      font-size: 12px;
      color: var(--text-muted);
    }

    .main-header-right {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .pill-toggle {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      padding: 4px;
      border-radius: 999px;
      background: rgba(15, 23, 42, 0.9);
      border: 1px solid rgba(31, 41, 55, 0.9);
      font-size: 11px;
      color: #9ca3af;
    }

    .pill-toggle span {
      padding: 3px 8px;
      border-radius: 999px;
      cursor: pointer;
      transition: background var(--transition-fast), color var(--transition-fast);
    }

    .pill-toggle span.active {
      background: rgba(79, 70, 229, 0.9);
      color: #e5e7eb;
    }

    .avatar {
      width: 28px;
      height: 28px;
      border-radius: 999px;
      background: radial-gradient(circle at 30% 0, #1f2937, #020617 70%);
      border: 1px solid rgba(55, 65, 81, 0.9);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 13px;
      color: #e5e7eb;
    }

    .chat-wrapper {
      flex: 1;
      border-radius: var(--radius-lg);
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.96));
      padding: 12px 12px 10px;
      display: flex;
      flex-direction: column;
      gap: 10px;
      overflow: hidden;
      position: relative;
    }

    .chat-wrapper::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top, rgba(79, 70, 229, 0.18), transparent 55%);
      opacity: 0.7;
      pointer-events: none;
    }

    .chat-inner {
      position: relative;
      z-index: 1;
      display: flex;
      flex-direction: column;
      gap: 10px;
      height: 100%;
      overflow: hidden;
    }

    .chat-suggestions {
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
      gap: 8px;
      margin-bottom: 4px;
    }

    .suggestion-card {
      border-radius: 12px;
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.9));
      padding: 8px 9px;
      font-size: 11px;
      color: #e5e7eb;
      display: flex;
      flex-direction: column;
      gap: 4px;
      cursor: pointer;
      transition: border-color var(--transition-fast), background var(--transition-fast),
        transform var(--transition-fast), box-shadow var(--transition-fast);
    }

    .suggestion-card:hover {
      border-color: rgba(79, 70, 229, 0.9);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.96));
      transform: translateY(-1px);
      box-shadow: 0 12px 30px rgba(15, 23, 42, 0.9);
    }

    .suggestion-label {
      font-size: 10px;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: #9ca3af;
    }

    .suggestion-title {
      font-size: 11px;
      font-weight: 500;
    }

    .suggestion-meta {
      font-size: 10px;
      color: #6b7280;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 4px;
    }

    .suggestion-meta span {
      display: inline-flex;
      align-items: center;
      gap: 4px;
    }

    .suggestion-dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: rgba(79, 70, 229, 0.9);
    }

    .chat-stream {
      flex: 1;
      border-radius: 14px;
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.96));
      padding: 10px 10px 8px;
      overflow-y: auto;
      display: flex;
      flex-direction: column;
      gap: 10px;
      scroll-behavior: smooth;
    }

    .chat-stream::-webkit-scrollbar {
      width: 6px;
    }

    .chat-stream::-webkit-scrollbar-track {
      background: transparent;
    }

    .chat-stream::-webkit-scrollbar-thumb {
      background: rgba(31, 41, 55, 0.9);
      border-radius: 999px;
    }

    .message {
      display: flex;
      align-items: flex-start;
      gap: 8px;
      font-size: 13px;
      line-height: 1.5;
    }

    .message-avatar {
      width: 24px;
      height: 24px;
      border-radius: 999px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 12px;
      flex-shrink: 0;
    }

    .message-avatar.user {
      background: radial-gradient(circle at 30% 0, #1f2937, #020617 70%);
      border: 1px solid rgba(55, 65, 81, 0.9);
      color: #e5e7eb;
    }

    .message-avatar.ai {
      background: radial-gradient(circle at 30% 0, #4f46e5, #22d3ee 70%);
      border: 1px solid rgba(129, 140, 248, 0.9);
      color: #020617;
    }

    .message-body {
      max-width: 100%;
      display: flex;
      flex-direction: column;
      gap: 4px;
    }

    .message-meta {
      font-size: 11px;
      color: #6b7280;
      display: flex;
      align-items: center;
      gap: 6px;
    }

    .message-meta span.role {
      text-transform: uppercase;
      letter-spacing: 0.14em;
      font-size: 10px;
      color: #9ca3af;
    }

    .message-bubble {
      border-radius: 12px;
      padding: 8px 10px;
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: rgba(15, 23, 42, 0.96);
      color: #e5e7eb;
    }

    .message.user .message-bubble {
      background: rgba(15, 23, 42, 0.96);
    }

    .message.ai .message-bubble {
      background: radial-gradient(circle at top left, rgba(79, 70, 229, 0.35), rgba(15, 23, 42, 0.96));
      border-color: rgba(79, 70, 229, 0.9);
      box-shadow: 0 10px 30px rgba(15, 23, 42, 0.9);
    }

    .message-actions {
      display: flex;
      align-items: center;
      gap: 6px;
      font-size: 11px;
      color: #6b7280;
    }

    .message-actions button {
      border: none;
      background: transparent;
      color: inherit;
      font-size: 11px;
      cursor: pointer;
      padding: 0;
      display: inline-flex;
      align-items: center;
      gap: 4px;
      opacity: 0.9;
    }

    .message-actions button:hover {
      color: var(--accent-strong);
    }

    .typing-indicator {
      display: inline-flex;
      align-items: center;
      gap: 4px;
      font-size: 11px;
      color: #9ca3af;
    }

    .typing-dot {
      width: 4px;
      height: 4px;
      border-radius: 999px;
      background: #9ca3af;
      animation: bounce 1s infinite ease-in-out;
    }

    .typing-dot:nth-child(2) {
      animation-delay: 0.15s;
    }

    .typing-dot:nth-child(3) {
      animation-delay: 0.3s;
    }

    @keyframes bounce {
      0%,
      80%,
      100% {
        transform: translateY(0);
        opacity: 0.4;
      }
      40% {
        transform: translateY(-3px);
        opacity: 1;
      }
    }

    .chat-input-area {
      position: relative;
      z-index: 1;
      margin-top: 4px;
      display: flex;
      flex-direction: column;
      gap: 6px;
    }

    .input-row {
      display: flex;
      align-items: flex-end;
      gap: 8px;
    }

    .input-shell {
      flex: 1;
      border-radius: 999px;
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: radial-gradient(circle at top, rgba(15, 23, 42, 0.96), rgba(15, 23, 42, 0.96));
      padding: 6px 10px 6px 12px;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .input-prefix {
      font-size: 11px;
      color: #6b7280;
      padding-right: 6px;
      border-right: 1px solid rgba(31, 41, 55, 0.9);
      display: flex;
      align-items: center;
      gap: 4px;
    }

    .input-prefix span.dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: rgba(79, 70, 229, 0.9);
    }

    .input-field {
      flex: 1;
      border: none;
      outline: none;
      background: transparent;
      color: #e5e7eb;
      font-size: 13px;
      padding: 6px 0;
      resize: none;
      max-height: 80px;
      line-height: 1.4;
    }

    .input-field::placeholder {
      color: #6b7280;
    }

    .input-tools {
      display: flex;
      align-items: center;
      gap: 6px;
      margin-left: 4px;
    }

    .input-tool-btn {
      width: 26px;
      height: 26px;
      border-radius: 999px;
      border: 1px solid rgba(31, 41, 55, 0.9);
      background: rgba(15, 23, 42, 0.96);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 13px;
      color: #9ca3af;
      cursor: pointer;
      transition: background var(--transition-fast), border-color var(--transition-fast),
        color var(--transition-fast), transform var(--transition-fast);
    }

    .input-tool-btn:hover {
      background: rgba(31, 41, 55, 0.9);
      border-color: rgba(55, 65, 81, 0.9);
      color: #e5e7eb;
      transform: translateY(-0.5px);
    }

    .send-btn {
      width: 34px;
      height: 34px;
      border-radius: 999px;
      border: none;
      background: radial-gradient(circle at top left, #4f46e5, #22d3ee);
      color: #f9fafb;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 16px;
      cursor: pointer;
      box-shadow: 0 14px 32px rgba(37, 99, 235, 0.7);
      transition: transform var(--transition-fast), box-shadow var(--transition-fast),
        filter var(--transition-fast);
      flex-shrink: 0;
    }

    .send-btn:hover {
      transform: translateY(-1px);
      box-shadow: 0 18px 40px rgba(37, 99, 235, 0.9);
      filter: brightness(1.05);
    }

    .send-btn:active {
      transform: translateY(0);
      box-shadow: 0 10px 24px rgba(37, 99, 235, 0.7);
    }

    .input-meta-row {
      display: flex;
      align-items: center;
      justify-content: space-between;
      font-size: 10px;
      color: #6b7280;
      padding: 0 4px;
    }

    .input-meta-left {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .input-meta-left span.key-hint {
      padding: 2px 6px;
      border-radius: 6px;
      background: rgba(15, 23, 42, 0.96);
      border: 1px solid rgba(31, 41, 55, 0.9);
      color: #9ca3af;
      display: inline-flex;
      align-items: center;
      gap: 4px;
    }

    .input-meta-right {
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .input-meta-right span {
      display: inline-flex;
      align-items: center;
      gap: 4px;
    }

    .input-meta-right span.dot {
      width: 6px;
      height: 6px;
      border-radius: 999px;
      background: rgba(79, 70, 229, 0.9);
    }

    .input-meta-right span.warn {
      color: var(--danger);
    }

    /* Responsive */

    @media (max-width: 960px) {
      body {
        padding: 10px;
      }

      .app-shell {
        grid-template-columns: minmax(0, 1fr);
        max-height: none;
      }

      .sidebar {
        display: none;
      }
    }

    @media (max-width: 720px) {
      .chat-suggestions {
        grid-template-columns: repeat(2, minmax(0, 1fr));
      }

      .main-header {
        flex-direction: column;
        align-items: flex-start;
      }

      .main-header-right {
        align-self: stretch;
        justify-content: space-between;
      }
    }

    @media (max-width: 480px) {
      body {
        padding: 6px;
      }

      .chat-suggestions {
        display: none;
      }

      .chat-wrapper {
        padding: 10px 10px 8px;
      }

      .input-shell {
        border-radius: 16px;
      }

      .input-row {
        align-items: center;
      }
    }
  </style>
</head>
<body>
  <div class="app-shell">
    <div class="orb orb-1"></div>
    <div class="orb orb-2"></div>

    <!-- Sidebar -->
    <aside class="sidebar">
      <header class="brand">
        <div class="brand-left">
          <div class="brand-logo">
            <div class="brand-logo-inner">CI</div>
          </div>
          <div class="brand-text">
            <div class="brand-name">
              chat<span class="highlight">idea</span>
            </div>
            <div class="brand-tagline">Where your ideas meet AI.</div>
          </div>
        </div>
        <div class="brand-pill">
          <span class="brand-pill-dot"></span>
          Live · v1.0
        </div>
      </header>

      <button class="new-chat-btn">
        <span class="icon">+</span>
        <span>New chat</span>
      </button>

      <section>
        <div class="sidebar-section-title">Recent</div>
        <div class="sidebar-card">
          <div class="sidebar-card-header">
            <div class="sidebar-card-title">
              Conversations
              <span class="sidebar-card-title-pill">Today</span>
            </div>
            <div class="sidebar-card-link">View all</div>
          </div>
          <div class="sidebar-list">
            <div class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-item-icon">💡</div>
                <div class="sidebar-item-text">
                  <div class="sidebar-item-title">Brainstorm startup ideas</div>
                  <div class="sidebar-item-subtitle">AI + productivity tools</div>
                </div>
              </div>
              <div class="sidebar-item-badge">12:04</div>
            </div>
            <div class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-item-icon">✍️</div>
                <div class="sidebar-item-text">
                  <div class="sidebar-item-title">Rewrite landing page copy</div>
                  <div class="sidebar-item-subtitle">More friendly, less formal</div>
                </div>
              </div>
              <div class="sidebar-item-badge">11:32</div>
            </div>
            <div class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-item-icon">📊</div>
                <div class="sidebar-item-text">
                  <div class="sidebar-item-title">Summarize research article</div>
                  <div class="sidebar-item-subtitle">Key insights in 5 bullets</div>
                </div>
              </div>
              <div class="sidebar-item-badge">09:18</div>
            </div>
          </div>
        </div>
      </section>

      <section>
        <div class="sidebar-section-title">Modes</div>
        <div class="sidebar-card">
          <div class="sidebar-list">
            <div class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-item-icon">⚡</div>
                <div class="sidebar-item-text">
                  <div class="sidebar-item-title">Quick ideas</div>
                  <div class="sidebar-item-subtitle">Fast, lightweight responses</div>
                </div>
              </div>
              <div class="sidebar-item-badge">Default</div>
            </div>
            <div class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-item-icon">🧠</div>
                <div class="sidebar-item-text">
                  <div class="sidebar-item-title">Deep dive</div>
                  <div class="sidebar-item-subtitle">More context & reasoning</div>
                </div>
              </div>
              <div class="sidebar-item-badge">Beta</div>
            </div>
            <div class="sidebar-item">
              <div class="sidebar-item-main">
                <div class="sidebar-item-icon">🎨</div>
                <div class="sidebar-item-text">
                  <div class="sidebar-item-title">Creative studio</div>
                  <div class="sidebar-item-subtitle">Stories, scripts & visuals</div>
                </div>
              </div>
              <div class="sidebar-item-badge">New</div>
            </div>
          </div>
        </div>
      </section>

      <footer class="sidebar-footer">
        <div class="sidebar-footer-top">
          <div class="sidebar-footer-pill">
            <span>Shortcuts</span>
            <span class="key">⌘</span>
            <span class="key">/</span>
          </div>
          <div class="sidebar-footer-usage">
            Usage: <span>Light</span>
          </div>
        </div>
        <div class="sidebar-footer-links">
          <a href="#">Docs</a>
          <a href="#">Changelog</a>
          <a href="#">Settings</a>
        </div>
      </footer>
    </aside>

    <!-- Main -->
    <main class="main">
      <header class="main-header">
        <div class="main-header-left">
          <div class="main-title-row">
            <div class="main-title">
              <span class="main-title-gradient">Chat Idea</span>
              <span class="main-title-chip">AI chat workspace</span>
            </div>
          </div>
          <div class="main-subtitle">
            Start typing to explore ideas, draft content, or ask anything—your AI collaborator is ready.
          </div>
        </div>
        <div class="main-header-right">
          <div class="pill-toggle">
            <span class="active">Balanced</span>
            <span>Creative</span>
          </div>
          <div class="avatar">You</div>
        </div>
      </header>

      <section class="chat-wrapper">
        <div class="chat-inner">
          <div class="chat-suggestions">
            <div class="suggestion-card">
              <div class="suggestion-label">Brainstorm</div>
              <div class="suggestion-title">“Give me 5 startup ideas using AI in education.”</div>
              <div class="suggestion-meta">
                <span><span class="suggestion-dot"></span> 12 sec</span>
                <span>Idea mode</span>
              </div>
            </div>
            <div class="suggestion-card">
              <div class="suggestion-label">Rewrite</div>
              <div class="suggestion-title">“Rewrite this paragraph to sound more confident.”</div>
              <div class="suggestion-meta">
                <span><span class="suggestion-dot"></span> 8 sec</span>
                <span>Copy polish</span>
              </div>
            </div>
            <div class="suggestion-card">
              <div class="suggestion-label">Summarize</div>
              <div class="suggestion-title">“Summarize this article in 5 bullet points.”</div>
              <div class="suggestion-meta">
                <span><span class="suggestion-dot"></span> 10 sec</span>
                <span>Research</span>
              </div>
            </div>
            <div class="suggestion-card">
              <div class="suggestion-label">Plan</div>
              <div class="suggestion-title">“Help me plan a 30-day learning roadmap.”</div>
              <div class="suggestion-meta">
                <span><span class="suggestion-dot"></span> 15 sec</span>
                <span>Structured</span>
              </div>
            </div>
          </div>

          <div class="chat-stream">
            <div class="message ai">
              <div class="message-avatar ai">AI</div>
              <div class="message-body">
                <div class="message-meta">
                  <span class="role">Assistant</span>
                  <span>·</span>
                  <span>Just now</span>
                </div>
                <div class="message-bubble">
                  Hey, welcome to <strong>Chat Idea</strong>—your space to explore, refine, and ship ideas faster.
                  <br /><br />
                  You can:
                  <ul style="margin-top: 6px; padding-left: 18px;">
                    <li>Brainstorm product, startup, or content ideas.</li>
                    <li>Rewrite and polish emails, posts, and landing pages.</li>
                    <li>Summarize long articles, notes, or transcripts.</li>
                    <li>Plan projects, learning paths, or creative workflows.</li>
                  </ul>
                  <br />
                  What are you working on tonight?
                </div>
                <div class="message-actions">
                  <button title="Like this response">👍 Helpful</button>
                  <button title="Dislike this response">👎 Not quite</button>
                  <button title="Copy response">📋 Copy</button>
                </div>
              </div>
            </div>

            <div class="message user">
              <div class="message-avatar user">U</div>
              <div class="message-body">
                <div class="message-meta">
                  <span class="role">You</span>
                  <span>·</span>
                  <span>Draft</span>
                </div>
                <div class="message-bubble">
                  Help me come up with a unique concept for a modern AI chat website called “Chat Idea”.
                </div>
              </div>
            </div>

            <div class="message ai">
              <div class="message-avatar ai">AI</div>
              <div class="message-body">
                <div class="message-meta">
                  <span class="role">Assistant</span>
                  <span>·</span>
                  <span>Thinking</span>
                </div>
                <div class="message-bubble">
                  <span class="typing-indicator">
                    <span class="typing-dot"></span>
                    <span class="typing-dot"></span>
                    <span class="typing-dot"></span>
                    Thinking through some concepts…
                  </span>
                </div>
              </div>
            </div>
          </div>

          <div class="chat-input-area">
            <div class="input-row">
              <div class="input-shell">
                <div class="input-prefix">
                  <span class="dot"></span>
                  <span>Prompt</span>
                </div>
                <textarea
                  class="input-field"
                  rows="1"
                  placeholder="Ask anything, or describe what you want to create…"
                ></textarea>
                <div class="input-tools">
                  <button class="input-tool-btn" title="Attach file">📎</button>
                  <button class="input-tool-btn" title="Insert template">⌘</button>
                </div>
              </div>
              <button class="send-btn" title="Send message">➤</button>
            </div>
            <div class="input-meta-row">
              <div class="input-meta-left">
                <span class="key-hint">
                  <span>Press</span>
                  <span>Enter</span>
                  <span>to send · Shift+Enter for new line</span>
                </span>
              </div>
              <div class="input-meta-right">
                <span><span class="dot"></span> Balanced mode</span>
                <span class="warn">Experimental · Don’t share sensitive data</span>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</body>
</html>
