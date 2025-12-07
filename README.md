<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>MecaniAI — Diagnóstico de máquinas industriales</title>
<style>
  :root{
    --bg:#f4f7fb; --card:#fff; --accent:#0b75ff; --muted:#6b7280;
    --success:#0f766e; --danger:#dc2626;
  }
  *{box-sizing:border-box}
  body{
    margin:0;font-family:Inter, "Segoe UI", Roboto, Arial, sans-serif;
    background:var(--bg); color:#0f172a;
  }
  header{
    background:linear-gradient(90deg,#fff 0%, #f7fbff 100%);
    border-bottom:1px solid rgba(15,23,42,0.06);
    padding:20px;
    text-align:center;
  }
  header h1{margin:0;font-size:1.6rem;letter-spacing:0.4px;}
  header p{margin:6px 0 0;color:var(--muted);font-size:0.95rem}

  .wrap{max-width:960px;margin:28px auto;padding:0 16px}
  .grid{display:grid;grid-template-columns:1fr 420px;gap:20px}
  @media (max-width:880px){.grid{grid-template-columns:1fr}}
  .card{background:var(--card);border-radius:12px;padding:18px;box-shadow:0 6px 18px rgba(2,6,23,0.04)}
  label{display:block;font-weight:600;margin-bottom:8px}
  select,input,textarea{width:100%;padding:10px;border-radius:8px;border:1px solid #dbe6f5;background:#fff;font-size:0.95rem}
  textarea{min-height:120px;resize:vertical}
  .row{display:flex;gap:10px}
  .row > *{flex:1}
  button.primary{
    width:100%;padding:12px;border-radius:10px;border:0;background:var(--accent);color:#fff;font-weight:700;font-size:1rem;
    cursor:pointer;
  }
  button.ghost{background:transparent;border:1px solid #e5eefc;color:var(--accent);padding:10px;border-radius:10px}
  .result{margin-top:12px;border-left:6px solid var(--accent);padding:12px;background:#f0f8ff;border-radius:8px}
  .tag{display:inli
