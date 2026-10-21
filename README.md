<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>VeloPay Admin</title>
  <style>
    :root {
      --bg: #f4f7ff;
      --panel: rgba(255,255,255,0.82);
      --panel-strong: #ffffff;
      --ink: #171f2d;
      --muted: #66758a;
      --line: #e8edf5;
      --primary: #5f6fff;
      --primary-2: #2cc7a2;
      --orange: #ff9f43;
      --pink: #ff5db1;
      --red: #ef5a52;
      --navy: #101d34;
      --shadow: 0 22px 50px rgba(30, 39, 60, 0.12);
      --radius-xl: 28px;
      --radius-lg: 20px;
      --radius-md: 16px;
    }

    * { box-sizing: border-box; }

    html, body {
      margin: 0;
      min-height: 100%;
      font-family: Inter, "Segoe UI", sans-serif;
      background: linear-gradient(180deg, var(--bg) 0%, #f9fbff 100%);
      color: var(--ink);
    }

    body {
      padding: 22px 14px;
    }

    .app {
      max-width: 1280px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: 240px minmax(0, 1fr);
      gap: 22px;
    }

    .sidebar {
      background: rgba(16,29,52,0.98);
      color: white;
      border-radius: 28px;
      padding: 22px 18px;
      box-shadow: var(--shadow);
      min-height: 820px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 800;
      margin-bottom: 28px;
      letter-spacing: 0.04em;
    }

    .brand-mark {
      width: 38px;
      height: 38px;
      border-radius: 12px;
      background: linear-gradient(135deg, #7a8cff, var(--primary));
      position: relative;
    }

    .brand-mark::before {
      content: "";
      position: absolute;
      inset: 10px;
      border-radius: 50%;
      background: rgba(255,255,255,0.94);
      transform: rotate(45deg);
    }

    .nav {
      display: flex;
      flex-direction: column;
      gap: 8px;
      margin-top: 18px;
    }

    .nav-item {
      display: flex;
      align-items: center;
      gap: 12px;
      padding: 12px 12px;
      border-radius: 14px;
      color: rgba(255,255,255,0.72);
      font-weight: 600;
      background: transparent;
      border: none;
      text-align: left;
      cursor: pointer;
      transition: 0.2s ease;
    }

    .nav-item.active {
      background: rgba(255,255,255,0.08);
      color: white;
      box-shadow: inset 0 0 0 1px rgba(255,255,255,0.04);
    }

    .nav-item .dot {
      width: 10px;
      height: 10px;
      border-radius: 50%;
      background: rgba(255,255,255,0.8);
      display: inline-block;
    }

    .admin-card {
      background: linear-gradient(135deg, rgba(95,111,255,0.24), rgba(44,199,162,0.18));
      border: 1px solid rgba(255,255,255,0.1);
      border-radius: 18px;
      padding: 14px;
      margin-top: 30px;
    }

    .admin-card .label {
      font-size: 11px;
      color: rgba(255,255,255,0.78);
      margin-bottom: 10px;
    }

    .admin-user {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 14px;
    }

    .avatar {
      width: 42px;
      height: 42px;
      border-radius: 12px;
      display: grid;
      place-items: center;
      background: linear-gradient(135deg, #8d9bff, #5f6fff);
      font-weight: 700;
    }

    .admin-email {
      font-size: 12px;
      color: rgba(255,255,255,0.8);
      word-break: break-all;
    }

    .admin-btn {
      width: 100%;
      border: none;
      border-radius: 12px;
      background: white;
      color: var(--navy);
      padding: 11px 12px;
      font-weight: 800;
      cursor: pointer;
    }

    .main {
      display: grid;
      gap: 22px;
    }

    .topbar {
      background: rgba(255,255,255,0.7);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255,255,255,0.7);
      border-radius: 24px;
      padding: 16px 18px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      box-shadow: var(--shadow);
    }

    .title-block h1 {
      margin: 0;
      font-size: clamp(1.5rem, 2vw, 2.2rem);
      letter-spacing: -0.05em;
    }

    .sub {
      margin-top: 4px;
      color: var(--mut*

