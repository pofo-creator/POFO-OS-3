<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>POFO OS ???</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            user-select: none;
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
        }

        body {
            background: radial-gradient(circle at 20% 30%, #1a1e2c, #0b0d14);
            height: 100vh;
            width: 100vw;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 0;
            margin: 0;
            overflow: hidden;
        }

        .screen {
            width: 100vw;
            height: 100vh;
            padding: 20px 18px 16px;
            display: flex;
            flex-direction: column;
            transition: background 0.4s, color 0.4s;
            overflow: hidden;
            position: relative;
            background: radial-gradient(circle at 30% 40%, #1a1e2c, #0b0d14);
            background-size: cover;
            background-position: center;
        }

        .screen.light-theme {
            background: rgba(240, 242, 255, 0.92) !important;
            color: #1a202c;
        }
        .screen.light-theme .status-bar { color: rgba(30, 40, 80, 0.7); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .logo-text { background: linear-gradient(to right, #7c3aed, #ec4899); -webkit-background-clip: text; -webkit-text-fill-color: transparent; }
        .screen.light-theme .spiral-clock { color: #4a5568; background: rgba(255,255,255,0.5); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .app-name { color: rgba(30, 40, 80, 0.7); }
        .screen.light-theme .gesture-pill { color: rgba(30, 40, 80, 0.5); background: rgba(255,255,255,0.3); }
        .screen.light-theme .nav-item { color: rgba(30, 40, 80, 0.35); }
        .screen.light-theme .nav-item.active { color: #7c3aed; background: rgba(124, 58, 237, 0.08); }
        .screen.light-theme .back-tap-hint { color: rgba(30, 40, 80, 0.15); }
        .screen.light-theme .app-window { background: rgba(240, 242, 255, 0.96); }
        .screen.light-theme .app-window-title { color: #1a202c; }
        .screen.light-theme .app-window-header { border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .settings-item { background: rgba(255,255,255,0.3); border-color: rgba(0,0,0,0.03); }
        .screen.light-theme .settings-item:hover { background: rgba(255,255,255,0.5); }
        .screen.light-theme .settings-item-title { color: #1a202c; }
        .screen.light-theme .settings-item-desc { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .settings-detail-item { background: rgba(255,255,255,0.3); border-color: rgba(0,0,0,0.03); }
        .screen.light-theme .settings-detail-item .label { color: rgba(30, 40, 80, 0.7); }
        .screen.light-theme .settings-detail-item .value { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .settings-detail-header { border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .settings-detail-title { color: #1a202c; }
        .screen.light-theme .settings-detail-back { color: rgba(30, 40, 80, 0.5); }
        .screen.light-theme .settings-item-arrow { color: rgba(30, 40, 80, 0.2); }
        .screen.light-theme .settings-detail-item .toggle.off { color: rgba(30, 40, 80, 0.15); }
        .screen.light-theme .note-item { background: rgba(255,255,255,0.5); border-color: rgba(0,0,0,0.03); }
        .screen.light-theme .note-item .note-title { color: #1a202c; }
        .screen.light-theme .note-item .note-preview { color: rgba(30, 40, 80, 0.5); }
        .screen.light-theme .note-item .note-date { color: rgba(30, 40, 80, 0.3); }
        .screen.light-theme .note-viewer { background: rgba(255,255,255,0.95); }
        .screen.light-theme .note-viewer textarea { background: rgba(255,255,255,0.5); color: #1a202c; border-color: rgba(0,0,0,0.1); }
        .screen.light-theme .note-viewer .note-viewer-title { color: #1a202c; }
        .screen.light-theme .create-note-modal { background: rgba(240, 242, 255, 0.98); }
        .screen.light-theme .create-note-modal input { background: rgba(255,255,255,0.6); color: #1a202c; border-color: rgba(0,0,0,0.1); }
        .screen.light-theme .create-note-modal .modal-title { color: #1a202c; }
        .screen.light-theme .create-note-modal .modal-label { color: rgba(30, 40, 80, 0.6); }
        .screen.light-theme .gallery-item { background: rgba(255,255,255,0.5); border-color: rgba(0,0,0,0.03); }
        .screen.light-theme .gallery-item .gallery-name { color: #1a202c; }
        .screen.light-theme .gallery-item .gallery-count { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .photo-grid .photo-item { background: rgba(255,255,255,0.5); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .editor-toolbar { background: rgba(255,255,255,0.3); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .editor-toolbar button { color: rgba(30, 40, 80, 0.7); }
        .screen.light-theme .editor-toolbar button:hover { background: rgba(0,0,0,0.05); }
        .screen.light-theme .modal-content { background: rgba(240, 242, 255, 0.98); }
        .screen.light-theme .modal-title { color: #1a202c; }
        .screen.light-theme .modal-label { color: rgba(30, 40, 80, 0.6); }
        .screen.light-theme .modal-input { background: rgba(255,255,255,0.6); color: #1a202c; border-color: rgba(0,0,0,0.1); }
        .screen.light-theme .filter-chip { background: rgba(255,255,255,0.3); color: rgba(30, 40, 80, 0.6); }
        .screen.light-theme .filter-chip.active { background: rgba(124, 58, 237, 0.15); color: #7c3aed; }
        .screen.light-theme .editor-controls label { color: rgba(30, 40, 80, 0.6); }
        .screen.light-theme .editor-controls input[type="range"] { background: rgba(0,0,0,0.1); }
        .screen.light-theme .editor-controls input[type="range"]::-webkit-slider-thumb { background: #7c3aed; }
        .screen.light-theme .layers-list { background: rgba(255,255,255,0.3); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .layer-item { background: rgba(255,255,255,0.5); border-color: rgba(0,0,0,0.03); color: #1a202c; }
        .screen.light-theme .layer-item .layer-name { color: #1a202c; }
        .screen.light-theme .layer-item .layer-delete { color: rgba(30, 40, 80, 0.3); }
        .screen.light-theme .layer-item .layer-delete:hover { color: #ef4444; }
        .screen.light-theme .music-item { background: rgba(255,255,255,0.3); border-color: rgba(0,0,0,0.03); color: #1a202c; }
        .screen.light-theme .music-item .music-name { color: #1a202c; }
        .screen.light-theme .music-item .music-size { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .store-app { background: rgba(255,255,255,0.5); border-color: rgba(0,0,0,0.03); }
        .screen.light-theme .store-app .store-app-name { color: #1a202c; }
        .screen.light-theme .store-app .store-app-desc { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .wallpaper-option { background: rgba(255,255,255,0.3); border-color: rgba(0,0,0,0.03); }
        .screen.light-theme .wallpaper-option .wallpaper-name { color: #1a202c; }
        .screen.light-theme .root-status { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .account-menu { background: rgba(240, 242, 255, 0.98); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .account-menu .account-title { color: #1a202c; }
        .screen.light-theme .account-menu .account-input { background: rgba(255,255,255,0.6); color: #1a202c; border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .account-menu .account-status { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .account-menu .user-item { color: rgba(30, 40, 80, 0.5); }
        .screen.light-theme .account-menu .account-search { background: rgba(255,255,255,0.4); color: rgba(30, 40, 80, 0.5); border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .account-menu .account-close { color: rgba(30, 40, 80, 0.2); }
        .screen.light-theme .app-lock-overlay { background: rgba(240, 242, 255, 0.95); }
        .screen.light-theme .app-lock-overlay .lock-title { color: #1a202c; }
        .screen.light-theme .app-lock-overlay .lock-sub { color: rgba(30, 40, 80, 0.3); }
        .screen.light-theme .app-lock-overlay .lock-input { background: rgba(255,255,255,0.6); color: #1a202c; border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .app-lock-overlay .lock-key { background: rgba(255,255,255,0.3); color: #1a202c; border-color: rgba(0,0,0,0.05); }
        .screen.light-theme .app-lock-overlay .lock-key:hover { background: rgba(255,255,255,0.5); }
        .screen.light-theme .app-pages .page-dot { background: rgba(30, 40, 80, 0.15); }
        .screen.light-theme .app-pages .page-dot.active { background: #7c3aed; }
        .screen.light-theme .media-viewer { background: rgba(240, 242, 255, 0.95); }
        .screen.light-theme .media-viewer .media-viewer-close { color: rgba(30, 40, 80, 0.4); }
        .screen.light-theme .media-viewer .media-viewer-close:hover { color: rgba(30, 40, 80, 0.8); }
        .screen.light-theme .media-viewer .media-viewer-info { color: rgba(30, 40, 80, 0.3); }

        .screen.text-color-red .logo-text, .screen.text-color-red .app-name, .screen.text-color-red .app-window-title,
        .screen.text-color-red .settings-item-title, .screen.text-color-red .settings-detail-title,
        .screen.text-color-red .settings-detail-item .label, .screen.text-color-red .note-item .note-title,
        .screen.text-color-red .note-viewer .note-viewer-title, .screen.text-color-red .gallery-item .gallery-name,
        .screen.text-color-red .modal-title, .screen.text-color-red .editor-toolbar button,
        .screen.text-color-red .layer-item .layer-name, .screen.text-color-red .music-item .music-name,
        .screen.text-color-red .store-app .store-app-name, .screen.text-color-red .wallpaper-option .wallpaper-name,
        .screen.text-color-red .root-status, .screen.text-color-red .account-menu .account-title,
        .screen.text-color-red .account-menu .account-status { color: #ef4444 !important; }
        .screen.text-color-blue .logo-text, .screen.text-color-blue .app-name, .screen.text-color-blue .app-window-title,
        .screen.text-color-blue .settings-item-title, .screen.text-color-blue .settings-detail-title,
        .screen.text-color-blue .settings-detail-item .label, .screen.text-color-blue .note-item .note-title,
        .screen.text-color-blue .note-viewer .note-viewer-title, .screen.text-color-blue .gallery-item .gallery-name,
        .screen.text-color-blue .modal-title, .screen.text-color-blue .editor-toolbar button,
        .screen.text-color-blue .layer-item .layer-name, .screen.text-color-blue .music-item .music-name,
        .screen.text-color-blue .store-app .store-app-name, .screen.text-color-blue .wallpaper-option .wallpaper-name,
        .screen.text-color-blue .root-status, .screen.text-color-blue .account-menu .account-title,
        .screen.text-color-blue .account-menu .account-status { color: #3b82f6 !important; }
        .screen.text-color-green .logo-text, .screen.text-color-green .app-name, .screen.text-color-green .app-window-title,
        .screen.text-color-green .settings-item-title, .screen.text-color-green .settings-detail-title,
        .screen.text-color-green .settings-detail-item .label, .screen.text-color-green .note-item .note-title,
        .screen.text-color-green .note-viewer .note-viewer-title, .screen.text-color-green .gallery-item .gallery-name,
        .screen.text-color-green .modal-title, .screen.text-color-green .editor-toolbar button,
        .screen.text-color-green .layer-item .layer-name, .screen.text-color-green .music-item .music-name,
        .screen.text-color-green .store-app .store-app-name, .screen.text-color-green .wallpaper-option .wallpaper-name,
        .screen.text-color-green .root-status, .screen.text-color-green .account-menu .account-title,
        .screen.text-color-green .account-menu .account-status { color: #22c55e !important; }
        .screen.text-color-purple .logo-text, .screen.text-color-purple .app-name, .screen.text-color-purple .app-window-title,
        .screen.text-color-purple .settings-item-title, .screen.text-color-purple .settings-detail-title,
        .screen.text-color-purple .settings-detail-item .label, .screen.text-color-purple .note-item .note-title,
        .screen.text-color-purple .note-viewer .note-viewer-title, .screen.text-color-purple .gallery-item .gallery-name,
        .screen.text-color-purple .modal-title, .screen.text-color-purple .editor-toolbar button,
        .screen.text-color-purple .layer-item .layer-name, .screen.text-color-purple .music-item .music-name,
        .screen.text-color-purple .store-app .store-app-name, .screen.text-color-purple .wallpaper-option .wallpaper-name,
        .screen.text-color-purple .root-status, .screen.text-color-purple .account-menu .account-title,
        .screen.text-color-purple .account-menu .account-status { color: #a855f7 !important; }

        .status-bar {
            display: flex;
            justify-content: space-between;
            font-size: 15px;
            font-weight: 500;
            color: rgba(210, 220, 255, 0.7);
            padding-bottom: 14px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.03);
            margin-bottom: 12px;
            flex-shrink: 0;
            z-index: 10;
        }
        .status-left i,
        .status-right i { margin: 0 4px; font-size: 13px; opacity: 0.8; }

        .aurora-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            flex-shrink: 0;
            z-index: 10;
        }
        .logo-area { display: flex; align-items: center; gap: 10px; }
        .logo-icon { font-size: 28px; background: linear-gradient(135deg, #f472b6, #fb923c); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; filter: drop-shadow(0 0 10px rgba(244, 114, 182, 0.3)); }
        .logo-text { font-weight: 700; font-size: 22px; background: linear-gradient(to right, #fbcfe8, #fdba74); -webkit-background-clip: text; -webkit-text-fill-color: transparent; letter-spacing: -0.5px; transition: color 0.3s; }
        .logo-text .question-mark { background: linear-gradient(to right, #f472b6, #fb923c); -webkit-background-clip: text; -webkit-text-fill-color: transparent; font-weight: 800; }

        .spiral-clock {
            background: rgba(255, 255, 255, 0.02);
            border-radius: 40px;
            padding: 6px 16px 6px 12px;
            border: 1px solid rgba(255, 255, 255, 0.04);
            display: flex;
            align-items: center;
            gap: 8px;
            backdrop-filter: blur(4px);
            font-size: 15px;
            font-weight: 400;
            color: #cbd5e1;
            cursor: pointer;
            transition: 0.3s;
        }
        .spiral-clock:hover { background: rgba(255, 255, 255, 0.04); }
        .spiral-clock i { font-size: 17px; color: #f472b6; transition: transform 1s ease; }
        .spiral-ring { display: inline-block; transform: rotate(var(--spiral-rotate, 120deg)); transition: transform 0.8s cubic-bezier(0.34, 1.56, 0.64, 1); }

        .app-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 18px 12px;
            margin: 8px 0 16px;
            flex-shrink: 0;
            z-index: 10;
        }
        .app-grid.hidden { display: none; }

        .app-item { display: flex; flex-direction: column; align-items: center; gap: 6px; transition: all 0.2s ease; cursor: pointer; }
        .app-icon {
            width: 64px;
            height: 64px;
            border-radius: 22px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 28px;
            color: white;
            box-shadow: 0 10px 20px -8px rgba(0, 0, 0, 0.7);
            transition: all 0.25s cubic-bezier(0.34, 1.56, 0.64, 1);
            background: rgba(255, 255, 255, 0.03);
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.04);
        }
        .app-icon.grad-1 { background: linear-gradient(145deg, #ec4899, #f472b6); }
        .app-icon.grad-2 { background: linear-gradient(145deg, #f59e0b, #fbbf24); }
        .app-icon.grad-3 { background: linear-gradient(145deg, #8b5cf6, #a78bfa); }
        .app-icon.grad-4 { background: linear-gradient(145deg, #06b6d4, #22d3ee); }
        .app-icon.grad-5 { background: linear-gradient(145deg, #ef4444, #f87171); }
        .app-icon.grad-6 { background: linear-gradient(145deg, #10b981, #34d399); }
        .app-icon.grad-7 { background: linear-gradient(145deg, #f97316, #fb923c); }
        .app-icon.grad-8 { background: linear-gradient(145deg, #6366f1, #818cf8); }
        .app-icon.grad-admin { background: linear-gradient(145deg, #8b5cf6, #a855f7); }
        .app-icon.grad-owner { background: linear-gradient(145deg, #fbbf24, #f59e0b); }
        .app-icon.grad-clicker { background: linear-gradient(145deg, #f472b6, #ec4899); }
        .app-name { font-size: 12px; color: rgba(210, 220, 255, 0.65); font-weight: 450; letter-spacing: 0.2px; white-space: nowrap; transition: color 0.3s; }
        .app-item:active .app-icon { transform: scale(0.94); filter: brightness(1.2); }

        .app-pages {
            display: flex;
            gap: 8px;
            justify-content: center;
            margin-top: 4px;
            flex-shrink: 0;
            z-index: 10;
        }
        .app-pages .page-dot {
            width: 8px;
            height: 8px;
            border-radius: 50%;
            background: rgba(210, 220, 255, 0.15);
            cursor: pointer;
            transition: 0.3s;
        }
        .app-pages .page-dot.active {
            background: #f472b6;
            width: 20px;
            border-radius: 10px;
        }
        .app-pages .page-dot:hover {
            background: rgba(244, 114, 182, 0.3);
        }

        .gesture-area {
            margin: 8px 0 6px;
            padding: 10px 0;
            display: flex;
            justify-content: center;
            border-top: 1px dashed rgba(255, 255, 255, 0.03);
            border-bottom: 1px dashed rgba(255, 255, 255, 0.03);
            flex-shrink: 0;
            z-index: 10;
        }
        .gesture-pill {
            background: rgba(255, 255, 255, 0.02);
            padding: 10px 28px;
            border-radius: 60px;
            color: rgba(180, 190, 220, 0.5);
            font-size: 13px;
            letter-spacing: 1px;
            display: flex;
            align-items: center;
            gap: 14px;
            backdrop-filter: blur(4px);
            border: 1px solid rgba(255, 255, 255, 0.02);
            transition: 0.25s;
            cursor: pointer;
        }
        .gesture-pill i { color: #f472b6; font-size: 15px; }

        .nav-bar {
            display: flex;
            justify-content: space-around;
            align-items: center;
            padding: 12px 10px 4px;
            margin-top: 4px;
            border-top: 1px solid rgba(255, 255, 255, 0.02);
            flex-shrink: 0;
            z-index: 10;
        }
        .nav-item {
            color: rgba(180, 190, 220, 0.35);
            font-size: 22px;
            transition: 0.2s;
            padding: 6px 16px;
            border-radius: 40px;
            background: transparent;
            cursor: pointer;
        }
        .nav-item.active { color: #f472b6; background: rgba(244, 114, 182, 0.06); }
        .nav-item i { filter: drop-shadow(0 0 6px rgba(244, 114, 182, 0.2)); }

        .back-tap-hint { display: flex; justify-content: center; margin: 4px 0 2px; font-size: 11px; color: rgba(255, 255, 255, 0.08); letter-spacing: 1.5px; gap: 6px; flex-shrink: 0; z-index: 10; }
        .back-tap-hint i { color: rgba(244, 114, 182, 0.2); }

        .compress-demo { display: flex; justify-content: center; gap: 8px; margin-top: 4px; cursor: pointer; flex-shrink: 0; z-index: 10; }
        .compress-dot { width: 7px; height: 7px; background: rgba(244, 114, 182, 0.15); border-radius: 20px; transition: 0.3s; }
        .compress-dot.active { background: #f472b6; width: 22px; }

        .app-window {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(14, 18, 28, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            transform: translateY(100%);
            transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            z-index: 100;
            display: flex;
            flex-direction: column;
            padding: 20px 18px 16px;
            overflow: hidden;
        }
        .app-window.open { transform: translateY(0); }

        .app-window-header {
            display: flex;
            align-items: center;
            gap: 16px;
            padding-bottom: 16px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            margin-bottom: 20px;
            flex-shrink: 0;
        }
        .app-window-back { font-size: 24px; color: rgba(210, 220, 255, 0.6); cursor: pointer; transition: 0.2s; padding: 4px 8px; border-radius: 12px; }
        .app-window-back:hover { background: rgba(255, 255, 255, 0.05); color: #f472b6; }
        .app-window-title { font-size: 20px; font-weight: 600; color: #e0e7ff; flex: 1; transition: color 0.3s; }
        .app-window-close { font-size: 22px; color: rgba(210, 220, 255, 0.4); cursor: pointer; transition: 0.2s; padding: 4px 8px; border-radius: 12px; }
        .app-window-close:hover { background: rgba(255, 255, 255, 0.05); color: #f472b6; }
        .app-window-body { flex: 1; overflow-y: auto; padding-right: 4px; }
        .app-window-body::-webkit-scrollbar { width: 4px; }
        .app-window-body::-webkit-scrollbar-track { background: transparent; }
        .app-window-body::-webkit-scrollbar-thumb { background: rgba(244, 114, 182, 0.2); border-radius: 10px; }

        /* ===== НАСТРОЙКИ ===== */
        .settings-list { display: flex; flex-direction: column; gap: 4px; }
        .settings-item {
            display: flex;
            align-items: center;
            gap: 16px;
            padding: 14px 16px;
            border-radius: 16px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.02);
            transition: 0.2s;
            cursor: pointer;
        }
        .settings-item:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.1); }
        .settings-item-icon {
            width: 40px;
            height: 40px;
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 18px;
            color: white;
            flex-shrink: 0;
        }
        .settings-item-icon.pink { background: rgba(244, 114, 182, 0.2); color: #f472b6; }
        .settings-item-icon.blue { background: rgba(99, 102, 241, 0.2); color: #818cf8; }
        .settings-item-icon.green { background: rgba(52, 211, 153, 0.2); color: #34d399; }
        .settings-item-icon.orange { background: rgba(251, 146, 60, 0.2); color: #fb923c; }
        .settings-item-icon.purple { background: rgba(167, 139, 250, 0.2); color: #a78bfa; }
        .settings-item-icon.red { background: rgba(239, 68, 68, 0.2); color: #f87171; }
        .settings-item-icon.teal { background: rgba(20, 184, 166, 0.2); color: #14b8a6; }
        .settings-item-icon.indigo { background: rgba(99, 102, 241, 0.2); color: #818cf8; }
        .settings-item-info { flex: 1; }
        .settings-item-title { color: #e0e7ff; font-size: 15px; font-weight: 500; transition: color 0.3s; }
        .settings-item-desc { color: rgba(210, 220, 255, 0.4); font-size: 12px; margin-top: 2px; }
        .settings-item-arrow { color: rgba(210, 220, 255, 0.2); font-size: 14px; }

        .settings-detail {
            display: none;
            flex-direction: column;
            gap: 12px;
            animation: fadeSlide 0.3s ease;
        }
        .settings-detail.active { display: flex; }
        @keyframes fadeSlide {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .settings-detail-header {
            display: flex;
            align-items: center;
            gap: 12px;
            padding-bottom: 12px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            margin-bottom: 8px;
        }
        .settings-detail-back { font-size: 20px; color: rgba(210, 220, 255, 0.5); cursor: pointer; transition: 0.2s; padding: 4px 8px; border-radius: 10px; }
        .settings-detail-back:hover { background: rgba(255, 255, 255, 0.05); color: #f472b6; }
        .settings-detail-title { color: #e0e7ff; font-size: 17px; font-weight: 500; transition: color 0.3s; }

        .settings-detail-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 12px 16px;
            border-radius: 14px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.02);
            transition: 0.2s;
            cursor: pointer;
        }
        .settings-detail-item:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.05); }
        .settings-detail-item .label { color: rgba(210, 220, 255, 0.7); font-size: 14px; transition: color 0.3s; }
        .settings-detail-item .value { color: rgba(210, 220, 255, 0.4); font-size: 14px; transition: color 0.3s; }
        .settings-detail-item .value.on { color: #34d399; }
        .settings-detail-item .toggle { color: #f472b6; font-size: 26px; transition: 0.3s; cursor: pointer; }
        .settings-detail-item .toggle.off { color: rgba(210, 220, 255, 0.15); }
        .settings-detail-item .toggle:hover { transform: scale(1.1); }

        .root-status { color: rgba(210, 220, 255, 0.3); font-size: 12px; font-weight: 400; transition: color 0.3s; }
        .root-status.on { color: #34d399; }
        .root-status.off { color: rgba(210, 220, 255, 0.3); }

        /* ===== ЧЕРНОВИК ===== */
        .notes-header {
            display: flex;
            gap: 12px;
            margin-bottom: 16px;
            flex-shrink: 0;
        }
        .notes-search {
            flex: 1;
            background: rgba(255, 255, 255, 0.05);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 14px;
            padding: 10px 16px;
            color: #e0e7ff;
            font-size: 14px;
            outline: none;
            transition: 0.3s;
        }
        .notes-search::placeholder { color: rgba(210, 220, 255, 0.3); }
        .notes-search:focus { border-color: rgba(244, 114, 182, 0.3); background: rgba(255, 255, 255, 0.08); }
        .notes-create-btn {
            background: linear-gradient(135deg, #f472b6, #fb923c);
            border: none;
            border-radius: 14px;
            padding: 10px 20px;
            color: white;
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
            white-space: nowrap;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        .notes-create-btn:hover { transform: scale(1.02); box-shadow: 0 4px 20px rgba(244, 114, 182, 0.3); }
        .notes-create-btn i { font-size: 16px; }

        .notes-list { display: flex; flex-direction: column; gap: 8px; flex: 1; overflow-y: auto; padding-bottom: 10px; }
        .notes-list::-webkit-scrollbar { width: 4px; }
        .notes-list::-webkit-scrollbar-track { background: transparent; }
        .notes-list::-webkit-scrollbar-thumb { background: rgba(244, 114, 182, 0.2); border-radius: 10px; }

        .note-item {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 14px;
            padding: 14px 16px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .note-item:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.1); }
        .note-item .note-info { flex: 1; min-width: 0; }
        .note-item .note-title { color: #e0e7ff; font-weight: 500; font-size: 15px; transition: color 0.3s; }
        .note-item .note-preview { color: rgba(210, 220, 255, 0.4); font-size: 13px; margin-top: 2px; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
        .note-item .note-date { color: rgba(210, 220, 255, 0.2); font-size: 11px; flex-shrink: 0; margin-left: 12px; }
        .note-empty { color: rgba(210, 220, 255, 0.2); text-align: center; padding: 40px 0; font-size: 14px; }

        .note-viewer {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(14, 18, 28, 0.98);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            transform: translateY(100%);
            transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
            z-index: 200;
            display: flex;
            flex-direction: column;
            padding: 20px 18px 16px;
        }
        .note-viewer.open { transform: translateY(0); }
        .note-viewer-header {
            display: flex;
            align-items: center;
            gap: 16px;
            padding-bottom: 16px;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            margin-bottom: 16px;
            flex-shrink: 0;
        }
        .note-viewer-back { font-size: 24px; color: rgba(210, 220, 255, 0.6); cursor: pointer; transition: 0.2s; padding: 4px 8px; border-radius: 12px; }
        .note-viewer-back:hover { background: rgba(255, 255, 255, 0.05); color: #f472b6; }
        .note-viewer-title { font-size: 18px; font-weight: 600; color: #e0e7ff; flex: 1; transition: color 0.3s; }
        .note-viewer-delete { font-size: 20px; color: rgba(239, 68, 68, 0.4); cursor: pointer; transition: 0.2s; padding: 4px 8px; border-radius: 12px; }
        .note-viewer-delete:hover { background: rgba(239, 68, 68, 0.1); color: #ef4444; }
        .note-viewer textarea {
            flex: 1;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 14px;
            padding: 16px;
            color: #e0e7ff;
            font-size: 15px;
            line-height: 1.6;
            resize: none;
            outline: none;
            font-family: inherit;
            transition: 0.3s;
        }
        .note-viewer textarea:focus { border-color: rgba(244, 114, 182, 0.2); background: rgba(255, 255, 255, 0.04); }
        .note-viewer textarea::placeholder { color: rgba(210, 220, 255, 0.2); }

        .create-note-modal {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            z-index: 300;
            display: none;
            justify-content: center;
            align-items: center;
            padding: 30px;
        }
        .create-note-modal.open { display: flex; }
        .create-note-modal .modal-content {
            background: rgba(14, 18, 28, 0.95);
            border-radius: 24px;
            padding: 30px;
            max-width: 400px;
            width: 100%;
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
        }
        .create-note-modal .modal-title { color: #e0e7ff; font-size: 20px; font-weight: 600; margin-bottom: 20px; transition: color 0.3s; }
        .create-note-modal .modal-label { color: rgba(210, 220, 255, 0.5); font-size: 13px; font-weight: 500; margin-bottom: 6px; display: block; transition: color 0.3s; }
        .create-note-modal input {
            width: 100%;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 12px 16px;
            color: #e0e7ff;
            font-size: 15px;
            outline: none;
            transition: 0.3s;
            margin-bottom: 16px;
        }
        .create-note-modal input:focus { border-color: rgba(244, 114, 182, 0.3); background: rgba(255, 255, 255, 0.06); }
        .create-note-modal input::placeholder { color: rgba(210, 220, 255, 0.2); }
        .create-note-modal .modal-actions { display: flex; gap: 12px; justify-content: flex-end; }
        .create-note-modal .modal-btn {
            padding: 10px 24px;
            border-radius: 12px;
            border: none;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.3s;
        }
        .create-note-modal .modal-btn.cancel { background: rgba(255, 255, 255, 0.05); color: rgba(210, 220, 255, 0.5); }
        .create-note-modal .modal-btn.cancel:hover { background: rgba(255, 255, 255, 0.1); }
        .create-note-modal .modal-btn.create { background: linear-gradient(135deg, #f472b6, #fb923c); color: white; }
        .create-note-modal .modal-btn.create:hover { transform: scale(1.02); box-shadow: 0 4px 20px rgba(244, 114, 182, 0.3); }

        /* ===== ГАЛЕРЕЯ ===== */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 12px;
            padding: 10px 0;
        }
        .gallery-item {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 16px;
            padding: 20px 16px;
            text-align: center;
            cursor: pointer;
            transition: 0.3s;
        }
        .gallery-item:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.1); }
        .gallery-item .gallery-icon { font-size: 32px; color: #f472b6; margin-bottom: 8px; display: block; }
        .gallery-item .gallery-name { color: #e0e7ff; font-weight: 500; font-size: 14px; transition: color 0.3s; }
        .gallery-item .gallery-count { color: rgba(210, 220, 255, 0.3); font-size: 12px; margin-top: 4px; }

        .photo-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 8px;
            padding: 4px 0;
        }
        .photo-grid .photo-item {
            aspect-ratio: 1;
            border-radius: 12px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            cursor: pointer;
            transition: 0.3s;
        }
        .photo-grid .photo-item:hover { border-color: rgba(244, 114, 182, 0.2); }
        .photo-grid .photo-item img { width: 100%; height: 100%; object-fit: cover; }
        .photo-grid .photo-item video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .photo-grid .photo-item .video-play {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 32px;
            opacity: 0.7;
            text-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            pointer-events: none;
        }
        .photo-grid .photo-item .video-duration {
            position: absolute;
            bottom: 4px;
            right: 4px;
            background: rgba(0, 0, 0, 0.6);
            color: white;
            font-size: 11px;
            padding: 2px 8px;
            border-radius: 10px;
            font-family: monospace;
        }
        .photo-grid .photo-item .photo-delete {
            position: absolute;
            top: 4px;
            right: 4px;
            background: rgba(239, 68, 68, 0.8);
            border: none;
            color: white;
            border-radius: 50%;
            width: 24px;
            height: 24px;
            font-size: 12px;
            cursor: pointer;
            display: none;
            align-items: center;
            justify-content: center;
        }
        .photo-grid .photo-item:hover .photo-delete { display: flex; }

        .gallery-header-actions { display: flex; gap: 10px; margin-bottom: 12px; }
        .gallery-header-actions button {
            background: rgba(244, 114, 182, 0.1);
            border: 1px solid rgba(244, 114, 182, 0.2);
            border-radius: 12px;
            padding: 8px 16px;
            color: #e0e7ff;
            font-size: 13px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            align-items: center;
            gap: 6px;
        }
        .gallery-header-actions button:hover { background: rgba(244, 114, 182, 0.2); }

        /* ===== МЕДИА-ПРОСМОТРЩИК ===== */
        .media-viewer {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            z-index: 250;
            display: none;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        .media-viewer.open { display: flex; }
        .media-viewer .media-viewer-close {
            position: absolute;
            top: 16px;
            right: 20px;
            color: rgba(255, 255, 255, 0.4);
            font-size: 28px;
            cursor: pointer;
            transition: 0.2s;
            z-index: 10;
        }
        .media-viewer .media-viewer-close:hover { color: white; }
        .media-viewer .media-viewer-content {
            max-width: 90%;
            max-height: 80%;
            border-radius: 12px;
            object-fit: contain;
        }
        .media-viewer .media-viewer-content video {
            max-width: 90%;
            max-height: 80%;
            border-radius: 12px;
        }
        .media-viewer .media-viewer-content img {
            max-width: 90%;
            max-height: 80%;
            border-radius: 12px;
        }
        .media-viewer .media-viewer-info {
            color: rgba(255, 255, 255, 0.3);
            font-size: 14px;
            margin-top: 16px;
            text-align: center;
        }

        /* ===== МОНТАЖ ===== */
        .editor-container {
            display: flex;
            flex-direction: column;
            height: 100%;
            gap: 10px;
        }
        .editor-canvas-wrap {
            flex: 2;
            min-height: 250px;
            background: rgba(0, 0, 0, 0.3);
            border-radius: 16px;
            border: 1px solid rgba(255, 255, 255, 0.03);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            cursor: default;
        }
        .editor-canvas-wrap canvas { max-width: 100%; max-height: 100%; object-fit: contain; cursor: default; }
        .editor-canvas-wrap .editor-placeholder { color: rgba(210, 220, 255, 0.2); text-align: center; font-size: 14px; }
        .editor-canvas-wrap .editor-placeholder i { font-size: 48px; display: block; margin-bottom: 12px; }

        .editor-bottom { display: flex; gap: 10px; flex: 1; min-height: 120px; }
        .editor-toolbar-wrap { display: flex; flex-direction: column; gap: 6px; flex: 2; }
        .editor-toolbar {
            display: flex;
            flex-wrap: wrap;
            gap: 4px;
            padding: 8px 10px;
            background: rgba(255, 255, 255, 0.02);
            border-radius: 14px;
            border: 1px solid rgba(255, 255, 255, 0.03);
            flex-shrink: 0;
        }
        .editor-toolbar button {
            background: transparent;
            border: none;
            color: rgba(210, 220, 255, 0.5);
            padding: 5px 10px;
            border-radius: 8px;
            font-size: 12px;
            cursor: pointer;
            transition: 0.2s;
            display: flex;
            align-items: center;
            gap: 4px;
        }
        .editor-toolbar button:hover { background: rgba(255, 255, 255, 0.05); color: #f472b6; }
        .editor-toolbar button.active { background: rgba(244, 114, 182, 0.1); color: #f472b6; }

        .editor-controls { display: flex; flex-wrap: wrap; gap: 8px; padding: 4px 0; flex-shrink: 0; }
        .editor-controls label { color: rgba(210, 220, 255, 0.4); font-size: 11px; display: flex; align-items: center; gap: 6px; }
        .editor-controls input[type="range"] {
            width: 60px;
            height: 4px;
            -webkit-appearance: none;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 2px;
            outline: none;
        }
        .editor-controls input[type="range"]::-webkit-slider-thumb {
            -webkit-appearance: none;
            width: 12px;
            height: 12px;
            border-radius: 50%;
            background: #f472b6;
            cursor: pointer;
        }
        .filter-chips { display: flex; flex-wrap: wrap; gap: 4px; }
        .filter-chip {
            padding: 3px 10px;
            border-radius: 16px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            color: rgba(210, 220, 255, 0.4);
            font-size: 10px;
            cursor: pointer;
            transition: 0.3s;
        }
        .filter-chip:hover { background: rgba(255, 255, 255, 0.05); }
        .filter-chip.active { background: rgba(244, 114, 182, 0.1); color: #f472b6; border-color: rgba(244, 114, 182, 0.2); }

        .layers-panel {
            flex: 1;
            min-width: 120px;
            max-width: 200px;
            background: rgba(255, 255, 255, 0.02);
            border-radius: 14px;
            border: 1px solid rgba(255, 255, 255, 0.03);
            padding: 8px 10px;
            overflow-y: auto;
        }
        .layers-panel::-webkit-scrollbar { width: 3px; }
        .layers-panel::-webkit-scrollbar-thumb { background: rgba(244, 114, 182, 0.2); border-radius: 10px; }
        .layers-title { color: rgba(210, 220, 255, 0.3); font-size: 10px; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 6px; }
        .layer-item {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding: 4px 8px;
            border-radius: 8px;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.02);
            margin-bottom: 3px;
            cursor: pointer;
            transition: 0.2s;
            font-size: 11px;
        }
        .layer-item:hover { background: rgba(255, 255, 255, 0.04); }
        .layer-item .layer-name { color: rgba(210, 220, 255, 0.6); transition: color 0.3s; flex: 1; overflow: hidden; text-overflow: ellipsis; white-space: nowrap; }
        .layer-item .layer-delete { color: rgba(210, 220, 255, 0.2); cursor: pointer; padding: 0 4px; font-size: 10px; transition: 0.2s; }
        .layer-item .layer-delete:hover { color: #ef4444; }
        .layer-item.active { background: rgba(244, 114, 182, 0.08); border-color: rgba(244, 114, 182, 0.15); }
        .layer-item .layer-vis { margin-right: 6px; font-size: 10px; color: rgba(210, 220, 255, 0.2); cursor: pointer; }

        /* ===== МУЗЫКА ===== */
        .music-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); gap: 10px; padding: 8px 0; }
        .music-item {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 14px;
            padding: 14px 12px;
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 4px;
        }
        .music-item:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.1); }
        .music-item .music-icon { font-size: 28px; color: #f472b6; }
        .music-item .music-name { color: #e0e7ff; font-size: 13px; font-weight: 500; text-align: center; word-break: break-all; transition: color 0.3s; }
        .music-item .music-size { color: rgba(210, 220, 255, 0.2); font-size: 10px; }
        .music-item .music-delete { color: rgba(210, 220, 255, 0.15); cursor: pointer; font-size: 12px; transition: 0.2s; margin-top: 4px; }
        .music-item .music-delete:hover { color: #ef4444; }

        .music-upload-btn {
            background: rgba(244, 114, 182, 0.1);
            border: 2px dashed rgba(244, 114, 182, 0.2);
            border-radius: 14px;
            padding: 20px;
            text-align: center;
            cursor: pointer;
            transition: 0.3s;
            color: rgba(210, 220, 255, 0.3);
            font-size: 13px;
        }
        .music-upload-btn:hover { background: rgba(244, 114, 182, 0.05); border-color: rgba(244, 114, 182, 0.3); }
        .music-upload-btn i { font-size: 32px; display: block; margin-bottom: 8px; color: #f472b6; }

        /* ===== POFO PLAY ===== */
        .store-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(160px, 1fr)); gap: 12px; padding: 8px 0; }
        .store-app {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 16px;
            padding: 16px;
            text-align: center;
            cursor: pointer;
            transition: 0.3s;
        }
        .store-app:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.1); }
        .store-app .store-app-icon { font-size: 36px; color: #f472b6; display: block; margin-bottom: 8px; }
        .store-app .store-app-name { color: #e0e7ff; font-weight: 500; font-size: 14px; transition: color 0.3s; }
        .store-app .store-app-desc { color: rgba(210, 220, 255, 0.3); font-size: 11px; margin-top: 4px; }
        .store-app .store-app-btn {
            margin-top: 10px;
            background: rgba(244, 114, 182, 0.1);
            border: 1px solid rgba(244, 114, 182, 0.2);
            border-radius: 10px;
            padding: 4px 16px;
            color: #e0e7ff;
            font-size: 12px;
            cursor: pointer;
            transition: 0.3s;
        }
        .store-app .store-app-btn:hover { background: rgba(244, 114, 182, 0.2); }
        .store-app .store-app-btn.installed { background: rgba(52, 211, 153, 0.15); border-color: rgba(52, 211, 153, 0.2); color: #34d399; cursor: default; }
        .store-app .store-app-btn.installed:hover { background: rgba(52, 211, 153, 0.15); }

        /* ===== КЛИКЕР ===== */
        .clicker-container {
            display: flex;
            flex-direction: column;
            height: 100%;
            gap: 16px;
        }
        .clicker-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 12px 16px;
            background: rgba(255, 255, 255, 0.02);
            border-radius: 14px;
            border: 1px solid rgba(255, 255, 255, 0.03);
        }
        .clicker-header .clicker-coins {
            color: #f472b6;
            font-size: 20px;
            font-weight: 700;
        }
        .clicker-header .clicker-stats {
            color: rgba(210, 220, 255, 0.3);
            font-size: 13px;
        }

        .clicker-area {
            flex: 1;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 16px;
            background: rgba(255, 255, 255, 0.01);
            border-radius: 20px;
            border: 1px solid rgba(255, 255, 255, 0.02);
            cursor: pointer;
            transition: 0.2s;
            min-height: 200px;
            position: relative;
        }
        .clicker-area:active { transform: scale(0.98); }
        .clicker-area .clicker-big {
            font-size: 64px;
            color: #f472b6;
            opacity: 0.4;
        }
        .clicker-area .clicker-count {
            font-size: 48px;
            font-weight: 700;
            color: #e0e7ff;
        }
        .clicker-area .clicker-per-click {
            color: rgba(210, 220, 255, 0.2);
            font-size: 14px;
        }

        .clicker-shop {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
            gap: 8px;
            padding: 8px 0;
            flex-shrink: 0;
        }
        .clicker-shop .shop-item {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            padding: 12px;
            text-align: center;
            cursor: pointer;
            transition: 0.3s;
        }
        .clicker-shop .shop-item:hover { background: rgba(255, 255, 255, 0.04); border-color: rgba(244, 114, 182, 0.1); }
        .clicker-shop .shop-item .shop-name { color: #e0e7ff; font-size: 13px; font-weight: 500; }
        .clicker-shop .shop-item .shop-cost { color: rgba(210, 220, 255, 0.3); font-size: 11px; }
        .clicker-shop .shop-item .shop-btn {
            margin-top: 6px;
            background: rgba(244, 114, 182, 0.1);
            border: 1px solid rgba(244, 114, 182, 0.2);
            border-radius: 8px;
            padding: 4px 12px;
            color: #e0e7ff;
            font-size: 11px;
            cursor: pointer;
            transition: 0.3s;
        }
        .clicker-shop .shop-item .shop-btn:hover { background: rgba(244, 114, 182, 0.2); }
        .clicker-shop .shop-item .shop-btn.owned { background: rgba(52, 211, 153, 0.15); border-color: rgba(52, 211, 153, 0.2); color: #34d399; cursor: default; }

        .clicker-mode-switch {
            display: flex;
            gap: 8px;
            justify-content: center;
            flex-shrink: 0;
        }
        .clicker-mode-switch button {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 8px 20px;
            color: rgba(210, 220, 255, 0.4);
            font-size: 13px;
            cursor: pointer;
            transition: 0.3s;
        }
        .clicker-mode-switch button:hover { background: rgba(255, 255, 255, 0.04); }
        .clicker-mode-switch button.active { background: rgba(244, 114, 182, 0.1); color: #f472b6; border-color: rgba(244, 114, 182, 0.2); }

        .clicker-reward {
            background: rgba(52, 211, 153, 0.05);
            border: 1px solid rgba(52, 211, 153, 0.1);
            border-radius: 14px;
            padding: 16px;
            text-align: center;
            margin-top: 8px;
            flex-shrink: 0;
        }
        .clicker-reward .reward-text {
            color: #34d399;
            font-size: 16px;
            font-weight: 600;
        }
        .clicker-reward .reward-sub {
            color: rgba(210, 220, 255, 0.3);
            font-size: 13px;
        }
        .clicker-reward .reward-btn {
            margin-top: 8px;
            background: linear-gradient(135deg, #34d399, #10b981);
            border: none;
            border-radius: 12px;
            padding: 8px 24px;
            color: white;
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
        }
        .clicker-reward .reward-btn:hover { transform: scale(1.02); box-shadow: 0 4px 20px rgba(52, 211, 153, 0.3); }
        .clicker-reward .reward-btn:disabled { opacity: 0.3; cursor: default; transform: none; }

        /* ===== ОБОИ ===== */
        .wallpaper-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 10px; padding: 8px 0; }
        .wallpaper-option {
            aspect-ratio: 9/16;
            border-radius: 14px;
            border: 2px solid rgba(255, 255, 255, 0.05);
            cursor: pointer;
            transition: 0.3s;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
            background: rgba(255, 255, 255, 0.02);
        }
        .wallpaper-option:hover { border-color: rgba(244, 114, 182, 0.3); transform: scale(1.02); }
        .wallpaper-option .wallpaper-preview {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
        }
        .wallpaper-option .wallpaper-preview img { width: 100%; height: 100%; object-fit: cover; }
        .wallpaper-option .wallpaper-preview video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .wallpaper-option .wallpaper-preview .video-play-icon {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: rgba(255, 255, 255, 0.4);
            font-size: 40px;
            z-index: 1;
        }
        .wallpaper-option .wallpaper-name {
            position: relative;
            z-index: 1;
            color: #e0e7ff;
            font-weight: 500;
            font-size: 14px;
            background: rgba(0, 0, 0, 0.3);
            padding: 4px 12px;
            border-radius: 20px;
            backdrop-filter: blur(4px);
            transition: color 0.3s;
        }
        .wallpaper-option .wallpaper-check {
            position: absolute;
            top: 8px;
            right: 8px;
            color: #34d399;
            font-size: 18px;
            display: none;
            z-index: 2;
        }
        .wallpaper-option.active { border-color: #34d399; }
        .wallpaper-option.active .wallpaper-check { display: block; }

        .color-picker-input {
            width: 100%;
            padding: 8px 12px;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            color: #e0e7ff;
            font-size: 14px;
            outline: none;
            transition: 0.3s;
            font-family: monospace;
        }
        .color-picker-input:focus { border-color: rgba(244, 114, 182, 0.3); background: rgba(255, 255, 255, 0.06); }
        .color-picker-input::placeholder { color: rgba(210, 220, 255, 0.2); }

        .install-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            z-index: 400;
            display: none;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            gap: 20px;
        }
        .install-overlay.open { display: flex; }
        .install-overlay .spinner {
            width: 50px;
            height: 50px;
            border: 4px solid rgba(244, 114, 182, 0.1);
            border-top: 4px solid #f472b6;
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        .install-overlay .install-text {
            color: #e0e7ff;
            font-size: 16px;
            font-weight: 400;
            opacity: 0.7;
        }

        /* ===== АККАУНТЫ ===== */
        .account-menu {
            position: absolute;
            bottom: 70px;
            left: 50%;
            transform: translateX(-50%) translateY(20px);
            background: rgba(14, 18, 28, 0.95);
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border-radius: 24px;
            border: 1px solid rgba(255, 255, 255, 0.05);
            padding: 20px;
            min-width: 300px;
            max-width: 380px;
            width: 90%;
            z-index: 50;
            opacity: 0;
            pointer-events: none;
            transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.6);
        }
        .account-menu.open {
            opacity: 1;
            pointer-events: all;
            transform: translateX(-50%) translateY(0);
        }

        .account-menu .account-title {
            color: #e0e7ff;
            font-size: 18px;
            font-weight: 600;
            margin-bottom: 12px;
            text-align: center;
        }

        .account-menu .account-input {
            width: 100%;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 10px 14px;
            color: #e0e7ff;
            font-size: 14px;
            outline: none;
            transition: 0.3s;
            margin-bottom: 10px;
        }
        .account-menu .account-input:focus {
            border-color: rgba(244, 114, 182, 0.3);
            background: rgba(255, 255, 255, 0.06);
        }
        .account-menu .account-input::placeholder {
            color: rgba(210, 220, 255, 0.2);
        }

        .account-menu .account-btn {
            width: 100%;
            background: linear-gradient(135deg, #f472b6, #fb923c);
            border: none;
            border-radius: 12px;
            padding: 10px;
            color: white;
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
        }
        .account-menu .account-btn:hover {
            transform: scale(1.02);
            box-shadow: 0 4px 20px rgba(244, 114, 182, 0.3);
        }

        .account-menu .account-status {
            color: rgba(210, 220, 255, 0.4);
            font-size: 12px;
            text-align: center;
            margin-top: 8px;
        }
        .account-menu .account-status .role {
            font-weight: 600;
            color: #f472b6;
        }

        .account-menu .account-logout {
            background: rgba(239, 68, 68, 0.1);
            border: 1px solid rgba(239, 68, 68, 0.2);
            border-radius: 12px;
            padding: 8px;
            color: #ef4444;
            font-size: 13px;
            cursor: pointer;
            transition: 0.3s;
            width: 100%;
            margin-top: 8px;
        }
        .account-menu .account-logout:hover {
            background: rgba(239, 68, 68, 0.2);
        }

        .account-menu .account-search {
            width: 100%;
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid rgba(255, 255, 255, 0.03);
            border-radius: 12px;
            padding: 8px 12px;
            color: rgba(210, 220, 255, 0.6);
            font-size: 13px;
            outline: none;
            transition: 0.3s;
            margin-bottom: 8px;
        }
        .account-menu .account-search:focus {
            border-color: rgba(244, 114, 182, 0.2);
            background: rgba(255, 255, 255, 0.04);
        }
        .account-menu .account-search::placeholder {
            color: rgba(210, 220, 255, 0.15);
        }

        .account-menu .user-list {
            max-height: 100px;
            overflow-y: auto;
            margin-top: 4px;
        }
        .account-menu .user-list::-webkit-scrollbar {
            width: 3px;
        }
        .account-menu .user-list::-webkit-scrollbar-thumb {
            background: rgba(244, 114, 182, 0.2);
            border-radius: 10px;
        }

        .account-menu .user-item {
            display: flex;
            justify-content: space-between;
            padding: 4px 8px;
            border-radius: 8px;
            color: rgba(210, 220, 255, 0.5);
            font-size: 13px;
            transition: 0.2s;
        }
        .account-menu .user-item:hover {
            background: rgba(255, 255, 255, 0.03);
        }
        .account-menu .user-item .user-role {
            font-size: 10px;
            padding: 1px 8px;
            border-radius: 10px;
            background: rgba(244, 114, 182, 0.1);
            color: #f472b6;
        }
        .account-menu .user-item .user-role.owner {
            background: rgba(251, 191, 36, 0.15);
            color: #fbbf24;
        }
        .account-menu .user-item .user-role.admin {
            background: rgba(52, 211, 153, 0.15);
            color: #34d399;
        }
        .account-menu .user-item .user-role.user {
            background: rgba(148, 163, 184, 0.1);
            color: #94a3b8;
        }

        .account-menu .account-close {
            position: absolute;
            top: 12px;
            right: 16px;
            color: rgba(210, 220, 255, 0.2);
            cursor: pointer;
            font-size: 18px;
            transition: 0.2s;
        }
        .account-menu .account-close:hover {
            color: rgba(210, 220, 255, 0.5);
        }

        /* ===== ЗАЩИТА ПРИЛОЖЕНИЙ ===== */
        .app-lock-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.85);
            backdrop-filter: blur(15px);
            -webkit-backdrop-filter: blur(15px);
            z-index: 500;
            display: none;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            gap: 20px;
        }
        .app-lock-overlay.open {
            display: flex;
        }

        .app-lock-overlay .lock-title {
            color: #e0e7ff;
            font-size: 22px;
            font-weight: 600;
            margin-bottom: 10px;
        }
        .app-lock-overlay .lock-sub {
            color: rgba(210, 220, 255, 0.3);
            font-size: 14px;
            margin-bottom: 20px;
        }

        .app-lock-overlay .lock-input {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 14px;
            padding: 12px 20px;
            color: #e0e7ff;
            font-size: 28px;
            font-weight: 600;
            outline: none;
            width: 200px;
            text-align: center;
            letter-spacing: 8px;
            transition: 0.3s;
            font-family: monospace;
        }
        .app-lock-overlay .lock-input:focus {
            border-color: rgba(244, 114, 182, 0.3);
            background: rgba(255, 255, 255, 0.06);
        }
        .app-lock-overlay .lock-input::placeholder {
            color: rgba(210, 220, 255, 0.1);
            font-size: 16px;
            letter-spacing: 2px;
        }

        .app-lock-overlay .lock-keypad {
            display: grid;
            grid-template-columns: repeat(3, 60px);
            gap: 10px;
            margin-top: 10px;
        }
        .app-lock-overlay .lock-key {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 14px;
            padding: 12px;
            color: #e0e7ff;
            font-size: 22px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.2s;
            text-align: center;
        }
        .app-lock-overlay .lock-key:hover {
            background: rgba(255, 255, 255, 0.08);
            border-color: rgba(244, 114, 182, 0.2);
        }
        .app-lock-overlay .lock-key:active {
            transform: scale(0.95);
        }

        .app-lock-overlay .lock-key.back {
            color: rgba(210, 220, 255, 0.3);
            font-size: 18px;
        }
        .app-lock-overlay .lock-key.clear {
            color: #ef4444;
        }

        .app-lock-overlay .lock-error {
            color: #ef4444;
            font-size: 13px;
            margin-top: 8px;
            min-height: 20px;
        }

        .app-lock-overlay .lock-btn {
            background: linear-gradient(135deg, #f472b6, #fb923c);
            border: none;
            border-radius: 12px;
            padding: 10px 30px;
            color: white;
            font-weight: 600;
            font-size: 14px;
            cursor: pointer;
            transition: 0.3s;
            margin-top: 10px;
        }
        .app-lock-overlay .lock-btn:hover {
            transform: scale(1.02);
            box-shadow: 0 4px 20px rgba(244, 114, 182, 0.3);
        }

        /* ===== МОДАЛ ===== */
        .modal-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(8px);
            -webkit-backdrop-filter: blur(8px);
            z-index: 300;
            display: none;
            justify-content: center;
            align-items: center;
            padding: 30px;
        }
        .modal-overlay.open { display: flex; }
        .modal-content {
            background: rgba(14, 18, 28, 0.95);
            border-radius: 24px;
            padding: 30px;
            max-width: 420px;
            width: 100%;
            border: 1px solid rgba(255, 255, 255, 0.05);
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
        }
        .modal-title { color: #e0e7ff; font-size: 20px; font-weight: 600; margin-bottom: 16px; transition: color 0.3s; }
        .modal-label { color: rgba(210, 220, 255, 0.5); font-size: 13px; font-weight: 500; margin-bottom: 6px; display: block; transition: color 0.3s; }
        .modal-input {
            width: 100%;
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.05);
            border-radius: 12px;
            padding: 12px 16px;
            color: #e0e7ff;
            font-size: 15px;
            outline: none;
            transition: 0.3s;
            margin-bottom: 16px;
        }
        .modal-input:focus { border-color: rgba(244, 114, 182, 0.3); background: rgba(255, 255, 255, 0.06); }
        .modal-input::placeholder { color: rgba(210, 220, 255, 0.2); }
        .modal-actions { display: flex; gap: 12px; justify-content: flex-end; }
        .modal-btn {
            padding: 10px 24px;
            border-radius: 12px;
            border: none;
            font-size: 14px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.3s;
        }
        .modal-btn.cancel { background: rgba(255, 255, 255, 0.05); color: rgba(210, 220, 255, 0.5); }
        .modal-btn.cancel:hover { background: rgba(255, 255, 255, 0.1); }
        .modal-btn.create { background: linear-gradient(135deg, #f472b6, #fb923c); color: white; }
        .modal-btn.create:hover { transform: scale(1.02); box-shadow: 0 4px 20px rgba(244, 114, 182, 0.3); }

        .toast-notification {
            position: fixed;
            bottom: 80px;
            left: 50%;
            transform: translateX(-50%);
            background: rgba(244, 114, 182, 0.15);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border: 1px solid rgba(244, 114, 182, 0.2);
            border-radius: 16px;
            padding: 12px 24px;
            color: #e0e7ff;
            font-size: 14px;
            font-weight: 400;
            z-index: 9999;
            opacity: 0;
            transition: opacity 0.3s ease, transform 0.3s ease;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
            max-width: 80%;
            text-align: center;
            pointer-events: none;
        }
        .toast-notification.show { opacity: 1; transform: translateX(-50%) translateY(-10px); }

        @media (max-width: 420px) {
            .screen { padding: 14px 12px 10px; }
            .app-icon { width: 50px; height: 50px; font-size: 20px; }
            .app-grid { gap: 10px 6px; }
            .logo-text { font-size: 17px; }
            .spiral-clock { font-size: 11px; padding: 4px 10px 4px 6px; }
            .gallery-grid { grid-template-columns: repeat(3, 1fr); gap: 8px; }
            .photo-grid { grid-template-columns: repeat(3, 1fr); gap: 6px; }
            .modal-content { padding: 20px; }
            .layers-panel { max-width: 100px; min-width: 80px; font-size: 10px; }
            .editor-toolbar button { font-size: 10px; padding: 3px 6px; }
            .editor-controls label { font-size: 10px; }
            .editor-controls input[type="range"] { width: 40px; }
            .wallpaper-grid { grid-template-columns: repeat(2, 1fr); }
            .store-grid { grid-template-columns: repeat(2, 1fr); }
            .account-menu { min-width: 280px; bottom: 60px; padding: 16px; }
            .app-lock-overlay .lock-keypad { grid-template-columns: repeat(3, 50px); gap: 8px; }
            .app-lock-overlay .lock-key { font-size: 18px; padding: 10px; }
            .app-lock-overlay .lock-input { width: 160px; font-size: 24px; letter-spacing: 6px; }
            .clicker-shop { grid-template-columns: repeat(2, 1fr); }
            .clicker-area .clicker-count { font-size: 32px; }
            .media-viewer .media-viewer-content { max-width: 95%; max-height: 70%; }
            .media-viewer .media-viewer-content video { max-width: 95%; max-height: 70%; }
        }
        @media (max-height: 700px) {
            .app-grid { gap: 8px 6px; margin: 4px 0 8px; }
            .app-icon { width: 44px; height: 44px; font-size: 18px; }
            .app-name { font-size: 10px; }
            .nav-bar { padding: 6px 10px 2px; }
            .status-bar { padding-bottom: 8px; margin-bottom: 6px; font-size: 13px; }
            .aurora-header { margin-bottom: 10px; }
            .gesture-area { margin: 4px 0; padding: 4px 0; }
            .editor-canvas-wrap { min-height: 150px; }
            .editor-bottom { min-height: 80px; }
            .layers-panel { min-width: 70px; max-width: 120px; }
            .editor-toolbar { padding: 4px 6px; }
            .editor-toolbar button { font-size: 10px; padding: 3px 6px; }
            .wallpaper-grid { grid-template-columns: repeat(3, 1fr); }
            .account-menu { bottom: 50px; padding: 14px; min-width: 260px; }
            .account-menu .user-list { max-height: 60px; }
            .clicker-area { min-height: 120px; }
            .clicker-area .clicker-count { font-size: 28px; }
            .clicker-shop { grid-template-columns: repeat(2, 1fr); }
            .media-viewer .media-viewer-content { max-height: 60%; }
            .media-viewer .media-viewer-content video { max-height: 60%; }
        }
    </style>
</head>
<body>

    <div class="screen" id="screen">

        <div class="status-bar">
            <div class="status-left"><i class="fas fa-signal"></i> <i class="fas fa-wifi"></i></div>
            <div style="font-weight: 400; opacity: 0.6;" id="osNameDisplay">POFO</div>
            <div class="status-right" id="statusRight"><i class="fas fa-battery-three-quarters"></i> 86%</div>
        </div>

        <div class="aurora-header">
            <div class="logo-area">
                <span class="logo-icon"><i class="fas fa-gem"></i></span>
                <span class="logo-text" id="logoText">POFO <span class="question-mark">???</span></span>
            </div>
            <div class="spiral-clock" id="musicBtn" onclick="openApp('musicWindow')">
                <i class="fas fa-circle-notch spiral-ring" id="spiralIcon" style="--spiral-rotate: 120deg;"></i>
                <span id="clockDisplay">14:20</span>
                <i class="fas fa-music" style="margin-left:4px;font-size:14px;opacity:0.4;"></i>
            </div>
        </div>

        <div class="app-grid" id="appGrid">
            <div class="app-item" data-app="settings"><div class="app-icon grad-8"><i class="fas fa-cog"></i></div><span class="app-name">Настройки</span></div>
            <div class="app-item" data-app="gallery"><div class="app-icon grad-3"><i class="fas fa-images"></i></div><span class="app-name">Галерея</span></div>
            <div class="app-item" data-app="editor"><div class="app-icon grad-5"><i class="fas fa-wand-magic-sparkles"></i></div><span class="app-name">Монтаж</span></div>
            <div class="app-item" data-app="notes"><div class="app-icon grad-4"><i class="fas fa-pen-fancy"></i></div><span class="app-name">Черновик</span></div>
            <div class="app-item" data-app="music"><div class="app-icon grad-6"><i class="fas fa-music"></i></div><span class="app-name">Музыка</span></div>
            <div class="app-item" data-app="store"><div class="app-icon grad-1"><i class="fas fa-store"></i></div><span class="app-name">POFO Play</span></div>
        </div>

        <div class="app-grid" id="appGrid2" style="display:none;"></div>
        <div class="app-grid" id="appGrid3" style="display:none;"></div>
        <div class="app-grid" id="appGrid4" style="display:none;"></div>
        <div class="app-grid" id="appGrid5" style="display:none;"></div>

        <div class="app-pages" id="appPages">
            <div class="page-dot active" data-page="1" onclick="switchAppPage(1)"></div>
            <div class="page-dot" data-page="2" onclick="switchAppPage(2)"></div>
            <div class="page-dot" data-page="3" onclick="switchAppPage(3)"></div>
            <div class="page-dot" data-page="4" onclick="switchAppPage(4)"></div>
            <div class="page-dot" data-page="5" onclick="switchAppPage(5)"></div>
        </div>

        <div class="gesture-area">
            <div class="gesture-pill" id="gesturePill">
                <i class="fas fa-arrow-up"></i> Смахни вникуда · Тишина
                <i class="fas fa-bell-slash" style="opacity: 0.3;"></i>
            </div>
        </div>

        <div class="compress-demo">
            <span class="compress-dot"></span>
            <span class="compress-dot"></span>
            <span class="compress-dot"></span>
            <span class="compress-dot"></span>
            <span class="compress-dot active"></span>
        </div>

        <div class="nav-bar">
            <div class="nav-item active" onclick="toggleAccountMenu()"><i class="fas fa-house"></i></div>
            <div class="nav-item"><i class="fas fa-square"></i></div>
            <div class="nav-item"><i class="fas fa-compress-alt"></i></div>
            <div class="nav-item" onclick="toggleAccountMenu()"><i class="fas fa-user"></i></div>
        </div>

        <div class="back-tap-hint">
            <i class="fas fa-circle"></i> · дважды коснись задней крышки · <i class="fas fa-circle"></i>
        </div>

        <!-- ===== МЕНЮ АККАУНТОВ ===== -->
        <div class="account-menu" id="accountMenu">
            <div class="account-close" onclick="toggleAccountMenu()"><i class="fas fa-times"></i></div>
            <div class="account-title" id="accountTitle">👤 Войти в аккаунт</div>

            <div id="loginForm">
                <input class="account-input" id="loginUsername" placeholder="Ник аккаунта" autocomplete="off">
                <input class="account-input" id="loginPassword" type="password" placeholder="Пароль">
                <button class="account-btn" onclick="loginAccount()">Войти</button>
                <div class="account-status" id="accountStatus">Введите данные для входа</div>
            </div>

            <div id="profileInfo" style="display:none;">
                <div class="account-status" id="profileDisplay" style="font-size:14px; margin-bottom:8px;"></div>
                <button class="account-logout" onclick="logoutAccount()">Выйти из аккаунта</button>
            </div>

            <div style="margin-top:12px; border-top:1px solid rgba(255,255,255,0.03); padding-top:10px;">
                <input class="account-search" id="userSearch" placeholder="Поиск аккаунтов..." oninput="renderUserList()">
                <div class="user-list" id="userList"></div>
            </div>
        </div>

        <!-- ===== ЗАЩИТА ПРИЛОЖЕНИЙ ===== -->
        <div class="app-lock-overlay" id="appLockOverlay">
            <div class="lock-title">🔒 Вход в приложение</div>
            <div class="lock-sub">Введите пароль для доступа</div>
            <input class="lock-input" id="lockInput" type="text" placeholder="••••" maxlength="4" readonly>
            <div class="lock-keypad">
                <div class="lock-key" onclick="lockKeyPress('1')">1</div>
                <div class="lock-key" onclick="lockKeyPress('2')">2</div>
                <div class="lock-key" onclick="lockKeyPress('3')">3</div>
                <div class="lock-key" onclick="lockKeyPress('4')">4</div>
                <div class="lock-key" onclick="lockKeyPress('5')">5</div>
                <div class="lock-key" onclick="lockKeyPress('6')">6</div>
                <div class="lock-key" onclick="lockKeyPress('7')">7</div>
                <div class="lock-key" onclick="lockKeyPress('8')">8</div>
                <div class="lock-key" onclick="lockKeyPress('9')">9</div>
                <div class="lock-key back" onclick="lockKeyPress('back')"><i class="fas fa-arrow-left"></i></div>
                <div class="lock-key" onclick="lockKeyPress('0')">0</div>
                <div class="lock-key clear" onclick="lockKeyPress('clear')">⌫</div>
            </div>
            <div class="lock-error" id="lockError"></div>
            <button class="lock-btn" onclick="lockConfirm()">Подтвердить</button>
        </div>

        <!-- ===== НАСТРОЙКИ ===== -->
        <div class="app-window" id="settingsWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('settingsWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="settingsTitle">Настройки</div>
                <div class="app-window-close" onclick="closeApp('settingsWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body">
                <div class="settings-list" id="settingsList">
                    <div class="settings-item" data-detail="wifi"><div class="settings-item-icon pink"><i class="fas fa-wifi"></i></div><div class="settings-item-info"><div class="settings-item-title">Wi-Fi</div><div class="settings-item-desc" id="wifiDesc">POFO_Network · Подключено</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="bluetooth"><div class="settings-item-icon blue"><i class="fas fa-bluetooth-b"></i></div><div class="settings-item-info"><div class="settings-item-title">Bluetooth</div><div class="settings-item-desc" id="btDesc">Включено · 2 устройства</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="display"><div class="settings-item-icon green"><i class="fas fa-moon"></i></div><div class="settings-item-info"><div class="settings-item-title">Экран и тема</div><div class="settings-item-desc" id="displayDesc">Тёмная тема · Адаптивная яркость</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="sounds"><div class="settings-item-icon orange"><i class="fas fa-volume-up"></i></div><div class="settings-item-info"><div class="settings-item-title">Звук и вибрация</div><div class="settings-item-desc" id="soundDesc">Звонок 80% · Медиа 60%</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="security"><div class="settings-item-icon purple"><i class="fas fa-lock"></i></div><div class="settings-item-info"><div class="settings-item-title">Безопасность</div><div class="settings-item-desc" id="securityDesc">Защита приложений</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="battery"><div class="settings-item-icon red"><i class="fas fa-battery-three-quarters"></i></div><div class="settings-item-info"><div class="settings-item-title">Аккумулятор</div><div class="settings-item-desc" id="batteryDesc">86% · Режим экономии</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="storage"><div class="settings-item-icon teal"><i class="fas fa-database"></i></div><div class="settings-item-info"><div class="settings-item-title">Хранилище</div><div class="settings-item-desc" id="storageDesc">64.2 ГБ из 128 ГБ</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                    <div class="settings-item" data-detail="about"><div class="settings-item-icon indigo"><i class="fas fa-circle-info"></i></div><div class="settings-item-info"><div class="settings-item-title">О системе</div><div class="settings-item-desc" id="aboutDesc">POFO OS ??? v1 POFO</div></div><div class="settings-item-arrow"><i class="fas fa-chevron-right"></i></div></div>
                </div>

                <!-- Wi-Fi -->
                <div class="settings-detail" id="detail-wifi">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Wi-Fi</div></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'wifi')"><span class="label">Wi-Fi</span><span class="toggle on" id="wifiToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item"><span class="label">Сеть</span><span class="value" id="wifiNetwork">POFO_Network</span></div>
                    <div class="settings-detail-item"><span class="label">Сигнал</span><span class="value" style="color:#34d399;"><i class="fas fa-signal"></i> Отлично</span></div>
                    <div class="settings-detail-item"><span class="label">IP-адрес</span><span class="value">192.168.1.42</span></div>
                    <div class="settings-detail-item" onclick="changeWifiNetwork()"><span class="label">Доступные сети</span><span class="value"><i class="fas fa-chevron-right"></i></span></div>
                </div>

                <!-- Bluetooth -->
                <div class="settings-detail" id="detail-bluetooth">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Bluetooth</div></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'bluetooth')"><span class="label">Bluetooth</span><span class="toggle on" id="btToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item"><span class="label">Название</span><span class="value" id="deviceNameDisplay">POFO Phone</span></div>
                    <div class="settings-detail-item" onclick="toggleBtDevice(this)"><span class="label">Наушники POFO</span><span class="value on" id="btDevice1"><i class="fas fa-check-circle"></i> Подключено</span></div>
                    <div class="settings-detail-item" onclick="toggleBtDevice(this)"><span class="label">POFO Watch</span><span class="value on" id="btDevice2"><i class="fas fa-check-circle"></i> Подключено</span></div>
                    <div class="settings-detail-item"><span class="label">Доступные устройства</span><span class="value"><i class="fas fa-chevron-right"></i></span></div>
                </div>

                <!-- Экран и тема -->
                <div class="settings-detail" id="detail-display">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Экран и тема</div></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'darkTheme')"><span class="label">Тёмная тема</span><span class="toggle on" id="darkThemeToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'brightness')"><span class="label">Адаптивная яркость</span><span class="toggle on" id="brightnessToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item" onclick="cycleAccentColor()"><span class="label">Акцентный цвет</span><span class="value" id="accentColorDisplay" style="color:#f472b6;">● Розовый</span></div>
                    <div class="settings-detail-item" onclick="cycleTextColor()"><span class="label">Цвет текста</span><span class="value" id="textColorDisplay" style="color:#e0e7ff;">● Белый</span></div>
                    <div class="settings-detail-item" onclick="cycleFontSize()"><span class="label">Размер шрифта</span><span class="value" id="fontSizeDisplay">Средний</span></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'spiralOnScreen')"><span class="label">Спираль на экране</span><span class="toggle on" id="spiralToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item"><span class="label">Частота обновления</span><span class="value">120 Гц</span></div>
                </div>

                <!-- Звук и вибрация -->
                <div class="settings-detail" id="detail-sounds">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Звук и вибрация</div></div>
                    <div class="settings-detail-item" onclick="changeVolume(this, 'ring')"><span class="label">Звонок</span><span class="value" id="ringVolume">80%</span></div>
                    <div class="settings-detail-item" onclick="changeVolume(this, 'media')"><span class="label">Медиа</span><span class="value" id="mediaVolume">60%</span></div>
                    <div class="settings-detail-item" onclick="changeVolume(this, 'notifications')"><span class="label">Уведомления</span><span class="value" id="notifVolume">70%</span></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'vibration')"><span class="label">Вибрация</span><span class="toggle on" id="vibrationToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'touchSounds')"><span class="label">Звук нажатий</span><span class="toggle on" id="touchSoundsToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'silentMode')"><span class="label">Режим «Тишина»</span><span class="toggle off" id="silentModeToggle"><i class="fas fa-toggle-off"></i></span></div>
                </div>

                <!-- Безопасность -->
                <div class="settings-detail" id="detail-security">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Безопасность</div></div>
                    <div class="settings-detail-item" onclick="toggleAppLock()">
                        <span class="label">Защита приложений</span>
                        <span class="toggle off" id="appLockToggle"><i class="fas fa-toggle-off"></i></span>
                    </div>
                    <div class="settings-detail-item" id="lockStatusItem" style="display:none;">
                        <span class="label">Статус</span>
                        <span class="value on" style="color:#34d399;">🔒 Защита активна</span>
                    </div>
                    <div class="settings-detail-item" onclick="changeLockPassword()" id="changePassItem" style="display:none;">
                        <span class="label">Изменить пароль</span>
                        <span class="value"><i class="fas fa-chevron-right"></i></span>
                    </div>
                    <div class="settings-detail-item" onclick="disableLockWithPassword()" id="disableLockItem" style="display:none;">
                        <span class="label">Отключить защиту</span>
                        <span class="value"><i class="fas fa-chevron-right"></i></span>
                    </div>
                </div>

                <!-- Аккумулятор -->
                <div class="settings-detail" id="detail-battery">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Аккумулятор</div></div>
                    <div class="settings-detail-item" onclick="changeBatteryLevel()"><span class="label">Заряд</span><span class="value" id="batteryLevel" style="color:#34d399;">86%</span></div>
                    <div class="settings-detail-item" onclick="toggleSwitch(this, 'batterySaver')"><span class="label">Режим экономии</span><span class="toggle on" id="batterySaverToggle"><i class="fas fa-toggle-on"></i></span></div>
                    <div class="settings-detail-item"><span class="label">Время работы</span><span class="value" id="batteryLife">~18 ч</span></div>
                    <div class="settings-detail-item" onclick="toggleFastCharge()"><span class="label">Быстрая зарядка</span><span class="value on" id="fastChargeStatus"><i class="fas fa-check-circle"></i> Активна</span></div>
                    <div class="settings-detail-item"><span class="label">Использование приложений</span><span class="value"><i class="fas fa-chevron-right"></i></span></div>
                </div>

                <!-- Хранилище -->
                <div class="settings-detail" id="detail-storage">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">Хранилище</div></div>
                    <div class="settings-detail-item"><span class="label">Всего</span><span class="value">128 ГБ</span></div>
                    <div class="settings-detail-item" onclick="changeStorage()"><span class="label">Использовано</span><span class="value" id="storageUsed">64.2 ГБ</span></div>
                    <div class="settings-detail-item"><span class="label">Свободно</span><span class="value" id="storageFree" style="color:#34d399;">63.8 ГБ</span></div>
                    <div class="settings-detail-item"><span class="label">Приложения</span><span class="value">28.4 ГБ</span></div>
                    <div class="settings-detail-item"><span class="label">Фото и видео</span><span class="value">22.1 ГБ</span></div>
                    <div class="settings-detail-item"><span class="label">Система</span><span class="value">13.7 ГБ</span></div>
                </div>

                <!-- О системе -->
                <div class="settings-detail" id="detail-about">
                    <div class="settings-detail-header"><div class="settings-detail-back" onclick="closeDetail()"><i class="fas fa-arrow-left"></i></div><div class="settings-detail-title">О системе</div></div>
                    <div class="settings-detail-item" onclick="editOSName()"><span class="label">Название ОС</span><span class="value" id="osNameValue">POFO OS ???</span></div>
                    <div class="settings-detail-item" onclick="editDeviceName()"><span class="label">Название устройства</span><span class="value" id="deviceNameValue">POFO Phone</span></div>
                    <div class="settings-detail-item" onclick="editAppName()"><span class="label">Название приложений</span><span class="value" id="appNameValue">POFO</span></div>
                    <div class="settings-detail-item"><span class="label">Версия</span><span class="value">v1 POFO</span></div>
                    <div class="settings-detail-item"><span class="label">Ядро</span><span class="value">SeL4</span></div>
                    <div class="settings-detail-item"><span class="label">Девиз</span><span class="value" style="color:#f472b6;">«Система, которая дышит»</span></div>
                    <div class="settings-detail-item" onclick="checkUpdates()"><span class="label">Обновления</span><span class="value" id="updateStatus" style="color:#34d399;"><i class="fas fa-check-circle"></i> Доступны</span></div>
                    <div class="settings-detail-item"><span class="label">Сборка</span><span class="value">POFO-2026.09</span></div>
                    <div style="margin-top:12px; padding-top:12px; border-top:1px solid rgba(255,255,255,0.05);">
                        <div style="display:flex; align-items:center; gap:12px; margin-bottom:8px;">
                            <span style="font-weight:600; font-size:15px; color:rgba(210,220,255,0.7);">🔑 ROOT</span>
                            <span class="root-status off" id="rootStatus">Выкл</span>
                        </div>
                        <div id="rootInputArea" style="display:flex; gap:8px;">
                            <input class="root-password-input" id="rootPasswordInput" type="password" placeholder="Введите пароль..." onkeydown="if(event.key==='Enter'){toggleRoot();}">
                            <button class="root-btn" onclick="toggleRoot()">Активировать</button>
                        </div>
                        <div id="rootActions" style="display:none; margin-top:8px;">
                            <button class="root-btn" onclick="toggleRoot()">Отключить ROOT</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== ГАЛЕРЕЯ ===== -->
        <div class="app-window" id="galleryWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('galleryWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="galleryTitle">Галерея</div>
                <div class="app-window-close" onclick="closeApp('galleryWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body" id="galleryBody">
                <div class="gallery-grid" id="galleryGrid">
                    <div class="gallery-item" onclick="openGallerySection('all')"><span class="gallery-icon"><i class="fas fa-photo-film"></i></span><div class="gallery-name">Все фото</div><div class="gallery-count" id="allCount">0 фото</div></div>
                    <div class="gallery-item" onclick="openGallerySection('camera')"><span class="gallery-icon"><i class="fas fa-camera"></i></span><div class="gallery-name">Сделать фото</div><div class="gallery-count">📸 Снимок</div></div>
                    <div class="gallery-item" onclick="openGallerySection('my')"><span class="gallery-icon"><i class="fas fa-user"></i></span><div class="gallery-name">Мои фото</div><div class="gallery-count" id="myCount">0 фото</div></div>
                </div>
                <div id="gallerySection" style="display:none;">
                    <div class="gallery-header-actions">
                        <button onclick="backToGallery()"><i class="fas fa-arrow-left"></i> Назад</button>
                        <button id="galleryAddBtn" onclick="addPhoto()" style="display:none;"><i class="fas fa-plus"></i> Добавить</button>
                        <button id="galleryCameraBtn" onclick="openCamera()" style="display:none;"><i class="fas fa-camera"></i> Снять</button>
                    </div>
                    <div class="photo-grid" id="photoGrid"></div>
                </div>
            </div>
        </div>

        <!-- ===== МЕДИА-ПРОСМОТРЩИК ===== -->
        <div class="media-viewer" id="mediaViewer">
            <div class="media-viewer-close" onclick="closeMediaViewer()"><i class="fas fa-times"></i></div>
            <div class="media-viewer-content" id="mediaViewerContent"></div>
            <div class="media-viewer-info" id="mediaViewerInfo"></div>
        </div>

        <!-- ===== МОНТАЖ ===== -->
        <div class="app-window" id="editorWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('editorWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="editorTitle">Монтаж</div>
                <div class="app-window-close" onclick="closeApp('editorWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body">
                <div class="editor-container">
                    <div class="editor-canvas-wrap" id="editorCanvasWrap" onclick="selectLayerOnCanvas(event)">
                        <div class="editor-placeholder" id="editorPlaceholder"><i class="fas fa-image"></i>Загрузите фото для редактирования</div>
                        <canvas id="editorCanvas"></canvas>
                    </div>
                    <div class="editor-bottom">
                        <div class="editor-toolbar-wrap">
                            <div class="editor-toolbar">
                                <button onclick="editorLoadImage()"><i class="fas fa-folder-open"></i> Загрузить</button>
                                <button onclick="editorAddText()"><i class="fas fa-font"></i> Текст</button>
                                <button onclick="editorAddEmoji()"><i class="fas fa-face-smile"></i> Эмодзи</button>
                                <button onclick="editorAddImage()"><i class="fas fa-image"></i> Фото</button>
                                <button onclick="editorExport()"><i class="fas fa-download"></i> Export</button>
                            </div>
                            <div class="editor-controls">
                                <div class="filter-chips">
                                    <span class="filter-chip active" onclick="applyFilter('none')">Нет</span>
                                    <span class="filter-chip" onclick="applyFilter('grayscale')">Ч/Б</span>
                                    <span class="filter-chip" onclick="applyFilter('invert')">Инверсия</span>
                                    <span class="filter-chip" onclick="applyFilter('sepia')">Сепия</span>
                                    <span class="filter-chip" onclick="applyFilter('brightness')">Яркость</span>
                                </div>
                                <label>Яркость <input type="range" id="brightnessSlider" min="0" max="200" value="100" oninput="updateBrightness()"></label>
                                <label>Контраст <input type="range" id="contrastSlider" min="0" max="200" value="100" oninput="updateContrast()"></label>
                            </div>
                        </div>
                        <div class="layers-panel" id="layersPanel">
                            <div class="layers-title">📋 Слои</div>
                            <div id="layersList"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== ЧЕРНОВИК ===== -->
        <div class="app-window" id="notesWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('notesWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="notesTitle">Черновик</div>
                <div class="app-window-close" onclick="closeApp('notesWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body">
                <div class="notes-header">
                    <input class="notes-search" id="notesSearch" placeholder="Поиск заметок..." oninput="filterNotes()">
                    <button class="notes-create-btn" onclick="openCreateModal()"><i class="fas fa-plus"></i> Создать</button>
                </div>
                <div class="notes-list" id="notesList"><div class="note-empty">Нет заметок. Нажмите «Создать»</div></div>
            </div>
        </div>

        <div class="note-viewer" id="noteViewer">
            <div class="note-viewer-header">
                <div class="note-viewer-back" onclick="closeNoteViewer()"><i class="fas fa-arrow-left"></i></div>
                <div class="note-viewer-title" id="noteViewerTitle">Заметка</div>
                <div class="note-viewer-delete" onclick="deleteNote()"><i class="fas fa-trash"></i></div>
            </div>
            <textarea id="noteViewerContent" placeholder="Введите текст заметки..." oninput="saveNoteContent()"></textarea>
        </div>

        <div class="create-note-modal" id="createModal">
            <div class="modal-content">
                <div class="modal-title">📝 Создать заметку</div>
                <label class="modal-label">Название</label>
                <input id="noteTitleInput" placeholder="Введите название..." maxlength="50">
                <div class="modal-actions">
                    <button class="modal-btn cancel" onclick="closeCreateModal()">Отмена</button>
                    <button class="modal-btn create" onclick="createNote()">Создать</button>
                </div>
            </div>
        </div>

        <!-- ===== МУЗЫКА ===== -->
        <div class="app-window" id="musicWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('musicWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="musicTitle">Музыка</div>
                <div class="app-window-close" onclick="closeApp('musicWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body">
                <div class="music-grid" id="musicGrid">
                    <div class="music-upload-btn" onclick="uploadMusic()">
                        <i class="fas fa-cloud-upload-alt"></i>
                        Загрузить музыку<br>
                        <span style="font-size:10px;opacity:0.5;">MP3, WAV, AAC</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== POFO PLAY ===== -->
        <div class="app-window" id="storeWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('storeWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="storeTitle">POFO Play</div>
                <div class="app-window-close" onclick="closeApp('storeWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body">
                <div style="margin-bottom:12px; color:rgba(210,220,255,0.3); font-size:13px;"><i class="fas fa-store"></i> Магазин приложений</div>
                <div class="store-grid" id="storeGrid">
                    <div class="store-app" onclick="installApp('wallpapers')">
                        <span class="store-app-icon"><i class="fas fa-image"></i></span>
                        <div class="store-app-name">Обои</div>
                        <div class="store-app-desc">Установите новые обои</div>
                        <button class="store-app-btn" id="installBtn_wallpapers">Установить</button>
                    </div>
                    <div class="store-app" onclick="installApp('clicker')">
                        <span class="store-app-icon"><i class="fas fa-hand-pointer"></i></span>
                        <div class="store-app-name">Кликер</div>
                        <div class="store-app-desc">Кликайте и зарабатывайте</div>
                        <button class="store-app-btn" id="installBtn_clicker">Установить</button>
                    </div>
                </div>
                <div id="appPage" style="display:none; margin-top:12px;">
                    <button onclick="backToStore()" style="background:transparent; border:none; color:rgba(210,220,255,0.4); font-size:14px; cursor:pointer; margin-bottom:12px;"><i class="fas fa-arrow-left"></i> Назад</button>
                    <div id="appPageContent"></div>
                </div>
            </div>
        </div>

        <!-- ===== КЛИКЕР ===== -->
        <div class="app-window" id="clickerWindow">
            <div class="app-window-header">
                <div class="app-window-back" onclick="closeApp('clickerWindow')"><i class="fas fa-arrow-left"></i></div>
                <div class="app-window-title" id="clickerTitle">Кликер</div>
                <div class="app-window-close" onclick="closeApp('clickerWindow')"><i class="fas fa-times"></i></div>
            </div>
            <div class="app-window-body">
                <div class="clicker-container" id="clickerContainer">
                    <div class="clicker-header">
                        <div class="clicker-coins">💰 <span id="clickerCoins">0</span></div>
                        <div class="clicker-stats">Кликов: <span id="clickerTotalClicks">0</span> · За клик: <span id="clickerPerClick">1</span></div>
                    </div>

                    <div class="clicker-mode-switch">
                        <button class="active" id="clickerModeNormal" onclick="switchClickerMode('normal')">Обычный</button>
                        <button id="clickerModeReward" onclick="switchClickerMode('reward')">Получение</button>
                    </div>

                    <div class="clicker-area" id="clickerArea">
                        <div class="clicker-big"><i class="fas fa-hand-pointer"></i></div>
                        <div class="clicker-count" id="clickerDisplay">0</div>
                        <div class="clicker-per-click">+<span id="clickerPerClickDisplay">1</span> за клик</div>
                    </div>

                    <div class="clicker-shop" id="clickerShop">
                        <div class="shop-item" onclick="buyUpgrade('click1')">
                            <div class="shop-name">+1 клик</div>
                            <div class="shop-cost">💰 25 кликов</div>
                            <button class="shop-btn" id="upgrade_click1">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('click5')">
                            <div class="shop-name">+5 кликов</div>
                            <div class="shop-cost">💰 100 кликов</div>
                            <button class="shop-btn" id="upgrade_click5">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('autoclicker')">
                            <div class="shop-name">Автокликер</div>
                            <div class="shop-cost">💰 250 кликов</div>
                            <button class="shop-btn" id="upgrade_autoclicker">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('click10')">
                            <div class="shop-name">+10 кликов</div>
                            <div class="shop-cost">💰 500 кликов</div>
                            <button class="shop-btn" id="upgrade_click10">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('click50')">
                            <div class="shop-name">+50 кликов</div>
                            <div class="shop-cost">💰 2000 кликов</div>
                            <button class="shop-btn" id="upgrade_click50">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('click100')">
                            <div class="shop-name">+100 кликов</div>
                            <div class="shop-cost">💰 5000 кликов</div>
                            <button class="shop-btn" id="upgrade_click100">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('autoclicker2')">
                            <div class="shop-name">Автокликер v2</div>
                            <div class="shop-cost">💰 10000 кликов</div>
                            <button class="shop-btn" id="upgrade_autoclicker2">Купить</button>
                        </div>
                        <div class="shop-item" onclick="buyUpgrade('click500')">
                            <div class="shop-name">+500 кликов</div>
                            <div class="shop-cost">💰 25000 кликов</div>
                            <button class="shop-btn" id="upgrade_click500">Купить</button>
                        </div>
                    </div>

                    <div class="clicker-reward" id="clickerReward" style="display:none;">
                        <div class="reward-text">🎉 Ты получил 100 POFO Coin!</div>
                        <div class="reward-sub">Нажми "Получить", чтобы забрать награду</div>
                        <button class="reward-btn" id="rewardClaimBtn" onclick="claimReward()">Получить</button>
                    </div>
                </div>
            </div>
        </div>

        <!-- ===== УСТАНОВКА ===== -->
        <div class="install-overlay" id="installOverlay">
            <div class="spinner"></div>
            <div class="install-text">Установка приложения...</div>
        </div>

        <!-- ===== МОДАЛ ===== -->
        <div class="modal-overlay" id="modalOverlay">
            <div class="modal-content">
                <div class="modal-title" id="modalTitle">Действие</div>
                <label class="modal-label" id="modalLabel">Введите значение</label>
                <input class="modal-input" id="modalInput" placeholder="...">
                <div class="modal-actions">
                    <button class="modal-btn cancel" onclick="closeModal()">Отмена</button>
                    <button class="modal-btn create" id="modalConfirmBtn" onclick="confirmModal()">Подтвердить</button>
                </div>
            </div>
        </div>

    </div>

    <script>
        (function() {
            // ===== АККАУНТЫ =====
            const users = [
                { username: 'Danpro', password: '666sigma', role: 'Владелец' },
                { username: 'Plesen', password: 'K$U#R@V(+A2281488', role: 'Админ' },
                { username: 'Artem', password: 'fp333_12', role: 'Админ' }
            ];
            let currentUser = null;
            let accountMenuOpen = false;
            let ownerPrivileges = {
                canAccessAnyAccount: false,
                infiniteClicker: false,
                ownerPanelEnabled: false
            };

            // ===== ЗАЩИТА ПРИЛОЖЕНИЙ =====
            let appLockEnabled = false;
            let appLockPassword = '1234';
            let pendingApp = null;
            let lockInputValue = '';

            // ===== ДАННЫЕ =====
            let allPhotos = [];
            let myPhotos = [];
            let cameraPhotos = [];
            let photoIdCounter = 0;
            let currentSection = '';
            let musicFiles = [];
            let noteIdCounter = 0;
            let notes = [];
            let currentNoteId = null;
            let rootEnabled = false;
            let currentWallpaper = null;
            let installedApps = [];
            let currentAppPage = 1;

            // ===== КЛИКЕР =====
            let clickerCoins = 0;
            let clickerTotalClicks = 0;
            let clickerPerClick = 1;
            let clickerMode = 'normal';
            let clickerRewardMode = {
                available: true,
                clicksToday: 0,
                maxClicks: 100,
                lastClaimDate: null,
                claimed: false
            };
            let clickerUpgrades = {
                click1: false,
                click5: false,
                click10: false,
                click50: false,
                click100: false,
                click500: false,
                autoclicker: false,
                autoclicker2: false
            };
            let autoclickerInterval = null;

            // ===== РЕДАКТОР =====
            let editorImage = null;
            let editorCanvas = null;
            let editorCtx = null;
            let editorFilter = 'none';
            let editorBrightness = 100;
            let editorContrast = 100;
            let editorLayers = [];
            let selectedLayerIndex = -1;
            let isDragging = false;
            let dragLayerIndex = -1;
            let dragStartX = 0,
                dragStartY = 0;

            // ===== ВРЕМЯ =====
            const clockEl = document.getElementById('clockDisplay');
            const spiral = document.getElementById('spiralIcon');
            let spiralVisible = true;
            let osName = 'POFO OS ???';
            let deviceName = 'POFO Phone';
            let appPrefix = 'POFO';

            function randomTime() {
                const h = String(Math.floor(Math.random() * 24)).padStart(2, '0');
                const m = String(Math.floor(Math.random() * 60)).padStart(2, '0');
                return h + ':' + m;
            }

            function setRandomSpiral() {
                if (!spiralVisible) return;
                const deg = Math.floor(Math.random() * 360);
                spiral.style.setProperty('--spiral-rotate', deg + 'deg');
            }
            clockEl.textContent = randomTime();
            setRandomSpiral();

            // ===== МЕНЮ ПРИЛОЖЕНИЙ =====
            function switchAppPage(page) {
                currentAppPage = page;
                document.querySelectorAll('.app-grid').forEach(el => el.style.display = 'none');
                const target = document.getElementById('appGrid' + (page === 1 ? '' : page));
                if (target) target.style.display = 'grid';
                document.querySelectorAll('.page-dot').forEach(dot => {
                    dot.classList.toggle('active', parseInt(dot.dataset.page) === page);
                });
            }

            function addAppToPage(appId, name, icon, grad, page) {
                const gridId = page === 1 ? 'appGrid' : 'appGrid' + page;
                const grid = document.getElementById(gridId);
                if (!grid) return;
                if (grid.querySelector('.app-item[data-app="' + appId + '"]')) return;

                const item = document.createElement('div');
                item.className = 'app-item';
                item.dataset.app = appId;
                item.innerHTML =
                    `<div class="app-icon ${grad}"><i class="fas ${icon}"></i></div><span class="app-name">${name}</span>`;
                grid.appendChild(item);

                item.addEventListener('click', function() {
                    const app = this.dataset.app;
                    if (app === 'wallpapers') {
                        openApp('storeWindow');
                        setTimeout(() => { openAppPage('wallpapers'); }, 300);
                    } else if (app === 'clicker') {
                        openAppWithLock('clickerWindow', 'Кликер');
                    }
                });
            }

            // ===== МЕНЮ АККАУНТОВ =====
            window.toggleAccountMenu = function() {
                accountMenuOpen = !accountMenuOpen;
                const menu = document.getElementById('accountMenu');
                if (accountMenuOpen) {
                    menu.classList.add('open');
                    renderUserList();
                    if (currentUser) {
                        document.getElementById('loginForm').style.display = 'none';
                        document.getElementById('profileInfo').style.display = 'block';
                        document.getElementById('profileDisplay').innerHTML =
                            `👤 <strong>${currentUser.username}</strong> · <span class="role">${currentUser.role}</span>`;
                        document.getElementById('accountTitle').textContent = '👤 Аккаунт';
                    } else {
                        document.getElementById('loginForm').style.display = 'block';
                        document.getElementById('profileInfo').style.display = 'none';
                        document.getElementById('accountTitle').textContent = '👤 Войти в аккаунт';
                        document.getElementById('accountStatus').textContent = 'Введите данные для входа';
                    }
                    updateRoleApps();
                } else {
                    menu.classList.remove('open');
                }
            };

            window.loginAccount = function() {
                const username = document.getElementById('loginUsername').value.trim();
                const password = document.getElementById('loginPassword').value.trim();
                const status = document.getElementById('accountStatus');

                if (!username || !password) {
                    status.textContent = '❌ Заполните все поля';
                    return;
                }

                if (currentUser && currentUser.role === 'Владелец' && ownerPrivileges.canAccessAnyAccount) {
                    const targetUser = users.find(u => u.username === username);
                    if (targetUser) {
                        currentUser = targetUser;
                        status.textContent = '✅ Вход выполнен как ' + currentUser.username + ' (владелец)';
                        status.style.color = '#fbbf24';
                        document.getElementById('loginForm').style.display = 'none';
                        document.getElementById('profileInfo').style.display = 'block';
                        document.getElementById('profileDisplay').innerHTML =
                            `👤 <strong>${currentUser.username}</strong> · <span class="role">${currentUser.role}</span> (👑 владелец)`;
                        document.getElementById('accountTitle').textContent = '👤 Аккаунт';
                        showToast('👑 Вход на аккаунт ' + currentUser.username);
                        renderUserList();
                        updateRoleApps();
                        return;
                    }
                }

                const user = users.find(u => u.username === username && u.password === password);
                if (user) {
                    currentUser = user;
                    status.textContent = '✅ Вход выполнен!';
                    status.style.color = '#34d399';
                    document.getElementById('loginForm').style.display = 'none';
                    document.getElementById('profileInfo').style.display = 'block';
                    document.getElementById('profileDisplay').innerHTML =
                        `👤 <strong>${currentUser.username}</strong> · <span class="role">${currentUser.role}</span>`;
                    document.getElementById('accountTitle').textContent = '👤 Аккаунт';
                    showToast('✅ Вход выполнен как ' + currentUser.username);
                    renderUserList();
                    updateRoleApps();
                } else {
                    status.textContent = '❌ Неверный логин или пароль';
                    status.style.color = '#ef4444';
                }
            };

            window.logoutAccount = function() {
                currentUser = null;
                document.getElementById('loginForm').style.display = 'block';
                document.getElementById('profileInfo').style.display = 'none';
                document.getElementById('accountTitle').textContent = '👤 Войти в аккаунт';
                document.getElementById('accountStatus').textContent = 'Введите данные для входа';
                document.getElementById('accountStatus').style.color = 'rgba(210,220,255,0.4)';
                document.getElementById('loginUsername').value = '';
                document.getElementById('loginPassword').value = '';
                showToast('🔒 Выход выполнен');
                renderUserList();
                updateRoleApps();
            };

            window.renderUserList = function() {
                const search = document.getElementById('userSearch').value.toLowerCase();
                const list = document.getElementById('userList');
                let filtered = users;
                if (search) {
                    filtered = users.filter(u => u.username.toLowerCase().includes(search));
                }
                if (filtered.length === 0) {
                    list.innerHTML = '<div style="color:rgba(210,220,255,0.15);font-size:12px;text-align:center;padding:8px 0;">Пользователи не найдены</div>';
                    return;
                }
                list.innerHTML = filtered.map(u => `
                        <div class="user-item">
                            <span>${u.username} ${currentUser && currentUser.username === u.username ? '⭐' : ''}</span>
                            <span class="user-role ${u.role === 'Владелец' ? 'owner' : u.role === 'Админ' ? 'admin' : 'user'}">${u.role}</span>
                        </div>
                    `).join('');
            };

            // ===== РОЛЕВЫЕ ПРИЛОЖЕНИЯ =====
            function updateRoleApps() {
                document.querySelectorAll('.app-item[data-app="adminPanel"], .app-item[data-app="ownerPanel"]').forEach(el =>
                    el.remove());

                if (!currentUser) return;

                let targetGrid = document.getElementById('appGrid');

                if (currentUser.role === 'Админ') {
                    const item = document.createElement('div');
                    item.className = 'app-item';
                    item.dataset.app = 'adminPanel';
                    item.innerHTML =
                        `<div class="app-icon grad-admin"><i class="fas fa-user-shield"></i></div><span class="app-name">Админ-панель</span>`;
                    item.addEventListener('click', function() { openAdminPanel(); });
                    targetGrid.appendChild(item);
                }

                if (currentUser.role === 'Владелец') {
                    const item = document.createElement('div');
                    item.className = 'app-item';
                    item.dataset.app = 'ownerPanel';
                    item.innerHTML =
                        `<div class="app-icon grad-owner"><i class="fas fa-crown"></i></div><span class="app-name">Мега-панель</span>`;
                    item.addEventListener('click', function() { openOwnerPanel(); });
                    targetGrid.appendChild(item);
                }
            }

            // ===== АДМИН-ПАНЕЛЬ =====
            function openAdminPanel() {
                if (!currentUser || currentUser.role !== 'Админ') { showToast('❌ Доступ запрещён'); return; }
                openModal('👑 Админ-панель', 'Выберите действие:\n1 - Админ-абьюз\n2 - Перезагрузка\n3 - Статистика\n4 - Заглушить всех\n5 - Рассылка', '',
                    function(value) {
                        if (value === '1') {
                            showToast('💥 Админ-абьюз активирован! Все пользователи получили уведомление.');
                        } else if (value === '2') {
                            showToast('🔄 Система перезагружена (симуляция)');
                        } else if (value === '3') {
                            showToast('📊 Статистика: 42 пользователя онлайн');
                        } else if (value === '4') {
                            showToast('🔇 Все пользователи заглушены на 5 минут');
                        } else if (value === '5') {
                            showToast('🎉 Разослано праздничное сообщение всем!');
                        } else {
                            showToast('❌ Неизвестная команда');
                        }
                    });
                document.getElementById('modalInput').placeholder = 'Введите номер команды...';
            }

            // ===== МЕГА-ПАНЕЛЬ ВЛАДЕЛЬЦА =====
            function openOwnerPanel() {
                if (!currentUser || currentUser.role !== 'Владелец') { showToast('❌ Доступ запрещён'); return; }

                const panel = document.createElement('div');
                panel.style.cssText =
                    'position:absolute;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.85);backdrop-filter:blur(20px);z-index:600;display:flex;flex-direction:column;padding:30px;overflow-y:auto;';
                panel.id = 'ownerPanel';

                const adminCommands = [
                    { id: 'admin_abuse', label: 'Админ-абьюз', desc: 'Активировать админ-абьюз' },
                    { id: 'admin_reboot', label: 'Перезагрузка', desc: 'Перезагрузить систему' },
                    { id: 'admin_stats', label: 'Статистика', desc: 'Показать статистику' },
                    { id: 'admin_mute', label: 'Заглушить всех', desc: 'Заглушить пользователей' },
                    { id: 'admin_broadcast', label: 'Рассылкa', desc: 'Разослать сообщение' }
                ];

                const ownerSettings = [
                    { id: 'dev_mode', label: 'Режим разработчика', default: false },
                    { id: 'debug_mode', label: 'Отладка', default: false },
                    { id: 'super_user', label: 'Супер-пользователь', default: true },
                    { id: 'user_management', label: 'Управление пользователями', default: true },
                    { id: 'system_logs', label: 'Логи системы', default: false },
                    { id: 'auto_updates', label: 'Авто-обновления', default: true },
                    { id: 'security_enhanced', label: 'Безопасность', default: true },
                    { id: 'data_compression', label: 'Сжатие данных', default: false },
                    { id: 'pofo_theme', label: 'Тема POFO', default: true },
                    { id: 'export_settings', label: 'Экспорт настроек', default: false },
                    { id: 'factory_reset', label: 'Полный сброс', default: false },
                    { id: 'ai_assistant', label: 'ИИ-ассистент', default: true },
                    { id: 'root_access', label: 'ROOT-доступ', default: true },
                    { id: 'account_switch', label: 'Вход на чужие аккаунты', default: false },
                    { id: 'infinite_clicker', label: 'Бесконечный кликер', default: false }
                ];

                panel.innerHTML = `
                        <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:20px;">
                            <h2 style="color:#fbbf24;font-size:24px;">👑 Мега-панель владельца</h2>
                            <button onclick="this.closest('#ownerPanel').remove()" style="background:transparent;border:none;color:rgba(210,220,255,0.4);font-size:24px;cursor:pointer;">✕</button>
                        </div>
                        <div style="margin-bottom:16px;">
                            <h3 style="color:rgba(210,220,255,0.4);font-size:13px;font-weight:500;margin-bottom:8px;">⚡ Админ-команды</h3>
                            <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(180px,1fr));gap:8px;">
                                ${adminCommands.map(cmd => `
                                    <div style="background:rgba(255,255,255,0.02);border-radius:12px;padding:12px;border:1px solid rgba(255,255,255,0.03);cursor:pointer;" onclick="executeAdminCommand('${cmd.id}')">
                                        <div style="color:#e0e7ff;font-size:13px;font-weight:500;">${cmd.label}</div>
                                        <div style="color:rgba(210,220,255,0.2);font-size:11px;margin-top:2px;">${cmd.desc}</div>
                                    </div>
                                `).join('')}
                            </div>
                        </div>
                        <div style="margin-bottom:16px;">
                            <h3 style="color:rgba(210,220,255,0.4);font-size:13px;font-weight:500;margin-bottom:8px;">🔧 Настройки владельца</h3>
                            <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:8px;">
                                ${ownerSettings.map(setting => `
                                    <div style="background:rgba(255,255,255,0.02);border-radius:12px;padding:12px;border:1px solid rgba(255,255,255,0.03);">
                                        <div style="display:flex;justify-content:space-between;align-items:center;">
                                            <span style="color:rgba(210,220,255,0.6);font-size:12px;">${setting.label}</span>
                                            <span class="toggle ${setting.default ? 'on' : 'off'}" onclick="toggleOwnerSetting('${setting.id}')" style="color:#fbbf24;font-size:22px;cursor:pointer;">
                                                <i class="fas fa-toggle-${setting.default ? 'on' : 'off'}"></i>
                                            </span>
                                        </div>
                                    </div>
                                `).join('')}
                            </div>
                        </div>
                        <div style="padding:12px;background:rgba(255,255,255,0.02);border-radius:12px;border:1px solid rgba(255,255,255,0.03);text-align:center;">
                            <div style="color:rgba(210,220,255,0.2);font-size:11px;">⚡ Полное управление системой доступно только владельцу</div>
                        </div>
                    `;

                document.body.appendChild(panel);

                setTimeout(() => {
                    document.querySelectorAll('#ownerPanel .toggle').forEach(el => {
                        const id = el.closest('div').querySelector('span')?.textContent?.trim();
                        const setting = ownerSettings.find(s => s.label === id);
                        if (setting) {
                            const state = ownerPrivileges[setting.id] !== undefined ? ownerPrivileges[setting
                                .id] : setting.default;
                            if (state) {
                                el.classList.remove('off');
                                el.classList.add('on');
                                el.innerHTML = '<i class="fas fa-toggle-on"></i>';
                            } else {
                                el.classList.remove('on');
                                el.classList.add('off');
                                el.innerHTML = '<i class="fas fa-toggle-off"></i>';
                            }
                        }
                    });
                }, 100);

                showToast('👑 Мега-панель открыта');
            }

            window.executeAdminCommand = function(cmd) {
                switch (cmd) {
                    case 'admin_abuse':
                        showToast('💥 Админ-абьюз активирован! Все пользователи получили уведомление.');
                        break;
                    case 'admin_reboot':
                        showToast('🔄 Система перезагружена (симуляция)');
                        break;
                    case 'admin_stats':
                        showToast('📊 Статистика: 42 пользователя онлайн');
                        break;
                    case 'admin_mute':
                        showToast('🔇 Все пользователи заглушены на 5 минут');
                        break;
                    case 'admin_broadcast':
                        showToast('🎉 Разослано праздничное сообщение всем!');
                        break;
                    default:
                        showToast('❌ Неизвестная команда');
                }
            };

            window.toggleOwnerSetting = function(id) {
                const toggle = event.target.closest('.toggle');
                if (!toggle) return;
                const isOn = toggle.classList.contains('on');
                if (isOn) {
                    toggle.classList.remove('on');
                    toggle.classList.add('off');
                    toggle.innerHTML = '<i class="fas fa-toggle-off"></i>';
                    ownerPrivileges[id] = false;
                } else {
                    toggle.classList.remove('off');
                    toggle.classList.add('on');
                    toggle.innerHTML = '<i class="fas fa-toggle-on"></i>';
                    ownerPrivileges[id] = true;
                }
                showToast(id + (ownerPrivileges[id] ? ' ✅ включено' : ' ❌ выключено'));

                if (id === 'account_switch' && ownerPrivileges[id]) {
                    showToast('👑 Теперь вы можете входить на чужие аккаунты без пароля');
                }
                if (id === 'infinite_clicker' && ownerPrivileges[id]) {
                    showToast('♾️ Бесконечный кликер активирован для владельца');
                    updateClickerUI();
                }
            };

            // ===== ROOT =====
            function toggleRoot() {
                const input = document.getElementById('rootPasswordInput');
                const status = document.getElementById('rootStatus');
                const inputArea = document.getElementById('rootInputArea');
                const actions = document.getElementById('rootActions');

                if (!rootEnabled) {
                    if (input.value === 'POFO_root') {
                        rootEnabled = true;
                        status.textContent = 'Вкл';
                        status.className = 'root-status on';
                        inputArea.style.display = 'none';
                        actions.style.display = 'block';
                        showToast('✅ ROOT активирован');
                        updateRootUI();
                    } else {
                        showToast('❌ Неверный пароль');
                        input.value = '';
                        input.focus();
                    }
                } else {
                    rootEnabled = false;
                    status.textContent = 'Выкл';
                    status.className = 'root-status off';
                    inputArea.style.display = 'flex';
                    actions.style.display = 'none';
                    input.value = '';
                    showToast('🔒 ROOT отключён');
                }
            }

            function updateRootUI() {
                if (rootEnabled) {
                    document.querySelectorAll('.settings-detail-item .value').forEach(el => {
                        if (el.id && (el.id === 'osNameValue' || el.id === 'deviceNameValue' || el.id ===
                                'appNameValue')) {
                            el.style.cursor = 'pointer';
                            el.style.color = '#f472b6';
                        }
                    });
                }
            }

            window.editOSName = function() {
                if (!rootEnabled) { showToast('❌ Требуется ROOT доступ'); return; }
                openModal('Изменение названия ОС', 'Введите новое название', osName, function(value) {
                    if (value.trim()) {
                        osName = value.trim();
                        document.getElementById('osNameValue').textContent = osName;
                        document.getElementById('aboutDesc').textContent = osName + ' v1 POFO';
                        document.getElementById('logoText').innerHTML = osName;
                        document.getElementById('osNameDisplay').textContent = osName.split(' ')[0] || 'POFO';
                        showToast('✅ Название ОС изменено');
                    }
                });
            };

            window.editDeviceName = function() {
                if (!rootEnabled) { showToast('❌ Требуется ROOT доступ'); return; }
                openModal('Изменение названия устройства', 'Введите новое название', deviceName, function(value) {
                    if (value.trim()) {
                        deviceName = value.trim();
                        document.getElementById('deviceNameValue').textContent = deviceName;
                        document.getElementById('deviceNameDisplay').textContent = deviceName;
                        showToast('✅ Название устройства изменено');
                    }
                });
            };

            window.editAppName = function() {
                if (!rootEnabled) { showToast('❌ Требуется ROOT доступ'); return; }
                openModal('Изменение названия приложений', 'Введите новый префикс', appPrefix, function(value) {
                    if (value.trim()) {
                        appPrefix = value.trim();
                        document.getElementById('appNameValue').textContent = appPrefix;
                        document.querySelectorAll('.app-name').forEach(el => {
                            const old = el.textContent;
                            if (old === 'Настройки' || old === 'Галерея' || old === 'Монтаж' || old ===
                                'Черновик' || old === 'Музыка' || old === 'POFO Play' || old === 'Кликер')
                                return;
                            el.textContent = appPrefix + ' ' + old;
                        });
                        document.getElementById('storeTitle').textContent = appPrefix + ' Play';
                        showToast('✅ Префикс приложений изменён');
                    }
                });
            };

            // ===== ЗАЩИТА ПРИЛОЖЕНИЙ =====
            window.toggleAppLock = function() {
                appLockEnabled = !appLockEnabled;
                const toggle = document.querySelector('#detail-security .settings-detail-item .toggle');
                if (toggle) {
                    if (appLockEnabled) {
                        toggle.classList.remove('off');
                        toggle.classList.add('on');
                    } else {
                        toggle.classList.remove('on');
                        toggle.classList.add('off');
                    }
                }
                document.getElementById('lockStatusItem').style.display = appLockEnabled ? 'flex' : 'none';
                document.getElementById('changePassItem').style.display = appLockEnabled ? 'flex' : 'none';
                document.getElementById('disableLockItem').style.display = appLockEnabled ? 'flex' : 'none';
                showToast(appLockEnabled ? '🔒 Защита приложений включена' : '🔓 Защита приложений отключена');
                if (appLockEnabled && appLockPassword === '1234') {
                    showToast('⚠️ Используйте пароль по умолчанию: 1234');
                }
            };

            window.changeLockPassword = function() {
                if (!appLockEnabled) { showToast('❌ Сначала включите защиту'); return; }
                openModal('Изменить пароль', 'Введите новый пароль (4 цифры)', '****', function(value) {
                    if (/^\d{4}$/.test(value)) {
                        appLockPassword = value;
                        showToast('✅ Пароль изменён на ' + value);
                    } else {
                        showToast('❌ Пароль должен содержать 4 цифры');
                    }
                });
                document.getElementById('modalInput').type = 'password';
                document.getElementById('modalInput').maxLength = 4;
            };

            window.disableLockWithPassword = function() {
                if (!appLockEnabled) { showToast('❌ Защита уже отключена'); return; }
                if (appLockPassword === '1234') {
                    appLockEnabled = false;
                    document.getElementById('appLockToggle').classList.remove('on');
                    document.getElementById('appLockToggle').classList.add('off');
                    document.getElementById('lockStatusItem').style.display = 'none';
                    document.getElementById('changePassItem').style.display = 'none';
                    document.getElementById('disableLockItem').style.display = 'none';
                    showToast('🔓 Защита отключена (пароль по умолчанию)');
                    return;
                }
                openModal('Отключение защиты', 'Введите текущий пароль', '****', function(value) {
                    if (value === appLockPassword) {
                        appLockEnabled = false;
                        document.getElementById('appLockToggle').classList.remove('on');
                        document.getElementById('appLockToggle').classList.add('off');
                        document.getElementById('lockStatusItem').style.display = 'none';
                        document.getElementById('changePassItem').style.display = 'none';
                        document.getElementById('disableLockItem').style.display = 'none';
                        showToast('🔓 Защита отключена');
                    } else {
                        showToast('❌ Неверный пароль');
                    }
                });
                document.getElementById('modalInput').type = 'password';
                document.getElementById('modalInput').maxLength = 4;
            };

            function checkAppLock(appName, callback) {
                if (!appLockEnabled) { callback(); return; }
                pendingApp = { name: appName, callback: callback };
                document.getElementById('appLockOverlay').classList.add('open');
                document.getElementById('lockInput').value = '';
                lockInputValue = '';
                document.getElementById('lockError').textContent = '';
                document.getElementById('lockInput').focus();
            }

            window.lockKeyPress = function(key) {
                const input = document.getElementById('lockInput');
                if (key === 'back') {
                    if (lockInputValue.length > 0) {
                        lockInputValue = lockInputValue.slice(0, -1);
                        input.value = lockInputValue;
                    }
                } else if (key === 'clear') {
                    lockInputValue = '';
                    input.value = '';
                } else {
                    if (lockInputValue.length < 4) {
                        lockInputValue += key;
                        input.value = lockInputValue;
                    }
                }
                document.getElementById('lockError').textContent = '';
            };

            window.lockConfirm = function() {
                if (lockInputValue === appLockPassword) {
                    document.getElementById('appLockOverlay').classList.remove('open');
                    if (pendingApp) {
                        pendingApp.callback();
                        pendingApp = null;
                    }
                } else {
                    document.getElementById('lockError').textContent = '❌ Неверный пароль';
                    lockInputValue = '';
                    document.getElementById('lockInput').value = '';
                }
            };

            document.getElementById('appLockOverlay').addEventListener('click', function(e) {
                if (e.target === this) {
                    this.classList.remove('open');
                    pendingApp = null;
                }
            });

            // ===== ОТКРЫТИЕ/ЗАКРЫТИЕ =====
            function openAppWithLock(windowId, appName) {
                checkAppLock(appName, function() {
                    openApp(windowId);
                });
            }

            function openApp(windowId) {
                const win = document.getElementById(windowId);
                if (win) win.classList.add('open');
                if (windowId === 'galleryWindow') renderGalleryGrid();
                if (windowId === 'editorWindow') initEditor();
                if (windowId === 'notesWindow') renderNotes();
                if (windowId === 'musicWindow') renderMusic();
                if (windowId === 'storeWindow') renderStore();
                if (windowId === 'clickerWindow') initClicker();
            }

            function closeApp(windowId) {
                const win = document.getElementById(windowId);
                if (win) {
                    win.classList.remove('open');
                    if (windowId === 'settingsWindow') {
                        document.querySelectorAll('.settings-detail').forEach(d => d.classList.remove('active'));
                        document.getElementById('settingsList').style.display = 'flex';
                    }
                    if (windowId === 'galleryWindow') {
                        document.getElementById('gallerySection').style.display = 'none';
                        document.getElementById('galleryGrid').style.display = 'grid';
                    }
                    if (windowId === 'storeWindow') {
                        document.getElementById('appPage').style.display = 'none';
                        document.getElementById('storeGrid').style.display = 'grid';
                    }
                    if (windowId === 'clickerWindow') {
                        if (autoclickerInterval) {
                            clearInterval(autoclickerInterval);
                            autoclickerInterval = null;
                        }
                    }
                }
            }

            document.querySelectorAll('.app-item[data-app]').forEach(item => {
                item.addEventListener('click', function() {
                    const app = this.dataset.app;
                    if (app === 'settings') openApp('settingsWindow');
                    else if (app === 'gallery') openAppWithLock('galleryWindow', 'Галерея');
                    else if (app === 'editor') openAppWithLock('editorWindow', 'Монтаж');
                    else if (app === 'notes') openAppWithLock('notesWindow', 'Черновик');
                    else if (app === 'music') openAppWithLock('musicWindow', 'Музыка');
                    else if (app === 'store') openAppWithLock('storeWindow', 'POFO Play');
                    else if (app === 'clicker') openAppWithLock('clickerWindow', 'Кликер');
                    else if (app === 'adminPanel') { if (currentUser && currentUser.role === 'Админ') openAdminPanel(); }
                    else if (app === 'ownerPanel') { if (currentUser && currentUser.role === 'Владелец') openOwnerPanel(); }
                });
            });

            document.querySelectorAll('.app-window').forEach(win => {
                win.addEventListener('click', function(e) {
                    if (e.target === this) {
                        this.classList.remove('open');
                        if (this.id === 'settingsWindow') {
                            document.querySelectorAll('.settings-detail').forEach(d => d.classList.remove('active'));
                            document.getElementById('settingsList').style.display = 'flex';
                        }
                        if (this.id === 'galleryWindow') {
                            document.getElementById('gallerySection').style.display = 'none';
                            document.getElementById('galleryGrid').style.display = 'grid';
                        }
                        if (this.id === 'storeWindow') {
                            document.getElementById('appPage').style.display = 'none';
                            document.getElementById('storeGrid').style.display = 'grid';
                        }
                        if (this.id === 'clickerWindow') {
                            if (autoclickerInterval) {
                                clearInterval(autoclickerInterval);
                                autoclickerInterval = null;
                            }
                        }
                    }
                });
            });

            // ===== НАСТРОЙКИ =====
            const settingsList = document.getElementById('settingsList');
            const details = document.querySelectorAll('.settings-detail');

            document.querySelectorAll('.settings-item[data-detail]').forEach(item => {
                item.addEventListener('click', function() {
                    const detailId = this.dataset.detail;
                    settingsList.style.display = 'none';
                    details.forEach(d => d.classList.remove('active'));
                    const target = document.getElementById('detail-' + detailId);
                    if (target) target.classList.add('active');
                    if (detailId === 'about') updateRootUI();
                    if (detailId === 'security') {
                        document.getElementById('lockStatusItem').style.display = appLockEnabled ? 'flex' : 'none';
                        document.getElementById('changePassItem').style.display = appLockEnabled ? 'flex' : 'none';
                        document.getElementById('disableLockItem').style.display = appLockEnabled ? 'flex' : 'none';
                    }
                });
            });

            window.closeDetail = function() {
                details.forEach(d => d.classList.remove('active'));
                settingsList.style.display = 'flex';
            };

            window.toggleSwitch = function(element, id) {
                const toggle = element.querySelector('.toggle');
                if (!toggle) return;
                const isOn = toggle.classList.contains('on');
                if (isOn) { toggle.classList.remove('on');
                    toggle.classList.add('off'); } else { toggle.classList.remove('off');
                    toggle.classList.add('on'); }
                applySettingChange(id, !isOn);
                updateAllDescriptions();
                showToast(isOn ? 'Выключено' : 'Включено');
            };

            function applySettingChange(id, newState) {
                const screen = document.getElementById('screen');
                switch (id) {
                    case 'darkTheme':
                        if (!newState) screen.classList.add('light-theme');
                        else screen.classList.remove('light-theme');
                        break;
                    case 'brightness':
                        const brightEl = document.getElementById('brightnessToggle');
                        if (brightEl) {
                            const isOn = brightEl.classList.contains('on');
                            document.getElementById('displayDesc').textContent =
                                (document.getElementById('darkThemeToggle').classList.contains('on') ? 'Тёмная тема' :
                                    'Светлая тема') +
                                ' · ' + (isOn ? 'Адаптивная яркость' : 'Ручная яркость');
                        }
                        break;
                    case 'spiralOnScreen':
                        spiralVisible = newState;
                        if (newState) { spiral.style.display = 'inline-block';
                            setRandomSpiral(); } else spiral.style.display = 'none';
                        break;
                    case 'wifi':
                        document.getElementById('wifiDesc').textContent = newState ? 'POFO_Network · Подключено' :
                            'Отключено';
                        const wt = document.getElementById('wifiToggle');
                        if (wt) { if (newState) { wt.classList.remove('off');
                            wt.classList.add('on'); } else { wt.classList.remove('on');
                            wt.classList.add('off'); } }
                        break;
                    case 'bluetooth':
                        document.getElementById('btDesc').textContent = newState ? 'Включено · 2 устройства' :
                        'Отключено';
                        const bt = document.getElementById('btToggle');
                        if (bt) { if (newState) { bt.classList.remove('off');
                            bt.classList.add('on'); } else { bt.classList.remove('on');
                            bt.classList.add('off'); } }
                        updateStatusBar();
                        break;
                    case 'silentMode':
                        updateStatusBar();
                        if (newState) {
                            document.getElementById('soundDesc').textContent = '🔇 Режим тишины включён';
                            document.getElementById('statusRight').innerHTML = '<i class="fas fa-bell-slash"></i> Тишина';
                        } else {
                            document.getElementById('soundDesc').textContent = 'Звонок ' + document.getElementById(
                                'ringVolume').textContent + ' · Медиа ' + document.getElementById('mediaVolume')
                            .textContent;
                            updateStatusBar();
                        }
                        break;
                    case 'batterySaver':
                        const saverOn = document.getElementById('batterySaverToggle').classList.contains('on');
                        document.getElementById('batteryDesc').textContent = document.getElementById('batteryLevel')
                            .textContent + '% · ' + (saverOn ? 'Режим экономии' : 'Обычный режим');
                        document.getElementById('batteryLife').textContent = saverOn ? '~24 ч' : '~18 ч';
                        break;
                }
                updateAllDescriptions();
            }

            const textColors = [{ name: 'Белый', class: '' }, { name: 'Красный', class: 'text-color-red' },
                { name: 'Синий', class: 'text-color-blue' }, { name: 'Зелёный', class: 'text-color-green' },
                { name: 'Фиолетовый', class: 'text-color-purple' }
            ];
            let textColorIndex = 0;

            window.cycleTextColor = function() {
                const screen = document.getElementById('screen');
                textColors.forEach(c => screen.classList.remove(c.class));
                textColorIndex = (textColorIndex + 1) % textColors.length;
                const color = textColors[textColorIndex];
                if (color.class) screen.classList.add(color.class);
                const display = document.getElementById('textColorDisplay');
                display.textContent = '● ' + color.name;
                display.style.color = color.class ?
                    (color.class.includes('red') ? '#ef4444' :
                        color.class.includes('blue') ? '#3b82f6' :
                        color.class.includes('green') ? '#22c55e' :
                        color.class.includes('purple') ? '#a855f7' : '#e0e7ff') : '#e0e7ff';
                showToast('Цвет текста: ' + color.name);
            };

            window.changeWifiNetwork = function() {
                const networks = ['POFO_Network', 'POFO_5G', 'POFO_Office', 'POFO_Home'];
                const current = document.getElementById('wifiNetwork');
                let idx = networks.indexOf(current.textContent);
                idx = (idx + 1) % networks.length;
                current.textContent = networks[idx];
                document.getElementById('wifiDesc').textContent = networks[idx] + ' · Подключено';
                showToast('Переключено на ' + networks[idx]);
            };

            window.toggleBtDevice = function(element) {
                const value = element.querySelector('.value');
                if (!value) return;
                if (value.classList.contains('on')) {
                    value.classList.remove('on');
                    value.innerHTML = '<i class="fas fa-circle" style="color:rgba(210,220,255,0.2);"></i> Отключено';
                } else {
                    value.classList.add('on');
                    value.innerHTML = '<i class="fas fa-check-circle"></i> Подключено';
                }
                updateBtDesc();
                showToast('Статус устройства изменён');
            };

            function updateBtDesc() {
                const d1 = document.getElementById('btDevice1');
                const d2 = document.getElementById('btDevice2');
                let count = 0;
                if (d1.classList.contains('on')) count++;
                if (d2.classList.contains('on')) count++;
                const btOn = document.getElementById('btToggle').classList.contains('on');
                document.getElementById('btDesc').textContent = (btOn ? 'Включено' : 'Отключено') + ' · ' + count +
                    ' устройств' + (count !== 1 ? 'а' : '');
            }

            const accentColors = [{ name: 'Розовый', color: '#f472b6' }, { name: 'Синий', color: '#818cf8' },
                { name: 'Зелёный', color: '#34d399' }, { name: 'Оранжевый', color: '#fb923c' },
                { name: 'Фиолетовый', color: '#a78bfa' }
            ];
            let accentIndex = 0;

            window.cycleAccentColor = function() {
                accentIndex = (accentIndex + 1) % accentColors.length;
                const color = accentColors[accentIndex];
                document.getElementById('accentColorDisplay').textContent = '● ' + color.name;
                document.getElementById('accentColorDisplay').style.color = color.color;
                document.querySelectorAll('.settings-item-icon.pink').forEach(el => {
                    el.style.color = color.color;
                    el.style.background = color.color + '33';
                });
                showToast('Цвет: ' + color.name);
            };

            const fontSizes = ['Маленький', 'Средний', 'Большой', 'Огромный'];
            let fontSizeIndex = 1;

            window.cycleFontSize = function() {
                fontSizeIndex = (fontSizeIndex + 1) % fontSizes.length;
                document.getElementById('fontSizeDisplay').textContent = fontSizes[fontSizeIndex];
                const sizes = { 'Маленький': '12px', 'Средний': '15px', 'Большой': '18px', 'Огромный': '22px' };
                document.querySelectorAll(
                    '.settings-item-title, .settings-detail-title, .app-name, .gallery-item .gallery-name, .note-item .note-title, .music-item .music-name'
                    ).forEach(el => {
                    el.style.fontSize = sizes[fontSizes[fontSizeIndex]];
                });
                showToast('Размер: ' + fontSizes[fontSizeIndex]);
            };

            window.changeVolume = function(element, type) {
                const valueEl = element.querySelector('.value');
                if (!valueEl) return;
                let current = parseInt(valueEl.textContent);
                current = (current + 10) % 110;
                if (current > 100) current = 10;
                valueEl.textContent = current + '%';
                if (type === 'ring') document.getElementById('soundDesc').textContent = 'Звонок ' + current + '% · Медиа ' +
                    document.getElementById('mediaVolume').textContent;
                if (type === 'media') document.getElementById('soundDesc').textContent = 'Звонок ' + document.getElementById(
                    'ringVolume').textContent + ' · Медиа ' + current + '%';
                showToast(type + ': ' + current + '%');
                if (navigator.vibrate) navigator.vibrate(30);
            };

            let batteryLevel = 86;

            window.changeBatteryLevel = function() {
                batteryLevel = batteryLevel - 5 + Math.floor(Math.random() * 11);
                if (batteryLevel < 10) batteryLevel = 10;
                if (batteryLevel > 100) batteryLevel = 100;
                document.getElementById('batteryLevel').textContent = batteryLevel + '%';
                const saverOn = document.getElementById('batterySaverToggle').classList.contains('on');
                document.getElementById('batteryDesc').textContent = batteryLevel + '% · ' + (saverOn ?
                    'Режим экономии' : 'Обычный режим');
                updateStatusBar();
                if (navigator.vibrate) navigator.vibrate(20);
                showToast('Заряд: ' + batteryLevel + '%');
            };

            let fastChargeOn = true;

            window.toggleFastCharge = function() {
                fastChargeOn = !fastChargeOn;
                const el = document.getElementById('fastChargeStatus');
                if (fastChargeOn) {
                    el.classList.add('on');
                    el.innerHTML = '<i class="fas fa-check-circle"></i> Активна';
                } else {
                    el.classList.remove('on');
                    el.innerHTML = '<i class="fas fa-circle" style="color:rgba(210,220,255,0.2);"></i> Отключена';
                }
                showToast(fastChargeOn ? '⚡ Быстрая зарядка включена' : '🔌 Быстрая зарядка отключена');
            };

            let storageUsed = 64.2;

            window.changeStorage = function() {
                storageUsed = storageUsed + 0.5 + Math.random() * 2;
                if (storageUsed > 120) storageUsed = 20;
                document.getElementById('storageUsed').textContent = storageUsed.toFixed(1) + ' ГБ';
                const free = (128 - storageUsed).toFixed(1);
                document.getElementById('storageFree').textContent = free + ' ГБ';
                document.getElementById('storageDesc').textContent = storageUsed.toFixed(1) + ' ГБ из 128 ГБ';
                showToast('Хранилище обновлено');
            };

            window.checkUpdates = function() {
                const el = document.getElementById('updateStatus');
                if (el.style.color === 'rgb(52, 211, 153)' || el.style.color === '#34d399') {
                    el.style.color = 'rgba(210,220,255,0.3)';
                    el.innerHTML = '<i class="fas fa-circle"></i> Нет обновлений';
                    showToast('✅ Система обновлена');
                } else {
                    el.style.color = '#34d399';
                    el.innerHTML = '<i class="fas fa-check-circle"></i> Доступны';
                    showToast('📦 Обновления найдены!');
                }
            };

            function updateAllDescriptions() {
                const darkOn = document.getElementById('darkThemeToggle').classList.contains('on');
                const brightOn = document.getElementById('brightnessToggle').classList.contains('on');
                document.getElementById('displayDesc').textContent = (darkOn ? 'Тёмная тема' : 'Светлая тема') + ' · ' + (
                    brightOn ? 'Адаптивная яркость' : 'Ручная яркость');
                updateBtDesc();
                const saverOn = document.getElementById('batterySaverToggle').classList.contains('on');
                document.getElementById('batteryDesc').textContent = document.getElementById('batteryLevel').textContent +
                    '% · ' + (saverOn ? 'Режим экономии' : 'Обычный режим');
                const silentOn = document.getElementById('silentModeToggle').classList.contains('on');
                if (silentOn) {
                    document.getElementById('soundDesc').textContent = '🔇 Режим тишины включён';
                } else {
                    document.getElementById('soundDesc').textContent = 'Звонок ' + document.getElementById('ringVolume')
                        .textContent + ' · Медиа ' + document.getElementById('mediaVolume').textContent;
                }
            }

            function updateStatusBar() {
                const statusRight = document.getElementById('statusRight');
                const btOn = document.getElementById('btToggle').classList.contains('on');
                const silentOn = document.getElementById('silentModeToggle').classList.contains('on');
                let text = '';
                if (silentOn) {
                    text = '<i class="fas fa-bell-slash"></i> Тишина';
                } else {
                    text = '<i class="fas fa-battery-three-quarters"></i> ' + batteryLevel + '%';
                }
                if (btOn) text += ' · <i class="fas fa-bluetooth-b"></i>';
                statusRight.innerHTML = text;
            }

            // ===== ГАЛЕРЕЯ =====
            function renderGalleryGrid() {
                document.getElementById('allCount').textContent = allPhotos.length + ' фото';
                document.getElementById('myCount').textContent = myPhotos.length + ' фото';
            }

            window.openGallerySection = function(section) {
                currentSection = section;
                document.getElementById('galleryGrid').style.display = 'none';
                document.getElementById('gallerySection').style.display = 'block';
                const grid = document.getElementById('photoGrid');
                const addBtn = document.getElementById('galleryAddBtn');
                const camBtn = document.getElementById('galleryCameraBtn');

                let photos = [];
                if (section === 'all') { photos = allPhotos;
                    addBtn.style.display = 'flex';
                    camBtn.style.display = 'none'; } else if (section === 'camera') { photos = cameraPhotos;
                    addBtn.style.display = 'none';
                    camBtn.style.display = 'flex'; } else if (section === 'my') { photos = myPhotos;
                    addBtn.style.display = 'flex';
                    camBtn.style.display = 'none'; }

                if (photos.length === 0) {
                    grid.innerHTML =
                        '<div style="grid-column:1/-1;text-align:center;padding:40px 0;color:rgba(210,220,255,0.2);font-size:14px;">Нет файлов</div>';
                    return;
                }
                grid.innerHTML = photos.map((p, idx) => {
                    const isVideo = p.type === 'video';
                    const mediaElement = isVideo ?
                        `<video src="${p.data}" muted preload="metadata"></video><div class="video-play"><i class="fas fa-play-circle"></i></div>` :
                        `<img src="${p.data}" alt="Фото">`;
                    const duration = isVideo ? `<span class="video-duration">▶</span>` : '';
                    return `
                            <div class="photo-item" onclick="openMediaViewer(${idx}, '${section}')">
                                ${mediaElement}
                                ${duration}
                                <button class="photo-delete" onclick="event.stopPropagation();deletePhoto('${section}', ${idx})"><i class="fas fa-times"></i></button>
                            </div>
                        `;
                }).join('');
            };

            window.openMediaViewer = function(idx, section) {
                let photos = [];
                if (section === 'all') photos = allPhotos;
                else if (section === 'camera') photos = cameraPhotos;
                else if (section === 'my') photos = myPhotos;
                const item = photos[idx];
                if (!item) return;

                const viewer = document.getElementById('mediaViewer');
                const content = document.getElementById('mediaViewerContent');
                const info = document.getElementById('mediaViewerInfo');

                if (item.type === 'video') {
                    content.innerHTML =
                        `<video src="${item.data}" controls autoplay style="max-width:90%;max-height:80%;border-radius:12px;"></video>`;
                    info.textContent = '🎬 Видео · ' + (item.name || 'Без названия');
                } else {
                    content.innerHTML = `<img src="${item.data}" alt="Фото" style="max-width:90%;max-height:80%;border-radius:12px;">`;
                    info.textContent = '🖼️ Фото · ' + (item.name || 'Без названия');
                }
                viewer.classList.add('open');
            };

            window.closeMediaViewer = function() {
                document.getElementById('mediaViewer').classList.remove('open');
                document.getElementById('mediaViewerContent').innerHTML = '';
            };

            window.backToGallery = function() {
                document.getElementById('gallerySection').style.display = 'none';
                document.getElementById('galleryGrid').style.display = 'grid';
                renderGalleryGrid();
            };

            window.deletePhoto = function(section, idx) {
                if (section === 'all') allPhotos.splice(idx, 1);
                else if (section === 'camera') cameraPhotos.splice(idx, 1);
                else if (section === 'my') myPhotos.splice(idx, 1);
                openGallerySection(section);
                renderGalleryGrid();
                showToast('🗑️ Файл удалён');
            };

            window.addPhoto = function() {
                const input = document.createElement('input');
                input.type = 'file';
                input.accept = 'image/*,video/*';
                input.multiple = true;
                input.onchange = function(e) {
                    Array.from(e.target.files).forEach(file => {
                        const reader = new FileReader();
                        reader.onload = function(ev) {
                            const data = ev.target.result;
                            const isVideo = file.type.startsWith('video/');
                            const mediaData = {
                                id: ++photoIdCounter,
                                data: data,
                                type: isVideo ? 'video' : 'image',
                                name: file.name
                            };
                            if (currentSection === 'all') {
                                allPhotos.push(mediaData);
                            } else if (currentSection === 'my') {
                                myPhotos.push(mediaData);
                            } else if (currentSection === 'camera') {
                                if (!isVideo) {
                                    cameraPhotos.push(mediaData);
                                }
                            }
                            openGallerySection(currentSection);
                            renderGalleryGrid();
                        };
                        reader.readAsDataURL(file);
                    });
                    showToast('📸 Файлы добавлены');
                };
                input.click();
            };

            window.openCamera = function() {
                if (navigator.mediaDevices && navigator.mediaDevices.getUserMedia) {
                    navigator.mediaDevices.getUserMedia({ video: true }).then(function(stream) {
                        const video = document.createElement('video');
                        video.style.display = 'none';
                        document.body.appendChild(video);
                        video.srcObject = stream;
                        video.play();
                        setTimeout(() => {
                            const canvas = document.createElement('canvas');
                            canvas.width = video.videoWidth || 640;
                            canvas.height = video.videoHeight || 480;
                            const ctx = canvas.getContext('2d');
                            ctx.drawImage(video, 0, 0);
                            const data = canvas.toDataURL('image/jpeg');
                            cameraPhotos.push({ id: ++photoIdCounter, data: data, type: 'image', name: 'Снимок' });
                            allPhotos.push({ id: ++photoIdCounter, data: data, type: 'image', name: 'Снимок' });
                            stream.getTracks().forEach(t => t.stop());
                            video.remove();
                            openGallerySection('camera');
                            renderGalleryGrid();
                            showToast('📸 Фото сделано!');
                        }, 500);
                    }).catch(() => {
                        showToast('❌ Не удалось открыть камеру');
                    });
                } else {
                    showToast('❌ Камера не поддерживается');
                }
            };

            // ===== МУЗЫКА =====
            function renderMusic() {
                const grid = document.getElementById('musicGrid');
                let html = `<div class="music-upload-btn" onclick="uploadMusic()">
                        <i class="fas fa-cloud-upload-alt"></i>
                        Загрузить музыку<br>
                        <span style="font-size:10px;opacity:0.5;">MP3, WAV, AAC</span>
                    </div>`;
                musicFiles.forEach((m, idx) => {
                    html += `<div class="music-item">
                            <div class="music-icon"><i class="fas fa-music"></i></div>
                            <div class="music-name">${m.name}</div>
                            <div class="music-size">${(m.size / 1024).toFixed(1)} KB</div>
                            <div class="music-delete" onclick="deleteMusic(${idx})"><i class="fas fa-trash"></i></div>
                        </div>`;
                });
                grid.innerHTML = html;
            }

            window.uploadMusic = function() {
                const input = document.createElement('input');
                input.type = 'file';
                input.accept = 'audio/*';
                input.multiple = true;
                input.onchange = function(e) {
                    Array.from(e.target.files).forEach(file => {
                        musicFiles.push({
                            name: file.name,
                            size: file.size,
                            data: file
                        });
                    });
                    renderMusic();
                    showToast('🎵 Загружено ' + e.target.files.length + ' треков');
                };
                input.click();
            };

            window.deleteMusic = function(idx) {
                musicFiles.splice(idx, 1);
                renderMusic();
                showToast('🗑️ Трек удалён');
            };

            // ===== ЧЕРНОВИК =====
            function renderNotes() {
                const list = document.getElementById('notesList');
                const search = document.getElementById('notesSearch').value.toLowerCase();
                let filtered = notes;
                if (search) {
                    filtered = notes.filter(n => n.title.toLowerCase().includes(search) || n.content.toLowerCase().includes(
                    search));
                }
                if (filtered.length === 0) {
                    list.innerHTML = '<div class="note-empty">' + (notes.length === 0 ? 'Нет заметок. Нажмите «Создать»' :
                        'Ничего не найдено') + '</div>';
                    return;
                }
                list.innerHTML = filtered.map(n => `
                        <div class="note-item" onclick="openNote(${n.id})">
                            <div class="note-info">
                                <div class="note-title">${n.title || 'Без названия'}</div>
                                <div class="note-preview">${n.content ? n.content.substring(0, 60) : 'Пустая заметка'}</div>
                            </div>
                            <div class="note-date">${n.date}</div>
                        </div>
                    `).join('');
            }

            window.filterNotes = function() { renderNotes(); };

            window.openCreateModal = function() {
                document.getElementById('createModal').classList.add('open');
                document.getElementById('noteTitleInput').value = '';
                document.getElementById('noteTitleInput').focus();
            };

            window.closeCreateModal = function() {
                document.getElementById('createModal').classList.remove('open');
            };

            window.createNote = function() {
                const title = document.getElementById('noteTitleInput').value.trim() || 'Без названия';
                const now = new Date();
                const date = now.toLocaleDateString() + ' ' + now.toLocaleTimeString([], { hour: '2-digit', minute: '2-digit' });
                notes.unshift({
                    id: ++noteIdCounter,
                    title: title,
                    content: '',
                    date: date
                });
                closeCreateModal();
                renderNotes();
                showToast('📝 Заметка создана: ' + title);
            };

            window.openNote = function(id) {
                const note = notes.find(n => n.id === id);
                if (!note) return;
                currentNoteId = id;
                document.getElementById('noteViewerTitle').textContent = note.title || 'Без названия';
                document.getElementById('noteViewerContent').value = note.content || '';
                document.getElementById('noteViewer').classList.add('open');
            };

            window.closeNoteViewer = function() {
                document.getElementById('noteViewer').classList.remove('open');
                currentNoteId = null;
                renderNotes();
            };

            window.saveNoteContent = function() {
                if (currentNoteId === null) return;
                const note = notes.find(n => n.id === currentNoteId);
                if (note) {
                    note.content = document.getElementById('noteViewerContent').value;
                }
            };

            window.deleteNote = function() {
                if (currentNoteId === null) return;
                if (confirm('Удалить заметку?')) {
                    notes = notes.filter(n => n.id !== currentNoteId);
                    closeNoteViewer();
                    renderNotes();
                    showToast('🗑️ Заметка удалена');
                }
            };

            document.getElementById('createModal').addEventListener('click', function(e) {
                if (e.target === this) closeCreateModal();
            });
            document.getElementById('noteTitleInput').addEventListener('keydown', function(e) {
                if (e.key === 'Enter') createNote();
            });

            // ===== МОНТАЖ =====
            function initEditor() {
                editorCanvas = document.getElementById('editorCanvas');
                editorCtx = editorCanvas.getContext('2d');
                if (!editorImage) {
                    document.getElementById('editorPlaceholder').style.display = 'block';
                    editorCanvas.style.display = 'none';
                } else {
                    document.getElementById('editorPlaceholder').style.display = 'none';
                    editorCanvas.style.display = 'block';
                    renderEditor();
                }
                renderLayers();
            }

            function renderEditor() {
                if (!editorImage || !editorCtx) return;
                const canvas = editorCanvas;
                const ctx = editorCtx;
                const w = canvas.width;
                const h = canvas.height;

                ctx.clearRect(0, 0, w, h);
                ctx.filter = getFilterString();
                ctx.drawImage(editorImage, 0, 0, w, h);
                ctx.filter = 'none';

                editorLayers.forEach((layer, idx) => {
                    if (layer.hidden) return;
                    if (layer.type === 'text') {
                        ctx.font = layer.size + 'px sans-serif';
                        ctx.fillStyle = layer.color || '#ffffff';
                        ctx.textAlign = 'center';
                        ctx.fillText(layer.text, layer.x, layer.y);
                    } else if (layer.type === 'emoji') {
                        ctx.font = layer.size + 'px sans-serif';
                        ctx.textAlign = 'center';
                        ctx.fillText(layer.emoji, layer.x, layer.y);
                    } else if (layer.type === 'image' && layer.image) {
                        const img = layer.image;
                        const ratio = Math.min(200 / img.width, 200 / img.height);
                        const iw = img.width * ratio;
                        const ih = img.height * ratio;
                        ctx.drawImage(img, layer.x - iw / 2, layer.y - ih / 2, iw, ih);
                    }
                });

                if (selectedLayerIndex >= 0 && selectedLayerIndex < editorLayers.length) {
                    const layer = editorLayers[selectedLayerIndex];
                    if (!layer.hidden) {
                        ctx.strokeStyle = 'rgba(244, 114, 182, 0.4)';
                        ctx.lineWidth = 2;
                        ctx.setLineDash([5, 5]);
                        ctx.strokeRect(layer.x - 50, layer.y - 30, 100, 60);
                        ctx.setLineDash([]);
                    }
                }
            }

            function getFilterString() {
                let f = '';
                if (editorFilter === 'grayscale') f = 'grayscale(1)';
                else if (editorFilter === 'invert') f = 'invert(1)';
                else if (editorFilter === 'sepia') f = 'sepia(1)';
                else if (editorFilter === 'brightness') f = 'brightness(' + (editorBrightness / 100) + ')';
                else f = 'brightness(' + (editorBrightness / 100) + ') contrast(' + (editorContrast / 100) + ')';
                return f;
            }

            function renderLayers() {
                const list = document.getElementById('layersList');
                if (editorLayers.length === 0) {
                    list.innerHTML = '<div style="color:rgba(210,220,255,0.15);font-size:11px;text-align:center;padding:10px 0;">Нет слоёв</div>';
                    return;
                }
                list.innerHTML = editorLayers.map((layer, idx) => `
                        <div class="layer-item ${idx === selectedLayerIndex ? 'active' : ''}" onclick="selectLayer(${idx})">
                            <span class="layer-vis" onclick="toggleLayerVisibility(${idx})">${layer.hidden ? '◯' : '●'}</span>
                            <span class="layer-name">${layer.type === 'text' ? '📝 ' + (layer.text || 'Текст') : layer.type === 'emoji' ? '😊 ' + (layer.emoji || 'Эмодзи') : '🖼️ Фото'}</span>
                            <span class="layer-delete" onclick="deleteLayer(${idx})"><i class="fas fa-times"></i></span>
                        </div>
                    `).join('');
            }

            window.selectLayer = function(idx) {
                selectedLayerIndex = idx;
                renderLayers();
                renderEditor();
            };

            window.toggleLayerVisibility = function(idx) {
                if (editorLayers[idx]) {
                    editorLayers[idx].hidden = !editorLayers[idx].hidden;
                    renderLayers();
                    renderEditor();
                }
            };

            window.deleteLayer = function(idx) {
                editorLayers.splice(idx, 1);
                if (selectedLayerIndex >= editorLayers.length) selectedLayerIndex = editorLayers.length - 1;
                renderLayers();
                renderEditor();
                showToast('🗑️ Слой удалён');
            };

            window.selectLayerOnCanvas = function(event) {
                const rect = editorCanvas.getBoundingClientRect();
                const scaleX = editorCanvas.width / rect.width;
                const scaleY = editorCanvas.height / rect.height;
                const mouseX = (event.clientX - rect.left) * scaleX;
                const mouseY = (event.clientY - rect.top) * scaleY;

                let found = -1;
                for (let i = editorLayers.length - 1; i >= 0; i--) {
                    const layer = editorLayers[i];
                    if (layer.hidden) continue;
                    const dx = Math.abs(mouseX - layer.x);
                    const dy = Math.abs(mouseY - layer.y);
                    if (dx < 60 && dy < 40) {
                        found = i;
                        break;
                    }
                }
                if (found >= 0) {
                    selectedLayerIndex = found;
                    renderLayers();
                    renderEditor();
                    showToast('Выбран слой ' + (found + 1));
                }
            };

            document.addEventListener('mousedown', function(e) {
                if (selectedLayerIndex < 0 || selectedLayerIndex >= editorLayers.length) return;
                const rect = editorCanvas.getBoundingClientRect();
                if (!e.target.closest('#editorCanvas')) return;
                const scaleX = editorCanvas.width / rect.width;
                const scaleY = editorCanvas.height / rect.height;
                const mouseX = (e.clientX - rect.left) * scaleX;
                const mouseY = (e.clientY - rect.top) * scaleY;
                const layer = editorLayers[selectedLayerIndex];
                if (layer.hidden) return;
                const dx = Math.abs(mouseX - layer.x);
                const dy = Math.abs(mouseY - layer.y);
                if (dx < 60 && dy < 40) {
                    dragLayerIndex = selectedLayerIndex;
                    dragStartX = mouseX - layer.x;
                    dragStartY = mouseY - layer.y;
                    isDragging = true;
                    editorCanvas.style.cursor = 'grabbing';
                }
            });

            document.addEventListener('mousemove', function(e) {
                if (!isDragging || dragLayerIndex < 0) return;
                const rect = editorCanvas.getBoundingClientRect();
                const scaleX = editorCanvas.width / rect.width;
                const scaleY = editorCanvas.height / rect.height;
                const mouseX = (e.clientX - rect.left) * scaleX;
                const mouseY = (e.clientY - rect.top) * scaleY;
                const layer = editorLayers[dragLayerIndex];
                if (layer) {
                    layer.x = Math.max(10, Math.min(editorCanvas.width - 10, mouseX - dragStartX));
                    layer.y = Math.max(20, Math.min(editorCanvas.height - 20, mouseY - dragStartY));
                    renderEditor();
                }
            });

            document.addEventListener('mouseup', function() {
                if (isDragging) {
                    isDragging = false;
                    dragLayerIndex = -1;
                    editorCanvas.style.cursor = 'default';
                }
            });

            window.editorLoadImage = function() {
                const input = document.createElement('input');
                input.type = 'file';
                input.accept = 'image/*';
                input.onchange = function(e) {
                    const file = e.target.files[0];
                    if (!file) return;
                    const reader = new FileReader();
                    reader.onload = function(ev) {
                        const img = new Image();
                        img.onload = function() {
                            editorImage = img;
                            editorCanvas.width = Math.min(img.width, 1200);
                            editorCanvas.height = Math.min(img.height, 900);
                            document.getElementById('editorPlaceholder').style.display = 'none';
                            editorCanvas.style.display = 'block';
                            editorLayers.unshift({
                                type: 'image',
                                image: img,
                                x: editorCanvas.width / 2,
                                y: editorCanvas.height / 2,
                                hidden: false
                            });
                            selectedLayerIndex = 0;
                            renderLayers();
                            renderEditor();
                            showToast('✅ Изображение загружено');
                        };
                        img.src = ev.target.result;
                    };
                    reader.readAsDataURL(file);
                };
                input.click();
            };

            window.editorAddText = function() {
                if (!editorImage) { showToast('❌ Сначала загрузите изображение'); return; }
                openModal('Добавить текст', 'Введите текст', 'Текст...', function(value) {
                    if (!value.trim()) return;
                    const canvas = editorCanvas;
                    editorLayers.push({
                        type: 'text',
                        text: value,
                        x: canvas.width / 2 + Math.random() * 60 - 30,
                        y: canvas.height / 2 + Math.random() * 60 - 30,
                        size: 30 + Math.floor(Math.random() * 20),
                        color: '#ffffff',
                        hidden: false
                    });
                    selectedLayerIndex = editorLayers.length - 1;
                    renderLayers();
                    renderEditor();
                    showToast('📝 Текст добавлен');
                });
            };

            window.editorAddEmoji = function() {
                if (!editorImage) { showToast('❌ Сначала загрузите изображение'); return; }
                openModal('Выберите эмодзи', 'Введите эмодзи (или скопируйте)', '😊', function(value) {
                    if (!value.trim()) return;
                    const canvas = editorCanvas;
                    editorLayers.push({
                        type: 'emoji',
                        emoji: value,
                        x: canvas.width / 2 + Math.random() * 100 - 50,
                        y: canvas.height / 2 + Math.random() * 100 - 50,
                        size: 40 + Math.floor(Math.random() * 30),
                        hidden: false
                    });
                    selectedLayerIndex = editorLayers.length - 1;
                    renderLayers();
                    renderEditor();
                    showToast('😊 Эмодзи добавлен');
                });
            };

            window.editorAddImage = function() {
                if (!editorImage) { showToast('❌ Сначала загрузите основное изображение'); return; }
                const input = document.createElement('input');
                input.type = 'file';
                input.accept = 'image/*';
                input.onchange = function(e) {
                    const file = e.target.files[0];
                    if (!file) return;
                    const reader = new FileReader();
                    reader.onload = function(ev) {
                        const img = new Image();
                        img.onload = function() {
                            const canvas = editorCanvas;
                            editorLayers.push({
                                type: 'image',
                                image: img,
                                x: canvas.width / 2 + Math.random() * 80 - 40,
                                y: canvas.height / 2 + Math.random() * 80 - 40,
                                hidden: false
                            });
                            selectedLayerIndex = editorLayers.length - 1;
                            renderLayers();
                            renderEditor();
                            showToast('🖼️ Фото добавлено как слой');
                        };
                        img.src = ev.target.result;
                    };
                    reader.readAsDataURL(file);
                };
                input.click();
            };

            window.applyFilter = function(filter) {
                editorFilter = filter;
                document.querySelectorAll('.filter-chip').forEach(el => el.classList.remove('active'));
                document.querySelectorAll('.filter-chip').forEach(el => {
                    if (el.textContent.toLowerCase() === filter || (filter === 'none' && el.textContent === 'Нет'))
                        el.classList.add('active');
                });
                renderEditor();
                showToast('Фильтр: ' + (filter === 'none' ? 'Нет' : filter));
            };

            window.updateBrightness = function() {
                editorBrightness = parseInt(document.getElementById('brightnessSlider').value);
                renderEditor();
            };

            window.updateContrast = function() {
                editorContrast = parseInt(document.getElementById('contrastSlider').value);
                renderEditor();
            };

            window.editorExport = function() {
                if (!editorImage) {
                    showToast('❌ Сначала загрузите изображение');
                    return;
                }
                openModal('Экспорт', 'Выберите размер (от 1 до 4096)', '1024', function(value) {
                    let size = parseInt(value);
                    if (isNaN(size) || size < 1) size = 1;
                    if (size > 4096) size = 4096;
                    const canvas = document.createElement('canvas');
                    const ratio = editorImage.width / editorImage.height;
                    let w, h;
                    if (ratio > 1) { w = size;
                        h = Math.round(size / ratio); } else { h = size;
                        w = Math.round(size * ratio); }
                    canvas.width = w;
                    canvas.height = h;
                    const ctx = canvas.getContext('2d');

                    ctx.filter = getFilterString();
                    ctx.drawImage(editorImage, 0, 0, w, h);
                    ctx.filter = 'none';

                    editorLayers.forEach(layer => {
                        if (layer.hidden) return;
                        const scale = w / editorImage.width;
                        if (layer.type === 'text') {
                            ctx.font = layer.size * scale + 'px sans-serif';
                            ctx.fillStyle = layer.color || '#ffffff';
                            ctx.textAlign = 'center';
                            ctx.fillText(layer.text, layer.x * scale, layer.y * scale);
                        } else if (layer.type === 'emoji') {
                            ctx.font = layer.size * scale + 'px sans-serif';
                            ctx.textAlign = 'center';
                            ctx.fillText(layer.emoji, layer.x * scale, layer.y * scale);
                        } else if (layer.type === 'image' && layer.image) {
                            const img = layer.image;
                            const ratio2 = Math.min(200 * scale / img.width, 200 * scale / img.height);
                            const iw = img.width * ratio2;
                            const ih = img.height * ratio2;
                            ctx.drawImage(img, layer.x * scale - iw / 2, layer.y * scale - ih / 2, iw, ih);
                        }
                    });

                    const link = document.createElement('a');
                    link.download = 'edited_' + size + 'px.png';
                    link.href = canvas.toDataURL('image/png');
                    link.click();
                    showToast('✅ Экспортировано в ' + size + 'px');
                });
            };

            // ===== POFO PLAY =====
            function renderStore() {
                document.getElementById('storeGrid').style.display = 'grid';
                document.getElementById('appPage').style.display = 'none';
                if (installedApps.includes('wallpapers')) {
                    const btn = document.getElementById('installBtn_wallpapers');
                    if (btn) { btn.textContent = 'Установлено';
                        btn.className = 'store-app-btn installed'; }
                }
                if (installedApps.includes('clicker')) {
                    const btn = document.getElementById('installBtn_clicker');
                    if (btn) { btn.textContent = 'Установлено';
                        btn.className = 'store-app-btn installed'; }
                }
            }

            window.installApp = function(app) {
                if (installedApps.includes(app)) {
                    showToast('✅ Приложение уже установлено');
                    if (app === 'wallpapers') openAppPage('wallpapers');
                    if (app === 'clicker') { openApp('clickerWindow'); }
                    return;
                }

                const overlay = document.getElementById('installOverlay');
                overlay.classList.add('open');

                setTimeout(() => {
                    overlay.classList.remove('open');
                    installedApps.push(app);

                    const btn = document.getElementById('installBtn_' + app);
                    if (btn) { btn.textContent = 'Установлено';
                        btn.className = 'store-app-btn installed'; }

                    let page = 1;
                    for (let p = 1; p <= 5; p++) {
                        const grid = document.getElementById(p === 1 ? 'appGrid' : 'appGrid' + p);
                        if (grid && grid.children.length < 8) {
                            page = p;
                            break;
                        }
                    }

                    if (app === 'wallpapers') {
                        addAppToPage('wallpapers', 'Обои', 'fa-image', 'grad-2', page);
                    } else if (app === 'clicker') {
                        addAppToPage('clicker', 'Кликер', 'fa-hand-pointer', 'grad-clicker', page);
                    }

                    showToast('✅ Приложение установлено!');
                }, 3000);
            };

            window.openAppPage = function(app) {
                document.getElementById('storeGrid').style.display = 'none';
                document.getElementById('appPage').style.display = 'block';
                const content = document.getElementById('appPageContent');

                if (app === 'wallpapers') {
                    content.innerHTML = `
                            <div style="margin-bottom:16px;">
                                <h3 style="color:#e0e7ff; font-weight:600; font-size:18px;">🖼️ Обои</h3>
                                <p style="color:rgba(210,220,255,0.3); font-size:13px; margin-top:4px;">Выберите стиль обоев</p>
                            </div>
                            <div style="display:flex; gap:10px; margin-bottom:16px; flex-wrap:wrap;">
                                <button onclick="showWallpapers('default')" style="background:rgba(244,114,182,0.1); border:1px solid rgba(244,114,182,0.2); border-radius:12px; padding:8px 16px; color:#e0e7ff; cursor:pointer;">🏠 Базовые</button>
                                <button onclick="showWallpapers('colors')" style="background:rgba(244,114,182,0.1); border:1px solid rgba(244,114,182,0.2); border-radius:12px; padding:8px 16px; color:#e0e7ff; cursor:pointer;">🎨 Цветовые</button>
                                <button onclick="showWallpapers('gallery')" style="background:rgba(244,114,182,0.1); border:1px solid rgba(244,114,182,0.2); border-radius:12px; padding:8px 16px; color:#e0e7ff; cursor:pointer;">📸 Из галереи</button>
                            </div>
                            <div id="wallpaperGrid" class="wallpaper-grid"></div>
                        `;
                    showWallpapers('default');
                }
            };

            window.backToStore = function() {
                document.getElementById('appPage').style.display = 'none';
                document.getElementById('storeGrid').style.display = 'grid';
            };

            const defaultWallpapers = [
                { name: 'Тёмная ночь', gradient: 'radial-gradient(circle at 30% 40%, #1a1e2c, #0b0d14)' },
                { name: 'Рассвет', gradient: 'linear-gradient(135deg, #f472b6, #fb923c)' },
                { name: 'Море', gradient: 'linear-gradient(135deg, #06b6d4, #3b82f6)' },
                { name: 'Лес', gradient: 'linear-gradient(135deg, #22c55e, #0d9488)' },
                { name: 'Закат', gradient: 'linear-gradient(135deg, #ef4444, #f97316)' },
                { name: 'Лаванда', gradient: 'linear-gradient(135deg, #a855f7, #7c3aed)' }
            ];

            const colorWallpapers = [
                { name: 'Красный', color: '#ef4444' },
                { name: 'Оранжевый', color: '#f97316' },
                { name: 'Жёлтый', color: '#eab308' },
                { name: 'Зелёный', color: '#22c55e' },
                { name: 'Голубой', color: '#06b6d4' },
                { name: 'Синий', color: '#3b82f6' },
                { name: 'Фиолетовый', color: '#a855f7' },
                { name: 'Розовый', color: '#ec4899' },
                { name: 'Белый', color: '#ffffff' },
                { name: 'Чёрный', color: '#111111' }
            ];

            const testImg = 'data:image/svg+xml,' + encodeURIComponent(
                '<svg xmlns="http://www.w3.org/2000/svg" width="200" height="200"><rect width="200" height="200" fill="#f472b6"/><text x="100" y="110" font-size="30" fill="white" text-anchor="middle" font-family="Arial">POFO</text><text x="100" y="150" font-size="20" fill="rgba(255,255,255,0.6)" text-anchor="middle" font-family="Arial">📸</text></svg>'
                );

            window.showWallpapers = function(type) {
                const grid = document.getElementById('wallpaperGrid');
                if (!grid) return;

                if (type === 'colors') {
                    let html = colorWallpapers.map(c => `
                            <div class="wallpaper-option ${currentWallpaper === c.color ? 'active' : ''}" onclick="setWallpaper('${c.color}')" style="background:${c.color};">
                                <div class="wallpaper-name">${c.name}</div>
                                <div class="wallpaper-check"><i class="fas fa-check-circle"></i></div>
                            </div>
                        `).join('');
                    html += `
                            <div style="grid-column:1/-1; margin-top:8px; padding:12px; background:rgba(255,255,255,0.02); border-radius:14px; border:1px solid rgba(255,255,255,0.03);">
                                <label style="color:rgba(210,220,255,0.5); font-size:12px; display:block; margin-bottom:6px;">Введите цвет в формате #RRGGBB</label>
                                <div style="display:flex; gap:8px;">
                                    <input class="color-picker-input" id="hexColorInput" placeholder="#ff5733" style="flex:1;" onkeydown="if(event.key==='Enter'){applyHexColor();}">
                                    <button onclick="applyHexColor()" style="background:rgba(244,114,182,0.1); border:1px solid rgba(244,114,182,0.2); border-radius:12px; padding:8px 16px; color:#e0e7ff; cursor:pointer;">Применить</button>
                                </div>
                            </div>
                        `;
                    grid.innerHTML = html;
                } else if (type === 'gallery') {
                    const items = allPhotos.length > 0 ? allPhotos : [{ data: testImg, type: 'image' }];
                    grid.innerHTML = items.map((p, idx) => {
                        const isVideo = p.type === 'video';
                        const preview = isVideo ?
                            `<video src="${p.data}" muted loop preload="metadata" style="width:100%;height:100%;object-fit:cover;"></video><div class="video-play-icon"><i class="fas fa-play-circle"></i></div>` :
                            `<img src="${p.data}" style="width:100%;height:100%;object-fit:cover;">`;
                        return `
                                <div class="wallpaper-option ${currentWallpaper === p.data ? 'active' : ''}" onclick="setWallpaper('${p.data}')" style="background:rgba(0,0,0,0.3);">
                                    <div class="wallpaper-preview">${preview}</div>
                                    <div class="wallpaper-name">${isVideo ? '🎬 Видео' : '📸 Фото'} ${idx+1}</div>
                                    <div class="wallpaper-check"><i class="fas fa-check-circle"></i></div>
                                </div>
                            `;
                    }).join('');
                } else {
                    grid.innerHTML = defaultWallpapers.map(w => `
                            <div class="wallpaper-option ${currentWallpaper === w.gradient ? 'active' : ''}" onclick="setWallpaper('${w.gradient}')" style="background:${w.gradient};">
                                <div class="wallpaper-name">${w.name}</div>
                                <div class="wallpaper-check"><i class="fas fa-check-circle"></i></div>
                            </div>
                        `).join('');
                }
            };

            window.applyHexColor = function() {
                const input = document.getElementById('hexColorInput');
                let color = input.value.trim();
                if (!color.startsWith('#')) color = '#' + color;
                if (/^#[0-9A-Fa-f]{6}$/.test(color) || /^#[0-9A-Fa-f]{3}$/.test(color)) {
                    setWallpaper(color);
                    input.value = '';
                } else {
                    showToast('❌ Неверный формат. Используйте #RRGGBB');
                }
            };

            window.setWallpaper = function(data) {
                currentWallpaper = data;
                const screen = document.getElementById('screen');

                const oldVideo = document.getElementById('wallpaperVideo');
                if (oldVideo) oldVideo.remove();
                const oldOverlay = document.getElementById('wallpaperOverlay');
                if (oldOverlay) oldOverlay.remove();

                if (data && data.startsWith('data:video/')) {
                    screen.style.background = 'rgba(0,0,0,0.9)';

                    const video = document.createElement('video');
                    video.id = 'wallpaperVideo';
                    video.src = data;
                    video.autoplay = true;
                    video.loop = true;
                    video.muted = true;
                    video.style.cssText =
                        'position:absolute;top:50%;left:50%;min-width:100%;min-height:100%;width:auto;height:auto;transform:translate(-50%,-50%);z-index:0;object-fit:cover;opacity:0.8;';
                    video.style.pointerEvents = 'none';
                    screen.prepend(video);

                    const overlay = document.createElement('div');
                    overlay.id = 'wallpaperOverlay';
                    overlay.style.cssText =
                        'position:absolute;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,0.2);z-index:1;pointer-events:none;';
                    screen.prepend(overlay);

                    video.play().catch(() => {});
                } else if (data && data.startsWith('#')) {
                    screen.style.background = data;
                    screen.style.backgroundSize = 'cover';
                } else if (data && (data.startsWith('linear-gradient') || data.startsWith('radial-gradient'))) {
                    screen.style.background = data;
                    screen.style.backgroundSize = 'cover';
                } else if (data && data.startsWith('data:image')) {
                    screen.style.background = `url(${data}) center/cover no-repeat`;
                } else if (data) {
                    screen.style.background = data;
                    screen.style.backgroundSize = 'cover';
                }

                document.querySelectorAll('.wallpaper-option').forEach(el => el.classList.remove('active'));
                document.querySelectorAll('.wallpaper-option').forEach(el => {
                    const onclick = el.getAttribute('onclick');
                    if (onclick && onclick.includes(data)) {
                        el.classList.add('active');
                    }
                });
                showToast('✅ Обои установлены');
            };

            // ===== КЛИКЕР =====
            function initClicker() {
                updateClickerUI();
                checkDailyReset();
            }

            function checkDailyReset() {
                const today = new Date().toDateString();
                if (clickerRewardMode.lastClaimDate !== today) {
                    clickerRewardMode.available = true;
                    clickerRewardMode.clicksToday = 0;
                    clickerRewardMode.claimed = false;
                    clickerRewardMode.lastClaimDate = today;
                    document.getElementById('clickerReward').style.display = 'none';
                }
            }

            function updateClickerUI() {
                document.getElementById('clickerCoins').textContent = clickerCoins;
                document.getElementById('clickerTotalClicks').textContent = clickerTotalClicks;
                document.getElementById('clickerPerClick').textContent = clickerPerClick;
                document.getElementById('clickerPerClickDisplay').textContent = clickerPerClick;

                const mode = clickerMode;
                const area = document.getElementById('clickerArea');
                const display = document.getElementById('clickerDisplay');

                if (mode === 'normal') {
                    display.textContent = clickerCoins;
                    area.style.cursor = 'pointer';
                    updateShopUI();
                } else {
                    if (ownerPrivileges.infiniteClicker && currentUser && currentUser.role === 'Владелец') {
                        display.textContent = clickerRewardMode.clicksToday + ' / ∞';
                        area.style.cursor = 'pointer';
                    } else if (!clickerRewardMode.available) {
                        display.textContent = '⏳ Завтра';
                        area.style.cursor = 'default';
                    } else {
                        display.textContent = clickerRewardMode.clicksToday + ' / 100';
                        area.style.cursor = 'pointer';
                    }
                }
            }

            function updateShopUI() {
                const upgrades = [
                    { id: 'click1', cost: 25, label: '+1 клик' },
                    { id: 'click5', cost: 100, label: '+5 кликов' },
                    { id: 'autoclicker', cost: 250, label: 'Автокликер' },
                    { id: 'click10', cost: 500, label: '+10 кликов' },
                    { id: 'click50', cost: 2000, label: '+50 кликов' },
                    { id: 'click100', cost: 5000, label: '+100 кликов' },
                    { id: 'autoclicker2', cost: 10000, label: 'Автокликер v2' },
                    { id: 'click500', cost: 25000, label: '+500 кликов' }
                ];

                upgrades.forEach(u => {
                    const btn = document.getElementById('upgrade_' + u.id);
                    if (!btn) return;
                    if (clickerUpgrades[u.id]) {
                        btn.textContent = '✅ Куплено';
                        btn.className = 'shop-btn owned';
                        btn.closest('.shop-item').style.opacity = '0.6';
                    } else {
                        btn.textContent = 'Купить';
                        btn.className = 'shop-btn';
                        btn.closest('.shop-item').style.opacity = clickerCoins >= u.cost ? '1' : '0.4';
                    }
                });
            }

            window.buyUpgrade = function(id) {
                const costs = {
                    click1: 25,
                    click5: 100,
                    autoclicker: 250,
                    click10: 500,
                    click50: 2000,
                    click100: 5000,
                    autoclicker2: 10000,
                    click500: 25000
                };
                const effects = {
                    click1: () => { clickerPerClick += 1; },
                    click5: () => { clickerPerClick += 5; },
                    click10: () => { clickerPerClick += 10; },
                    click50: () => { clickerPerClick += 50; },
                    click100: () => { clickerPerClick += 100; },
                    click500: () => { clickerPerClick += 500; },
                    autoclicker: () => {
                        if (autoclickerInterval) clearInterval(autoclickerInterval);
                        autoclickerInterval = setInterval(() => {
                            clickerCoins += clickerPerClick;
                            clickerTotalClicks += clickerPerClick;
                            if (clickerMode === 'normal') {
                                document.getElementById('clickerDisplay').textContent = clickerCoins;
                            }
                            document.getElementById('clickerCoins').textContent = clickerCoins;
                            document.getElementById('clickerTotalClicks').textContent = clickerTotalClicks;
                        }, 1000);
                        showToast('🤖 Автокликер активирован!');
                    },
                    autoclicker2: () => {
                        if (autoclickerInterval) clearInterval(autoclickerInterval);
                        autoclickerInterval = setInterval(() => {
                            clickerCoins += clickerPerClick * 2;
                            clickerTotalClicks += clickerPerClick * 2;
                            if (clickerMode === 'normal') {
                                document.getElementById('clickerDisplay').textContent = clickerCoins;
                            }
                            document.getElementById('clickerCoins').textContent = clickerCoins;
                            document.getElementById('clickerTotalClicks').textContent = clickerTotalClicks;
                        }, 500);
                        showToast('🤖 Автокликер v2 активирован (2x скорость)!');
                    }
                };

                if (clickerUpgrades[id]) {
                    showToast('✅ Уже куплено');
                    return;
                }

                const cost = costs[id];
                if (clickerCoins < cost) {
                    showToast('❌ Недостаточно кликов!');
                    return;
                }

                clickerCoins -= cost;
                clickerUpgrades[id] = true;
                if (effects[id]) effects[id]();
                updateClickerUI();
                showToast('✅ Улучшение куплено!');
            };

            window.switchClickerMode = function(mode) {
                clickerMode = mode;
                document.getElementById('clickerModeNormal').classList.toggle('active', mode === 'normal');
                document.getElementById('clickerModeReward').classList.toggle('active', mode === 'reward');

                if (mode === 'reward') {
                    checkDailyReset();
                    if (!clickerRewardMode.available && !ownerPrivileges.infiniteClicker) {
                        document.getElementById('clickerDisplay').textContent = '⏳ Завтра';
                        document.getElementById('clickerArea').style.cursor = 'default';
                    } else {
                        document.getElementById('clickerDisplay').textContent = clickerRewardMode.clicksToday + (ownerPrivileges
                            .infiniteClicker ? ' / ∞' : ' / 100');
                        document.getElementById('clickerArea').style.cursor = 'pointer';
                    }
                    document.getElementById('clickerShop').style.display = 'none';
                } else {
                    document.getElementById('clickerDisplay').textContent = clickerCoins;
                    document.getElementById('clickerArea').style.cursor = 'pointer';
                    document.getElementById('clickerShop').style.display = 'grid';
                    updateShopUI();
                }
            };

            document.getElementById('clickerArea').addEventListener('click', function() {
                if (clickerMode === 'normal') {
                    clickerCoins += clickerPerClick;
                    clickerTotalClicks += clickerPerClick;
                    document.getElementById('clickerDisplay').textContent = clickerCoins;
                    document.getElementById('clickerCoins').textContent = clickerCoins;
                    document.getElementById('clickerTotalClicks').textContent = clickerTotalClicks;
                    updateShopUI();
                } else if (clickerMode === 'reward') {
                    if (ownerPrivileges.infiniteClicker && currentUser && currentUser.role === 'Владелец') {
                        clickerRewardMode.clicksToday += clickerPerClick;
                        document.getElementById('clickerDisplay').textContent = clickerRewardMode.clicksToday + ' / ∞';
                        showToast('♾️ +' + clickerPerClick + ' (бесконечный режим)');
                        return;
                    }
                    if (!clickerRewardMode.available) {
                        showToast('⏳ Вы уже получили награду сегодня. Приходите завтра!');
                        return;
                    }
                    const maxClicks = 100;
                    const newClicks = Math.min(clickerRewardMode.clicksToday + clickerPerClick, maxClicks);
                    clickerRewardMode.clicksToday = newClicks;
                    document.getElementById('clickerDisplay').textContent = newClicks + ' / 100';
                    if (newClicks >= maxClicks) {
                        document.getElementById('clickerReward').style.display = 'block';
                        showToast('🎉 100 кликов! Нажмите "Получить"!');
                    }
                }
            });

            window.claimReward = function() {
                if (!clickerRewardMode.available) {
                    showToast('⏳ Вы уже получили награду сегодня');
                    return;
                }
                if (clickerRewardMode.clicksToday < 100 && !ownerPrivileges.infiniteClicker) {
                    showToast('❌ Нужно накликать 100 кликов!');
                    return;
                }
                clickerCoins += 100;
                clickerRewardMode.available = false;
                clickerRewardMode.claimed = true;
                clickerRewardMode.lastClaimDate = new Date().toDateString();
                document.getElementById('clickerReward').style.display = 'none';
                document.getElementById('clickerDisplay').textContent = '⏳ Завтра';
                document.getElementById('clickerArea').style.cursor = 'default';
                updateClickerUI();
                showToast('💰 +100 POFO Coin получено!');
            };

            // ===== МОДАЛ =====
            let modalCallback = null;

            function openModal(title, label, placeholder, callback) {
                document.getElementById('modalTitle').textContent = title;
                document.getElementById('modalLabel').textContent = label;
                document.getElementById('modalInput').placeholder = placeholder || '...';
                document.getElementById('modalInput').value = '';
                document.getElementById('modalInput').type = 'text';
                document.getElementById('modalInput').maxLength = 999;
                document.getElementById('modalOverlay').classList.add('open');
                modalCallback = callback;
                setTimeout(() => document.getElementById('modalInput').focus(), 100);
            }

            window.closeModal = function() {
                document.getElementById('modalOverlay').classList.remove('open');
                modalCallback = null;
            };

            window.confirmModal = function() {
                const val = document.getElementById('modalInput').value;
                if (modalCallback) modalCallback(val);
                closeModal();
            };

            document.getElementById('modalInput').addEventListener('keydown', function(e) {
                if (e.key === 'Enter') confirmModal();
            });
            document.getElementById('modalOverlay').addEventListener('click', function(e) {
                if (e.target === this) closeModal();
            });

            // ===== ЖЕСТЫ =====
            const gesturePill = document.getElementById('gesturePill');
            let silentMode = false;

            gesturePill.addEventListener('click', function(e) {
                silentMode = !silentMode;
                if (silentMode) {
                    gesturePill.style.background = 'rgba(244, 114, 182, 0.08)';
                    gesturePill.style.borderColor = 'rgba(244, 114, 182, 0.2)';
                    gesturePill.innerHTML =
                        `<i class="fas fa-bell-slash"></i> Тишина включена <i class="fas fa-check-circle" style="color:#34d399;"></i>`;
                    document.getElementById('statusRight').innerHTML = '<i class="fas fa-bell-slash"></i> Тишина';
                    const silentToggle = document.getElementById('silentModeToggle');
                    if (silentToggle && silentToggle.classList.contains('off')) {
                        silentToggle.classList.remove('off');
                        silentToggle.classList.add('on');
                    }
                } else {
                    gesturePill.style.background = 'rgba(255, 255, 255, 0.02)';
                    gesturePill.style.borderColor = 'rgba(255, 255, 255, 0.02)';
                    gesturePill.innerHTML =
                        `<i class="fas fa-arrow-up"></i> Смахни вникуда · Тишина <i class="fas fa-bell-slash" style="opacity: 0.3;"></i>`;
                    updateStatusBar();
                    const silentToggle = document.getElementById('silentModeToggle');
                    if (silentToggle && silentToggle.classList.contains('on')) {
                        silentToggle.classList.remove('on');
                        silentToggle.classList.add('off');
                    }
                }
            });

            // ===== ДВОЙНОЙ ТАП =====
            const screenEl = document.getElementById('screen');
            let tapCount = 0;
            let tapTimer = null;

            screenEl.addEventListener('click', function(e) {
                if (e.target.closest('.app-item') || e.target.closest('.gesture-pill') ||
                    e.target.closest('.app-window') || e.target.closest('.modal-overlay') ||
                    e.target.closest('.note-viewer') || e.target.closest('.create-note-modal') ||
                    e.target.closest('.install-overlay') || e.target.closest('.account-menu') ||
                    e.target.closest('.app-lock-overlay') || e.target.closest('#ownerPanel') ||
                    e.target.closest('.app-pages') || e.target.closest('.media-viewer')) {
                    return;
                }
                tapCount++;
                if (tapCount === 1) {
                    tapTimer = setTimeout(() => { tapCount = 0; }, 350);
                } else if (tapCount === 2) {
                    clearTimeout(tapTimer);
                    tapCount = 0;
                    const appIcons = document.querySelectorAll('.app-icon');
                    appIcons.forEach((icon, idx) => {
                        icon.style.transition = 'all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1)';
                        icon.style.transform = 'scale(0.6)';
                        icon.style.opacity = '0.3';
                        setTimeout(() => {
                            icon.style.transform = 'scale(1)';
                            icon.style.opacity = '1';
                        }, 400 + idx * 30);
                    });
                    setRandomSpiral();
                    clockEl.textContent = randomTime();
                    screenEl.style.transition = 'background 0.15s';
                    screenEl.style.background = 'rgba(244, 114, 182, 0.04)';
                    setTimeout(() => { screenEl.style.background = ''; }, 250);
                    if (navigator.vibrate) navigator.vibrate(40);
                    showToast('✨ Сжатие!');
                }
            });

            // ===== СЖАТИЕ =====
            const dots = document.querySelectorAll('.compress-dot');
            let dotIndex = 0;
            document.querySelector('.compress-demo').addEventListener('click', function() {
                dots.forEach(d => d.classList.remove('active'));
                dotIndex = (dotIndex + 1) % dots.length;
                dots[dotIndex].classList.add('active');
                if (navigator.vibrate) navigator.vibrate(20);
                showToast('Сжатие: ' + (dotIndex + 1) + '/' + dots.length);
            });

            // ===== НАВИГАЦИЯ =====
            const navItems = document.querySelectorAll('.nav-item');
            navItems.forEach(item => {
                item.addEventListener('click', function() {
                    navItems.forEach(i => i.classList.remove('active'));
                    this.classList.add('active');
                });
            });

            // ===== ОБНОВЛЕНИЕ СПИРАЛИ =====
            setInterval(() => {
                if (spiralVisible) {
                    setRandomSpiral();
                    if (Math.random() > 0.5) clockEl.textContent = randomTime();
                }
            }, 15000);

            // ===== TOAST =====
            function showToast(text) {
                const existing = document.querySelector('.toast-notification');
                if (existing) existing.remove();
                const toast = document.createElement('div');
                toast.className = 'toast-notification';
                toast.textContent = text;
                document.body.appendChild(toast);
                setTimeout(() => { toast.classList.add('show'); }, 50);
                setTimeout(() => {
                    toast.classList.remove('show');
                    setTimeout(() => toast.remove(), 400);
                }, 1800);
            }

            // ===== ИНИЦИАЛИЗАЦИЯ =====
            updateAllDescriptions();
            updateStatusBar();

            setWallpaper(defaultWallpapers[0].gradient);

            allPhotos.push({ id: ++photoIdCounter, data: testImg, type: 'image', name: 'Тестовое фото' });
            myPhotos.push({ id: ++photoIdCounter, data: testImg, type: 'image', name: 'Тестовое фото' });
            renderGalleryGrid();

            notes.push({
                id: ++noteIdCounter,
                title: 'Добро пожаловать в POFO OS ???',
                content: 'Это ваша первая заметка. Вы можете её редактировать, удалять или создавать новые.',
                date: new Date().toLocaleDateString() + ' ' + new Date().toLocaleTimeString([], { hour: '2-digit',
                    minute: '2-digit' })
            });
            renderNotes();

            switchAppPage(1);

            // Экспорт функций
            window.openApp = openApp;
            window.closeApp = closeApp;
            window.openModal = openModal;
            window.closeModal = closeModal;
            window.confirmModal = confirmModal;
            window.openNote = openNote;
            window.closeNoteViewer = closeNoteViewer;
            window.deleteNote = deleteNote;
            window.saveNoteContent = saveNoteContent;
            window.createNote = createNote;
            window.openCreateModal = openCreateModal;
            window.closeCreateModal = closeCreateModal;
            window.filterNotes = filterNotes;
            window.renderNotes = renderNotes;
            window.selectLayer = selectLayer;
            window.toggleLayerVisibility = toggleLayerVisibility;
            window.deleteLayer = deleteLayer;
            window.selectLayerOnCanvas = selectLayerOnCanvas;
            window.toggleRoot = toggleRoot;
            window.editOSName = editOSName;
            window.editDeviceName = editDeviceName;
            window.editAppName = editAppName;
            window.showWallpapers = showWallpapers;
            window.setWallpaper = setWallpaper;
            window.openAppPage = openAppPage;
            window.backToStore = backToStore;
            window.installApp = installApp;
            window.applyHexColor = applyHexColor;
            window.toggleAccountMenu = toggleAccountMenu;
            window.loginAccount = loginAccount;
            window.logoutAccount = logoutAccount;
            window.renderUserList = renderUserList;
            window.toggleAppLock = toggleAppLock;
            window.changeLockPassword = changeLockPassword;
            window.disableLockWithPassword = disableLockWithPassword;
            window.lockKeyPress = lockKeyPress;
            window.lockConfirm = lockConfirm;
            window.openAdminPanel = openAdminPanel;
            window.openOwnerPanel = openOwnerPanel;
            window.executeAdminCommand = executeAdminCommand;
            window.toggleOwnerSetting = toggleOwnerSetting;
            window.switchAppPage = switchAppPage;
            window.buyUpgrade = buyUpgrade;
            window.switchClickerMode = switchClickerMode;
            window.claimReward = claimReward;
            window.openMediaViewer = openMediaViewer;
            window.closeMediaViewer = closeMediaViewer;

            document.addEventListener('click', function(e) {
                if (accountMenuOpen && !e.target.closest('.account-menu') && !e.target.closest('.nav-item') &&
                    !e.target.closest('.back-tap-hint')) {
                    toggleAccountMenu();
                }
            });

            document.getElementById('lockStatusItem').style.display = 'none';
            document.getElementById('changePassItem').style.display = 'none';
            document.getElementById('disableLockItem').style.display = 'none';

        })();
    </script>
</body>
</html>
