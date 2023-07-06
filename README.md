import math

class Planeta:
    def __init__(self, nome, distancia_media_ao_sol):
        self.nome = nome
        self.distancia_media_ao_sol = distancia_media_ao_sol

class SistemaSolar:
    def __init__(self):
        self.planetas = []

    def adicionar_planeta(self, planeta):
        self.planetas.append(planeta)

    def calcular_distancia(self, planeta1, planeta2):
        distancia = abs(planeta1.distancia_media_ao_sol - planeta2.distancia_media_ao_sol)
        return distancia

# Criação dos planetas
mercurio = Planeta("Mercúrio", 57.9)
venus = Planeta("Vênus", 108.2)
terra = Planeta("Terra", 149.6)
marte = Planeta("Marte", 227.9)
jupiter = Planeta("Júpiter", 778.3)
saturno = Planeta("Saturno", 1427.0)
urano = Planeta("Urano", 2871.0)
netuno = Planeta("Netuno", 4497.1)

# Criação do sistema solar
sistema_solar = SistemaSolar()
sistema_solar.adicionar_planeta(mercurio)
sistema_solar.adicionar_planeta(venus)
sistema_solar.adicionar_planeta(terra)
sistema_solar.adicionar_planeta(marte)
sistema_solar.adicionar_planeta(jupiter)
sistema_solar.adicionar_planeta(saturno)
sistema_solar.adicionar_planeta(urano)
sistema_solar.adicionar_planeta(netuno)

# Exemplo de uso do simulador
distancia_terra_marte = sistema_solar.calcular_distancia(terra, marte)
print(f"A distância média entre a Terra e Marte é de {distancia_terra_marte} milhões de quilômetros.")
