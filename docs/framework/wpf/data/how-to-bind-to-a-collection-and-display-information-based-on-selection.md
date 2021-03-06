---
title: 'Como: Associar a uma coleção e exibir informações com base na seleção'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data collections [WPF], selecting data for views
- data binding [WPF], creating views of data collections
- data binding [WPF], selecting data for views
- data binding [WPF], binding to collections
ms.assetid: 952a7d76-dd29-49e5-86f5-32c4530e70eb
ms.openlocfilehash: bb7d4c89e63982a3052857dcb50d04d36d9517dd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61967929"
---
# <a name="how-to-bind-to-a-collection-and-display-information-based-on-selection"></a>Como: Associar a uma coleção e exibir informações com base na seleção
Em um cenário mestre / detalhes simples, você tem uma associação de dados <xref:System.Windows.Controls.ItemsControl> como um <xref:System.Windows.Controls.ListBox>. Com base na seleção do usuário, se exibe mais informações sobre o item selecionado. Este exemplo mostra como implementar este cenário.  
  
## <a name="example"></a>Exemplo  
 Neste exemplo, `People` é um <xref:System.Collections.ObjectModel.ObservableCollection%601> de `Person` classes. Esta classe `Person` contém três propriedades: `FirstName`, `LastName` e `HomeTown`, todas de tipo `string`.  
  
 [!code-xaml[CollectionBinding#Source](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#source)]  
[!code-xaml[CollectionBinding#UI](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#ui)]  
  
 O <xref:System.Windows.Controls.ContentControl> usa os seguintes <xref:System.Windows.DataTemplate> que define como as informações de um `Person` é apresentado:  
  
 [!code-xaml[CollectionBinding#DetailTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Window1.xaml#detailtemplate)]  
  
 A seguir temos uma imagem do que o exemplo produz. O <xref:System.Windows.Controls.ContentControl> mostra as outras propriedades da pessoa selecionada.  
  
 ![Associando a uma coleção](./media/databinding-collectionbindingsample.png "DataBinding_CollectionBindingSample")  
  
 As duas coisas a se observar neste exemplo são:  
  
1. O <xref:System.Windows.Controls.ListBox> e o <xref:System.Windows.Controls.ContentControl> associar à mesma fonte. O <xref:System.Windows.Data.Binding.Path%2A> propriedades de ambas as associações não são especificadas porque ambos os controles estão associados ao objeto da coleção inteira.  
  
2. Você deve definir a <xref:System.Windows.Controls.Primitives.Selector.IsSynchronizedWithCurrentItem%2A> propriedade para `true` para este trabalho. A definição dessa propriedade garante que o item selecionado é sempre definido como o <xref:System.Windows.Controls.ItemCollection.CurrentItem%2A>. Como alternativa, se o <xref:System.Windows.Controls.ListBox> obtém seus dados de um <xref:System.Windows.Data.CollectionViewSource>, ele sincroniza a seleção e moeda automaticamente.  
  
 Observe que a classe `Person` substitui o método `ToString` da seguinte forma. Por padrão, o <xref:System.Windows.Controls.ListBox> chamadas `ToString` e exibe uma representação de cadeia de caracteres de cada objeto na coleção associada. É por isso que cada `Person` aparece como um primeiro nome no <xref:System.Windows.Controls.ListBox>.  
  
 [!code-csharp[CollectionBinding#ToString](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionBinding/CSharp/Data.cs#tostring)]
 [!code-vb[CollectionBinding#ToString](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionBinding/VisualBasic/Person.vb#tostring)]  
  
## <a name="see-also"></a>Consulte também

- [Usar o padrão de detalhes mestre com os dados hierárquicos](how-to-use-the-master-detail-pattern-with-hierarchical-data.md)
- [Usar o padrão de detalhes mestre com os dados XML hierárquicos](how-to-use-the-master-detail-pattern-with-hierarchical-xml-data.md)
- [Visão geral da vinculação de dados](data-binding-overview.md)
- [Visão geral de modelagem dos dados](data-templating-overview.md)
- [Tópicos de instruções](data-binding-how-to-topics.md)
