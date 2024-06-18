## CASO DE ESTUDO 1 
Você trabalha na biblioteca da sua cidade, fazendo o suporte de TI e gerenciando o banco de 
dados da biblioteca. A biblioteca gerencia seu acervo utilizando uma tabela Livros. Nela estão 
cadastrados o título, autor, gênero e data da publicação dos livros da biblioteca. Analise as 
situações abaixo, gerando comandos SQL para realizar as atividades solicitadas a você. Os 
comandos de criação da tabela e inserção dos registros estão no material de apoio. 



#
### Questão 1
A biblioteca quer descobrir os gêneros mais populares para promover os livros corretos. Liste 
os gêneros e a quantidade contida em cada gênero, limitando a pesquisa aos cinco gêneros 
com mais livros na biblioteca. A coluna que contém a número de livros no gênero deve ser 
mostrada como "Quantidade”.

### Resposta
```sql
SELECT LV.GENERO, COUNT(*) AS QUANTIDADE 
FROM LIVROS LV
GROUP BY LV.GENERO
ORDER BY 2 DESC
FETCH FIRST 5 ROWS ONLY;
```

### Saída no Oracle SQL Developer
![image](https://github.com/JhonatanSantAna/ImersaoOracleSQL_DBAOCM/assets/107253206/d915efca-b2fc-45b3-bd80-175ca3ab51eb)
#
