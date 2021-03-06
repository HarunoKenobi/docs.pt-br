---
title: Visão geral do controle DataGridView (Windows Forms)
ms.date: 03/30/2017
f1_keywords:
- DataGridView
helpviewer_keywords:
- DataGridView control [Windows Forms], about DataGridView control
- grid controls [Windows Forms]
- tables [Windows Forms], displaying in DataGridView control
- tables [Windows Forms], binding to DataGridView control
- columns [Windows Forms], DataGridView control
- bound controls [Windows Forms], dataGridView control
- datasets [Windows Forms], binding to DataGridView control
- data grids [Windows Forms], about data grids
- data [Windows Forms], resorting
- data [Windows Forms], navigating
- grids [Windows Forms]
- data binding [Windows Forms], DataGridView control
- data sources [Windows Forms], binding to DataGridView control
- DataGridView control [Windows Forms], data binding
ms.assetid: 0a45c661-89dc-4390-9cc6-c47eee501488
ms.openlocfilehash: 4db2a8b0e30a6bb3db0c5c629d868bc01dc15a8c
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64648076"
---
# <a name="datagridview-control-overview-windows-forms"></a>Visão geral do controle DataGridView (Windows Forms)
> [!NOTE]
>  O controle <xref:System.Windows.Forms.DataGridView> substitui e adiciona funcionalidade ao controle <xref:System.Windows.Forms.DataGrid>, no entanto, o controle <xref:System.Windows.Forms.DataGrid> é mantido para compatibilidade com versões anteriores e para uso futuro, se desejado. Para obter mais informações, consulte [Diferenças Entre o Windows Forms DataGridView e os Controles do DataGrid](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Com o <xref:System.Windows.Forms.DataGridView> controle, você pode exibir e editar dados tabulares de muitos tipos diferentes de fontes de dados.  
  
 Associação de dados para o <xref:System.Windows.Forms.DataGridView> controle é simples e intuitiva e, em muitos casos é tão simple quanto a configuração de <xref:System.Windows.Forms.DataGridView.DataSource%2A> propriedade. Quando você associa a uma fonte de dados que contém várias listas ou tabelas, defina o <xref:System.Windows.Forms.DataGridView.DataMember%2A> propriedade como uma cadeia de caracteres que especifica a lista ou tabela a ser associada.  
  
 O <xref:System.Windows.Forms.DataGridView> controle é compatível com o modelo de associação de dados do Windows Forms padrão, portanto, ele associará a instâncias das classes descritas na lista a seguir:  
  
- Qualquer classe que implementa o <xref:System.Collections.IList> interface, inclusive matrizes unidimensionais.  
  
- Qualquer classe que implementa o <xref:System.ComponentModel.IListSource> interface, como o <xref:System.Data.DataTable> e <xref:System.Data.DataSet> classes.  
  
- Qualquer classe que implementa o <xref:System.ComponentModel.IBindingList> interface, como o <xref:System.ComponentModel.BindingList%601> classe.  
  
- Qualquer classe que implementa o <xref:System.ComponentModel.IBindingListView> interface, como o <xref:System.Windows.Forms.BindingSource> classe.  
  
 O <xref:System.Windows.Forms.DataGridView> controle dá suporte à vinculação de dados para as propriedades públicas dos objetos retornados por essas interfaces ou à coleção de propriedades retornado por um <xref:System.ComponentModel.ICustomTypeDescriptor> de interface, se implementada nos objetos retornados.  
  
 Normalmente, você associará a um <xref:System.Windows.Forms.BindingSource> componente e associar o <xref:System.Windows.Forms.BindingSource> componente para outra fonte de dados ou preenchê-lo com objetos comerciais. O <xref:System.Windows.Forms.BindingSource> componente é a fonte de dados preferencial, pois pode associar a uma ampla variedade de fontes de dados e pode resolver muitos problemas de associação de dados automaticamente. Para obter mais informações, consulte [Componente BindingSource](bindingsource-component.md).  
  
 O <xref:System.Windows.Forms.DataGridView> controle também pode ser usado no *desassociado* modo, com nenhum armazenamento de dados subjacente. Para obter um exemplo de código que usa um desassociado <xref:System.Windows.Forms.DataGridView> de controle, consulte [passo a passo: Criar um Windows não associado o controle DataGridView Forms](walkthrough-creating-an-unbound-windows-forms-datagridview-control.md).  
  
 O <xref:System.Windows.Forms.DataGridView> controle é altamente configurável e extensível e fornece muitas propriedades, métodos e eventos para personalizar sua aparência e comportamento. Quando você quiser que seu aplicativo do Windows Forms para exibir dados tabulares, considere usar o <xref:System.Windows.Forms.DataGridView> controle antes de outros (por exemplo, <xref:System.Windows.Forms.DataGrid>). Se você estiver exibindo uma pequena grade com valores somente leitura, ou se você estiver habilitando um usuário editar uma tabela com milhões de registros, o <xref:System.Windows.Forms.DataGridView> controle fornecerá uma solução eficiente da memória prontamente programável.  
  
## <a name="in-this-section"></a>Nesta seção  
 [Resumo de tecnologia do controle DataGridView](datagridview-control-technology-summary-windows-forms.md)  
 Resume <xref:System.Windows.Forms.DataGridView> controlar conceitos e o uso de classes relacionadas.  
  
 [Arquitetura de controle DataGridView](datagridview-control-architecture-windows-forms.md)  
 Descreve a arquitetura do <xref:System.Windows.Forms.DataGridView> controle, explicando sua estrutura de herança e hierarquia de tipo.  
  
 [Cenários do controle DataGridView](datagridview-control-scenarios-windows-forms.md)  
 Descreve os cenários mais comuns nos quais <xref:System.Windows.Forms.DataGridView> controles são usados.  
  
 [Diretório de código do controle DataGridView](datagridview-control-code-directory-windows-forms.md)  
 Fornece links para exemplos de código na documentação para vários <xref:System.Windows.Forms.DataGridView> tarefas. Esses exemplos são categorizados por tipo de tarefa.  
  
## <a name="related-sections"></a>Seções relacionadas  
 [Tipos de coluna no controle DataGridView dos Windows Forms](column-types-in-the-windows-forms-datagridview-control.md)  
 Discute os tipos de coluna nos formulários de Windows <xref:System.Windows.Forms.DataGridView> controle usado para exibir informações e permitir que os usuários modifiquem ou adicionem informações.  
  
 [Exibindo dados no controle DataGridView do Windows Forms](displaying-data-in-the-windows-forms-datagridview-control.md)  
 Fornece tópicos que descrevem como preencher o controle com os dados manualmente ou de uma fonte de dados externa.  
  
 [Personalizando o controle DataGridView dos Windows Forms](customizing-the-windows-forms-datagridview-control.md)  
 Fornece tópicos que descrevem a pintura personalizada de células e linhas <xref:System.Windows.Forms.DataGridView>, bem como a criação de tipos de célula, coluna e linha derivados.  
  
 [Ajuste de desempenho no controle DataGridView do Windows Forms](performance-tuning-in-the-windows-forms-datagridview-control.md)  
 Fornece tópicos que descrevem como usar o controle com eficiência para evitar problemas de desempenho ao trabalhar com grandes volumes de dados.  
  
## <a name="see-also"></a>Consulte também

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [Controle DataGridView](datagridview-control-windows-forms.md)
- [Funcionalidade padrão no controle DataGridView dos Windows Forms](default-functionality-in-the-windows-forms-datagridview-control.md)
- [Tratamento de teclado e mouse padrão no controle DataGridView do Windows Forms](default-keyboard-and-mouse-handling-in-the-windows-forms-datagridview-control.md)
