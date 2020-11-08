---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073631"
---
# <span data-ttu-id="e7aac-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e7aac-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="e7aac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7aac-102">SYNOPSIS</span></span>
<span data-ttu-id="e7aac-103">Создает новый объект CosmosDB SqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7aac-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e7aac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7aac-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7aac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7aac-105">DESCRIPTION</span></span>
<span data-ttu-id="e7aac-106">Командлет **New-AzCosmosDBSqlUniqueKeyPolicy** создает новый объект типа PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="e7aac-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e7aac-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7aac-107">EXAMPLES</span></span>

### <span data-ttu-id="e7aac-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e7aac-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="e7aac-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7aac-109">PARAMETERS</span></span>

### <span data-ttu-id="e7aac-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7aac-110">-DefaultProfile</span></span>
<span data-ttu-id="e7aac-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7aac-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aac-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="e7aac-112">-UniqueKey</span></span>
<span data-ttu-id="e7aac-113">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7aac-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7aac-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7aac-114">CommonParameters</span></span>
<span data-ttu-id="e7aac-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7aac-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7aac-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7aac-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7aac-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7aac-117">INPUTS</span></span>

### <span data-ttu-id="e7aac-118">Ничего</span><span class="sxs-lookup"><span data-stu-id="e7aac-118">None</span></span>

## <span data-ttu-id="e7aac-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7aac-119">OUTPUTS</span></span>

### <span data-ttu-id="e7aac-120">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e7aac-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="e7aac-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7aac-121">NOTES</span></span>

## <span data-ttu-id="e7aac-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7aac-122">RELATED LINKS</span></span>
