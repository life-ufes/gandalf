# Gandalf, the enviroment wizard 

Este repositório apenas mantém um arquivo de configuração `yml` para criação de um *environment* de desenvolvimento Python dentro do `conda`. Obviamente, o nome do *environment* é `gandalf` :mage_man:

<p align="center">
<img src="./assets/gandalf.png" alt="Gandalf" width=100% height=100%/>
</p>

## Como usar

Para criar o *environment* `gandalf`, basta executar o comando abaixo:

```bash
conda env create -f gandalf.yml
```

Para ativar o *environment* `gandalf`, basta executar o comando abaixo:

```bash
conda activate gandalf
```

Obviamente, é necessário que o `conda` esteja instalado na sua máquina. Caso não esteja, você pode instalar o `conda` através do [Miniconda](https://docs.conda.io/en/latest/miniconda.html).

## Como atualizar este arquivo
Caso você atualize algum pacote do *environment* `gandalf` e conclua que é necessário atualizar este repositório para que os códigos desenvolvidos no laboratório continuem a funciona, você deve fazer o seguite. 

1. Ative o *environment* `gandalf` como descrito anteriormente
2. Atualize ou instale um pacote dentro do *environment*
3. Execute o comando a seguir para gerar um novo arquivo `yml` com as atualizações feitas:

```bash
conda env export | grep -v "^prefix: " > gandalf.yml
```

4. Faça um pull request para este repositório com o arquivo `gandalf.yml` atualizado

## Pacotes instalados
Existem diversos pacotes instalados no *environment* `gandalf`. Para saber quais são, basta olhar o arquivo `gandalf.yml` ou executar o comando a seguir com o *environment* ativado:

```bash
conda list
```

## Dependências

||||| 
|------------------|--------------|---------------------|-------------|
| pretrainedmodels | tensorboard  | scikit-learn        | sacred      |
| joblib           | tensorboardX | imgaug              | gradio      |
| transformers     | torch        | opencv-python       | onnx        |
| praw             | torchvision  | pandas              | jupyter-lab |
| torchsummary     | matplotlib   | pillow              | glob2       |
| pytest           | scipy        | tqdm                |             |
| seaborn          | numpy        | python-telegram-bot |             | 


## Por que Gandalf?
Primeiramente, você não deveria estar fazendo essa pergunta! Mas, uma vez que chegou até aqui...

Gandalf é um mago do universo de J.R.R. Tolkien. Ele é conhecido por ser um dos mais poderosos magos da Terra Média e por ser um dos membros da Sociedade do Anel. Além disso, ele é conhecido por ser um mago sábio e um grande conselheiro. Portanto, nada mais justo do que nomear o *environment* de desenvolvimento Python do laboratório com o nome de Gandalf, o mago sábio e conselheiro :mage_man:











