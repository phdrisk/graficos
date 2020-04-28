## PIE ####

1) SELECIONE OS DADOS
  
  a) dados <- data %>%  filter(infeccao_hosp == 1) : ja selecione os dados que serao criados
  
    - idade <-table( dados$infeccao_hosp,dados$idade)
    
  ou
  
  b) idade <-table( dados$infeccao_hosp,dados$idade)[1,] : selecione a primeira linha da tabela criada

            0    1    2    3    4    5    6    7    8    9
        0   57  236  436 1057 2557 4462 5825 7044 4576  823
        1   29  102  207  466 1281 2210 3003 3531 2512  482



2) CASO SEJA UM FATOR, AS COLUNAS PODEM SER RENOMEADAS
 - names(idade)<- c("[10-18]","[19-25]","[26-30]","[31-40]","[41-50]","[51-60]","[61-70]","[71-80]","[81-90]","[91-")
 
3) CRIE OS LABELS
pielabels <- sprintf("%s", names(idade))

-CRIE O GRAFICO

    - pie(idade,
      labels=round(100*browsers/sum(idade),2), 
      clockwise=TRUE, 
      col=rainbow(lenght(idade)
      ,border="white", radius=0.9, cex=0.8,
      main="Percentage Share of Internet Browser usage"
      )

-INCLUA A LEGENDA EXTERNA   

      legend("topleft",legend=pielabels,bty="n" 
       ,fill=rainbow(lenght(idade), y.intersp = .7
       )   
