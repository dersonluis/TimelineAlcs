# TimelineAlcs para QlikSense Extension

O gráfico **TimelineAlcs** é um update do projeto	[*Qlik Sense Extension Timeline*](https://github.com/ralfbecher/QlikSense_Extension_Timeline) com foco em projetos.



## PRINCIPAIS CARACTERÍSTICAS:
- Personalização do *StyleCSS*
- Ordenação das fases de projeto na seguinte sequência: *Plan >> Forecast >> Actual*
- Agrupamento ordenado pelo ID (Dimensão0)

[![](https://github.com/dersonluis/TimelineAlcs/blob/master/timelineAlcs.png)](https://github.com/dersonluis/TimelineAlcs/blob/master/timelineAlcs.png)



## ENTRADAS DE DADOS - QlikSense
*TimelineAlcs* é populado com, basicamente 05 dimensões e 03 medidas (Sem alterações do original).

* Veja aplicativo exemplo: [TimelineAlcs](https://github.com/dersonluis/TimelineAlcs/blob/master/TimelineAlcs.qvf)

      DIMENSÃO 1 = ID
      DIMENSÃO 2 = Tipos de fases do Projeto (Plan, Forecast e Actual)
   	  DIMENSÃO 3 = Data início
  	  DIMENSÃO 4 = Data término (Opcional - null se omitido)
   	  DIMENSÃO 5 = Tipo Item (box (default), point, range, background)
    
   	  MEDIDA 1 = Legenda
   	  MEDIDA 2 = Cor
   	  MEDIDA 3 = Agrupamento (opcional)



## EXEMPLO FORMATO DE DADOS

```
[alcs]:
    Load * Inline
    [
        id|faseTipo|inicio|fim|tipoItem|grupo
        1|Forecast|01/08/2018|30/10/2018||GrupoA
        2|Plan|15/11/2018|15/12/2018||GrupoB
        3|Plan|01/08/2018|25/10/2018||GrupoA
        4|Plan|05/09/2018|||GrupoC
        5|Forecast|15/08/2018|15/12/2018||GrupoB
        6|Actual|01/08/2018|23/10/2018||GrupoA
    ](delimiter is '|');
```

[![](https://github.com/dersonluis/TimelineAlcs/blob/master/dados.png)](https://github.com/dersonluis/TimelineAlcs/blob/master/dados.png)



***
## License
Released under the [The MIT License](https://opensource.org/licenses/MIT)
