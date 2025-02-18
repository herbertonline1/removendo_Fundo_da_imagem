Nesse projeto você tem a possibilidade de remover fundo das fotos e salva automaticamente.

# Importando a biblioteca rembg
# OBS: Precisa instalar o rembg "pip install rembg"
from rembg import remove

from PIL import Image


# Caminho onde a foto esta salva
caminho_imagem = r'C:\Users\herbert.santos\Desktop\Nova pasta\download.jpg'
#Caminho onde a foto vai ser salva, OBS: Mudar o nome e a extesão da foto para .png
caminho_imagem_com_bg_removido = r'C:\Users\herbert.santos\Desktop\Nova pasta\download_sem_bg.png'
# Aqui vamos abrir a foto 
imagem_arquivo = Image.open(caminho_imagem) 
# Aqui vamos remover o fundo da foto
imagem_arquivo_sem_bg = remove(imagem_arquivo)
#Aqui vamos salvar a foto que foi removida o fundo
imagem_arquivo_sem_bg.save(caminho_imagem_com_bg_removido)
