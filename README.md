# FFHACK — Free Fire hack via depuração Wi‑Fi (ADB)

Hack de Free Fire (Free Fire MAX e Lite) que roda **por fora do jogo**:
nenhum arquivo entra na pasta do jogo, nenhum processo injetado na memória dele.
Tudo é feito por ADB sobre a **depuração Wi‑Fi** do celular e o controle sai do
**Termux** (no celular) ou **CMD** (no PC).

## Arquivos

| Arquivo | O que é |
|---|---|
| `FFHACK` | O programa inteiro num arquivo único. Abaixo da linha `:SECAO_CMD` está a metade CMD — não corte nada, é o mesmo arquivo nos dois lados. |
| `index.html` | Página pública (GitHub Pages) com instruções e botão de download. |

## Rodar no celular (Termux)

```bash
pkg install -y android-tools curl wget jq
curl -O https://roughendev123.github.io/ffhack/FFHACK
sed -i 's/\r$//' FFHACK
bash FFHACK
```

## Rodar no PC (CMD)

```bat
curl -o FFHACK.bat https://roughendev123.github.io/ffhack/FFHACK
FFHACK.bat
```

## Primeiro uso

No primeiro rodar ele cria o administrador `roughen` — escolha a senha ali.
Depois:

1. Celular: ative Depuração USB e ligue por cabo uma vez; no PC rode `adb tcpip 5555` e veja o IP do celular.
2. No menu, item **[1] Conectar**: digite `IP:5555`.
3. Item **[19]**: cole o Bin ID e a Master Key do jsonbin.io (crie um bin com `{"usuarios":[]}`). Cada terminal configura uma vez; quem roda depois só faz login.
4. Item **[20]**: crie os usuários que vão ter acesso ao hack completo.

## Funções

Tiro na cabeça / pescoço / acima da cabeça, autotiro, ESP, WALL, restaurar visão,
FPS 120, antireco, velocidade, voo, moedas/skins (root), modo Fantasma
(esconde a depuração do ADB), calibração de mira e atualização remota do código.

## Aviso honesto

Wall real (ver através de parede sólida) e ESP através de muros exigem overlay
injetado — esta versão faz zoom + brilho. Alturas de mira são estimativas de tela
(ajuste em [4] Calibrar ou nas constantes Y do topo do arquivo).
