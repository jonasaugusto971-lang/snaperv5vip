<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SNIPER V5 - OFICIAL</title>
    <style>
        :root { --neon: #39FF14; --rosa: #ff00ea; --bg: #050801; --red: #ff3131; --gold: #FFD700; }
        body { background: var(--bg); color: var(--neon); font-family: 'Segoe UI', sans-serif; margin: 0; padding: 0; height: 100vh; overflow: hidden; }
        .screen { display: none; height: 100vh; flex-direction: column; }
        .active { display: flex; }

        /* TELA DE VENDA */
        .venda-container { flex: 1; display: flex; flex-direction: column; align-items: center; padding: 25px; text-align: center; overflow-y: auto; background: radial-gradient(circle at top, #0a1a05 0%, #050801 100%); }
        .logo { letter-spacing: 8px; color: #fff; margin-top: 20px; font-size: 2rem; }
        .logo span { color: var(--neon); text-shadow: 0 0 15px var(--neon); }
        .descricao-top { background: rgba(255,255,255,0.03); border: 1px solid #1a1a1a; padding: 15px; border-radius: 12px; margin: 15px 0; width: 100%; box-sizing: border-box; }
        .descricao-top h2 { color: var(--neon); font-size: 1rem; margin-top: 0; text-transform: uppercase; }
        .descricao-top p { color: #bbb; font-size: 0.85rem; line-height: 1.5; margin: 5px 0; }
        .tabela-precos { width: 100%; margin: 10px 0; border-collapse: collapse; }
        .tabela-precos td { padding: 8px; border-bottom: 1px solid #111; font-size: 0.9rem; }
        .plano-nome { color: #fff; text-align: left; font-weight: bold; }
        .plano-valor { color: var(--neon); text-align: right; font-weight: bold; }
        .btn-buy { background: var(--neon); color: #000; border: none; padding: 18px; border-radius: 8px; font-weight: 1000; width: 100%; cursor: pointer; text-transform: uppercase; font-size: 1rem; box-shadow: 0 0 20px rgba(57, 255, 20, 0.4); margin-top: 10px; }

        /* PAINEL VIP */
        .painel-compacto { height: 32vh; background: #000; border-bottom: 2px solid #1a1a1a; padding: 8px 12px; box-sizing: border-box; display: flex; flex-direction: column; justify-content: space-between; }
        .topo-info { display: flex; justify-content: space-between; align-items: center; }
        #relogio { font-family: 'Courier New', monospace; font-size: 1.3rem; color: #fff; text-shadow: 0 0 8px var(--neon); font-weight: bold; background: #0a0a0a; padding: 2px 8px; border-radius: 5px; border: 1px solid #111; }
        .btn-sair { background: none; border: 1px solid var(--red); color: var(--red); font-size: 0.6rem; padding: 4px 8px; border-radius: 4px; cursor: pointer; text-transform: uppercase; font-weight: bold; }
        .lista-horarios { background: #0a0a0a; border-radius: 8px; padding: 5px; overflow-y: auto; flex-grow: 1; margin: 8px 0; border: 1px solid #111; }
        .horario-item { display: flex; justify-content: space-between; align-items: center; font-size: 0.75rem; padding: 6px 0; border-bottom: 1px solid #111; }
        .badge { font-weight: bold; padding: 1px 4px; border-radius: 3px; font-size: 0.55rem; text-transform: uppercase; }
        .b-prot { background: #fff; color: #000; margin-right: 3px; }
        .b-alvo { border: 1px solid var(--neon); color: var(--neon); }
        .b-rosa { border: 1px solid var(--rosa); color: var(--rosa); box-shadow: 0 0 5px var(--rosa); }
        .btn-gerar { background: #11
