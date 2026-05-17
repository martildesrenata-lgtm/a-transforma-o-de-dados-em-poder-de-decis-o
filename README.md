import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Criando dados que representam o mercado atual
# Comparando empresas 'Tradicionais' vs 'Digitalizadas' (que usam IA e Cloud)
dados = {
    'Ano': [2020, 2021, 2022, 2023, 2024, 2020, 2021, 2022, 2023, 2024],
    'Faturamento_Bilhoes': [100, 105, 108, 110, 112, 100, 120, 145, 180, 230],
    'Tipo_Empresa': ['Tradicional']*5 + ['Digitalizada (IA/Cloud)']*5
}

df = pd.DataFrame(dados)

# Criando o gráfico de impacto
plt.figure(figsize=(12, 6))
sns.lineplot(data=df, x='Ano', y='Faturamento_Bilhoes', hue='Tipo_Empresa', marker='o', linewidth=3)

# Estilização para o LinkedIn
plt.title('O Impacto Digital: Tradicional vs. Digitalizada (IA & Cloud)', fontsize=16)
plt.ylabel('Faturamento (em Bilhões)', fontsize=12)
plt.xlabel('Ano', fontsize=12)
plt.grid(True, linestyle='--', alpha=0.6)

# Salvando a imagem para o seu post
plt.savefig('impacto_digital.png', dpi=300, bbox_inches='tight')
plt.show()

print("Gráfico 'impacto_digital.png' gerado com sucesso!")
# a-transforma-o-de-dados-em-poder-de-decis-o
