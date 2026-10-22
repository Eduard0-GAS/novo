# Bônus da Aula 12 — meu primeiro workflow no GitHub Actions

Atividade opcional de Engenharia de Software II (IFSC Caçador).
Ela não é obrigatória e não vale presença. É para quem quer ver um workflow rodando de verdade.

## O que tem aqui

- `calculadora.py`: um programa pequeno em Python, com 4 funções
- `test_calculadora.py`: testes automatizados (pytest) para essas funções
- `requirements.txt`: as dependências (só o pytest)
- `.github/workflows/ci.yml`: o workflow de integração contínua

## Passo a passo

1. Crie um repositório novo e **público** no seu GitHub (pode chamar de `es2-aula12`).
2. Envie para a branch `main` todos os arquivos desta pasta, **incluindo a pasta oculta `.github`**.
   Dica: se for pelo navegador, use "Add file > Upload files" e arraste a pasta inteira.
3. Abra a aba **Actions** do repositório. O workflow "CI" deve rodar sozinho e terminar com ✅.
4. Crie uma branch nova (por exemplo, `quebra-teste`). Edite `test_calculadora.py` e troque um valor esperado por um errado, como `assert somar(2, 3) == 6`.
5. Faça o commit e abra um **Pull Request** para a `main`. Veja o ❌ aparecer na seção "Checks" do Pull Request e abra o log para achar o teste que falhou.
6. Na mesma branch, corrija o teste e faça um novo commit. O workflow roda de novo e volta para ✅.
7. Cole o link do seu repositório na pergunta bônus do exercício no SIGAA.

## Se algo der errado

- O workflow não aparece na aba Actions: confira se o arquivo está em `.github/workflows/ci.yml` (o caminho precisa ser exatamente esse).
- Erro "No module named pytest": confira se o `requirements.txt` foi enviado.
- Dúvidas: pergunte pelo SIGAA.
