---
title: 'Como: declarar tabelas como classes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
ms.assetid: 84dda12b-88a2-4cd2-92b3-8db87b28d14c
ms.openlocfilehash: ff943fbc7ae137128d6c635fd2366ad14cf70d15
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64620027"
---
# <a name="how-to-represent-tables-as-classes"></a>Como: declarar tabelas como classes
Use o [!INCLUDE[vbtecdlinq](../../../../../../includes/vbtecdlinq-md.md)] <xref:System.Data.Linq.Mapping.TableAttribute> atributo para designar uma classe como uma classe de entidade associada a uma tabela de banco de dados.  
  
### <a name="to-map-a-class-to-a-database-table"></a>Para mapear uma classe a uma tabela de base de dados  
  
- Adicione o atributo de <xref:System.Data.Linq.Mapping.TableAttribute> à declaração de classe.  
  
## <a name="example"></a>Exemplo  
 O código a seguir estabelece a classe de `Customer` como uma classe de entidade que está associada com a tabela de base de dados de `Customers` .  
  
 [!code-csharp[DLinqCustomize#1](../../../../../../samples/snippets/csharp/VS_Snippets_Data/DLinqCustomize/cs/Program.cs#1)]
 [!code-vb[DLinqCustomize#1](../../../../../../samples/snippets/visualbasic/VS_Snippets_Data/DLinqCustomize/vb/Module1.vb#1)]  
  
 Você não precisa especificar a propriedade de <xref:System.Data.Linq.Mapping.TableAttribute.Name%2A> se o nome pode ser inferido. Se você não especificar um nome, o nome é presumido ser o mesmo nome que a propriedade ou do campo.  
  
## <a name="see-also"></a>Consulte também

- [O modelo de objeto LINQ to SQL](../../../../../../docs/framework/data/adonet/sql/linq/the-linq-to-sql-object-model.md)
- [Como: Personalizar Classes de entidade usando o Editor de código](../../../../../../docs/framework/data/adonet/sql/linq/how-to-customize-entity-classes-by-using-the-code-editor.md)
