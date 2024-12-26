print("Bem-vindo ao Urso Hub!")
print("Carregando funcionalidades...")

function saudacao(nome)
    print("Olá, " .. nome .. "! Seja bem-vindo ao Urso Hub!")
end

function menu()
    print("\nvfly:")
    print("1 - Receber saudação")
    print("2 - Fazer um cálculo simples")
    print("3 - Sair")

    local escolha = io.read("*n")
    return escolha
end

function calcular(a, b)
    print("A soma de " .. a .. " e " .. b .. " é " .. (a + b))
end

local rodando = true

while rodando do
    local opcao = menu()

    if opcao == 1 then
        print("Digite seu nome:")
        local nome = io.read()
        saudacao(nome)
    elseif opcao == 2 then
        print("Digite o primeiro número:")
        local num1 = io.read("*n")
        print("Digite o segundo número:")
        local num2 = io.read("*n")
        calcular(num1, num2)
    elseif opcao == 3 then
        print("Saindo do Urso Hub... Até a próxima!")
        rodando = false
    else
        print("Opção inválida! Tente novamente.")
    end
end
