local OrionLib = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Orion/main/source'))()

-- Lista Completa de Frutas do Blox Fruits (Exemplo)

local frutasDisponiveis = {
    "Bomb",
    "Spike",
    "Chop",
    "Spring",
    "Kilo",
    "Smoke",
    "Spin",
    "Flame",
    "Falcon",
    "Ice",
    "Sand",
    "Dark",
    "Revive",
    "Diamond",
    "Light",
    "Love",
    "Rubber",
    "Barrier",
    "Kitsune",  -- Adicionada a fruta Kitsune[^1^][6]
    "Leopard",  -- Adicionada a fruta Leopard[^2^][4]
    "Phoenix",  -- Adicionada a fruta Phoenix[^3^][9]
    "Spirit",   -- Adicionada a fruta Spirit[^4^][15]
    -- Adicione mais frutas conforme necessário
}

-- Função para adicionar fruta ao inventário (exemplo)
local function adicionarFrutaAoInventario(nomeDaFruta)
    print("Adicionando " .. nomeDaFruta .. " ao inventário.")
    -- Aqui você adicionaria a lógica para adicionar a fruta ao inventário
end

-- Função para exibir o menu de frutas e escolher uma fruta
local function exibirMenuDeFrutas()
    print("Escolha uma fruta para adicionar ao seu inventário:")
    for indice, fruta in ipairs(frutasDisponiveis) do
        print(indice .. ". " .. fruta)
    end
    print("Digite o número da fruta que deseja adicionar:")
    
    local escolha = io.read() -- Lê a escolha do usuário
    local indiceEscolhido = tonumber(escolha)
    
    if indiceEscolhido and frutasDisponiveis[indiceEscolhido] then
        adicionarFrutaAoInventario(frutasDisponiveis[indiceEscolhido])
    else
        print("Escolha inválida. Tente novamente.")
        exibirMenuDeFrutas() -- Mostra o menu novamente se a escolha for inválida
    end
end

-- Iniciar o menu de frutas
exibirMenuDeFrutas()
