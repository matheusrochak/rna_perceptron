# Reconhecimento de Dígitos com RNA Perceptron de Monocamada.

Este projeto implementa uma Rede Neural Artificial (RNA) do tipo **Perceptron de uma camada** para reconhecer os dígitos `0` e `1` a partir de uma matriz de pixels **4x4**.

## 🚀 Tecnologias Utilizadas
- Python 3
- NumPy

## 📌 Funcionalidades
- Treinamento de um Perceptron com pesos ajustáveis.
- Armazenamento dos pesos após o treinamento.
- Teste com novos padrões de entrada.
- Cálculo da taxa de acerto.

## 📂 Estrutura do Projeto
```
📁 rna_perceptron          
│── 📄 trabalho_p1_inteligenciacomputacional_2024_2.py    # Código principal

```

## ⚙️ Instalação
### 1️⃣ Clonar o Repositório
```sh
git clone https://github.com/seu-usuario/rna_perceptron.git
cd rna_perceptron
```
### 2️⃣ Instalar Dependências
Certifique-se de ter o Python e o NumPy instalados:
```sh
pip install numpy
```

## 🎯 Como Executar o Código

### 🔹 Treinamento da RNA
Execute o script principal para treinar o modelo:
```sh
python trabalho_p1_inteligenciacomputacional_2024_2.py --train
```
Isso irá ajustar os pesos da rede e salvá-los no arquivo `treinado_pesos.npy`.

### 🔹 Teste da RNA
Para testar o modelo com novos padrões, execute:
```sh
python trabalho_p1_inteligenciacomputacional_2024_2.py --test
```
Isso apresentará **10 novos padrões** e calculará a **taxa de acerto**.

## 📊 Exemplo de Saída
```sh
Total de testes: 10
Acertos: 9
Taxa de acerto: 9.0%
```

## 🧠 Explicação Técnica
### ➤ Ativação e Ajuste de Pesos
O Perceptron usa a **função sigmoide** para ativação:
```python
def sigmoid(x):
    return 1 / (1 + np.exp(-x))
```
E a atualização dos pesos ocorre pelo **Gradiente Descendente**:
```python
pesos += taxa_aprendizado * entrada.T.dot(erro * derivada_sigmoid(saida))
```

### ➤ Teste de Novos Padrões
Os novos padrões são apresentados à rede, e a saída é convertida em `0` ou `1`:
```python
previsao = 1 if saida_teste > 0.5 else 0
```
A taxa de acerto é calculada com:
```python
taxa_acerto = (acertos / total_testes) * 10
```

## 🏆 Contribuição
Sinta-se à vontade para contribuir!
1. Faça um fork do repositório
2. Crie uma nova branch (`git checkout -b feature/minha-mudanca`)
3. Commit suas mudanças (`git commit -m 'Adicionando nova feature'`)
4. Envie para o repositório (`git push origin feature/minha-mudanca`)
5. Abra um **Pull Request**

---

Feito com ❤️ por [Matheus Rocha](https://github.com/matheusrochak) 🚀

