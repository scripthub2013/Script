-- Chave de script, apenas para premium, você pode deixar em branco se não for premium
script_key = "" -- premium apenas, você pode deixar em branco se não for

getgenv().Shutdown = false -- Ative se estiver farmando contas em massa

-- Configurações principais do script
getgenv().Configs = {
    -- Equipe do jogador
    ["Team"] = "pirates", -- Equipe a ser usada no jogo

    -- Configurações de melhoria de FPS
    ["FPS Boost"] = {
        ["Enable"] = true, -- Ativa o aumento de FPS
        ["FPS Cap"] = 30,  -- Limite de FPS (30 FPS aqui)
    },

    -- Configurações de farm de drops de chefes
    ["Farm Boss Drops"] = {
        ["Enable"] = false, -- Desativa o farm de drops de chefes
        ["When x2 Exp Expired"] = false -- Desativa quando o x2 XP expira
    },

    -- Configurações de 'Hop' (apenas para premium)
    ["Hop"] = { -- premium apenas
        ["Enable"] = true, -- Ativa a função de "Hop"
        ["Hop Find Tushita"] = true, -- Ativa busca por Tushita
        ["Hop Find Valkyrie Helm"] = true, -- Ativa busca por Valkyrie Helm
        ["Hop Find Mirror Fractal"] = true, -- Ativa busca por Mirror Fractal
        ["Hop Find Darkbeard"] = true, -- Ativa busca por Darkbeard (para guitarra de crânio)
        ["Hop Find Soul Reaper"] = true, -- Ativa busca por Soul Reaper (para CDK)
        ["Hop Find Mirage"] = true, -- Ativa busca por Mirage (para puxar alavanca)
        ["Find Fruit"] = true, -- Ativa a busca por frutas (acima de 1M) para abrir a porta de Swan e acessar o terceiro mar
    },

    -- Configurações de farm de Maestria
    ["Farm Mastery"] = {
        ["Enable"] = true, -- Ativa o farm de maestria
        ["Farm Mastery Weapons"] = {"Sword", "Gun", "Blox Fruit"}, -- Prioridade de farm de armas (Espada, Arma de Fogo, Blox Fruit)
        ["Swords To Farm"] = {"Cursed Dual Katana"}, -- Espadas a serem farmadas
        ["Guns To Farm"] = {"Skull Guitar"}, -- Armas a serem farmadas
        ["Mastery Health (%)"] = 40 -- Porcentagem de saúde para farm de Blox Fruit e Armas
    },

    -- Configurações de farm geral
    ["Farm Config"] = {
        ["First Farm At Sky"] = true, -- Começar o farm no céu
        ["Farm Bone Get x2 Exp"] = true -- Farmar ossos para x2 Exp
    },

    -- Configurações de rastreamento de estatísticas
    ["Trackstat"] = {
        ["Enable"] = false, -- Desativa o rastreamento de estatísticas
        ["Key"] = "", -- Obter chave de rastreamento de um site (xerohub.click)
        ["Device"] = "test" -- Nome do dispositivo (pode ser qualquer nome)
    },

    -- Ações automáticas (auto)
    ["Auto Spawn rip_indra"] = true, -- Ativa o spawn automático de rip_indra
    ["Auto Spawn Dough King"] = true, -- Ativa o spawn automático do Dough King
    ["Auto Pull Lever"] = true, -- Pegar Engrenagem Mirage
    ["Auto Collect Berry"] = true, -- Ativa a coleta automática de Berry
    ["Auto Evo Race"] = true, -- Ativa a evolução automática de Raça
    ["Awaken Fruit"] = true, -- Ativa o despertar da fruta
    ["Rainbow Haki"] = true, -- Ativa o Haki do Arco-íris
    ["Hop Player Near"] = true, -- Ativa a função de "Hop" se houver jogadores por perto
    ["Skull Guitar"] = false, -- Ativa a função para obter a Skull Guittar
    ["Cursed Dual Katana"] = true, -- Ativa a função para obter a Cursed Dual Katana
    ["Switch Melee"] = true, -- Ativa a troca de armas corpo a corpo
    ["Eat Fruit"] = "", -- Deixe em branco para nenhum, coloque o nome da fruta como "Smoke Fruit", "T-Rex Fruit", etc.
    ["Snipe Fruit"] = "", -- Deixe em branco para nenhum, coloque o nome da fruta para "Comprar"
    ["Lock Fragment"] = 30000, -- Define o limite de fragmentos (30000)
    ["Buy Stuffs"] = true -- Compra itens como Buso, Geppo, Soru, Ken Haki, etc.
}

repeat task.wait() pcall(function() loadstring(game:HttpGet("https://raw.githubusercontent.com/Xero2409/XeroHub/refs/heads/main/kaitun.lua"))() end) until getgenv().Check_Execute
