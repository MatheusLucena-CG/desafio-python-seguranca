# 👾 Desafio: Simulando Malwares com Python

Fala galera! Criei esse repositório para colocar os testes práticos que fiz no curso sobre malwares. A ideia aqui foi ver como funciona um Ransomware e um Keylogger de verdade, mas tudo rodando num ambiente 100% controlado no meu próprio PC, só para fins de estudo mesmo. Achei a parte de segurança da informação muito da hora de testar na prática.

## 📁 O que tem aqui?

Eu fiz dois scripts simples em Python:

1. **`ransomware_simples.py`:** Esse código usa a biblioteca `cryptography`. Ele gera uma chave de segurança, pega um arquivo de texto de teste (`meus_segredos.txt`), criptografa tudo e ainda larga um arquivo `RESGATE.txt` na pasta. Deu pra entender certinho a lógica de como os dados são sequestrados.
2. **`meu_keylogger.py`:** Esse usa o módulo `pynput`. Ele fica rodando de forma furtiva (tirei os prints da tela pra não dar pala) e salva tudo que eu digito num arquivo `.txt`. Eu ia colocar o código de mandar por email, mas como as caixas de email bloqueiam muito, foquei em fazer o registro local funcionar bem.

## 🛡️ Como a gente se defende disso no mundo real?

Rodando os códigos, deu pra perceber que é muito fácil a gente dar mole e executar um arquivo malicioso. Anotei algumas coisas importantes sobre prevenção:

* **Conscientização:** A regra número um. O meu ransomware só roda se a pessoa for lá e executar. Se o usuário não clica em links suspeitos ou arquivos disfarçados de PDF, o ataque já falha no início.
* **Backup Sempre:** Se você toma um ransomware de verdade, quase nunca dá pra quebrar a criptografia. O único jeito seguro de não perder tudo é ter backup na nuvem ou em um HD externo que não fica sempre conectado.
* **Antivírus e Defender:** Só de tentar instalar a biblioteca pynput o Windows já fica meio desconfiado. Manter isso atualizado ajuda a barrar comportamentos esquisitos.
* **Firewall:** Muito importante pra bloquear um keylogger, por exemplo, de tentar enviar o arquivo com as senhas capturadas pra um servidor de fora pela internet.

## 🛠️ Como testar no seu PC

Se alguém quiser testar (em ambiente seguro!):
1. Tenha o Python instalado.
2. Instale as bibliotecas usando no terminal: `pip install cryptography pynput`
3. Crie um arquivo qualquer com o nome `meus_segredos.txt` na mesma pasta.
4. Rode os scripts e veja a mágica (ou o caos) acontecer!
