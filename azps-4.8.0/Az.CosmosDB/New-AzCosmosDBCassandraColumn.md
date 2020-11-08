---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079754"
---
# <span data-ttu-id="90d38-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="90d38-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="90d38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90d38-102">SYNOPSIS</span></span>
<span data-ttu-id="90d38-103">Создание нового столбца CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="90d38-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="90d38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90d38-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90d38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90d38-105">DESCRIPTION</span></span>
<span data-ttu-id="90d38-106">**New-AzCosmosDBCassandraColumn** создает новый столбец CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="90d38-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="90d38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90d38-107">EXAMPLES</span></span>

### <span data-ttu-id="90d38-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90d38-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="90d38-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90d38-109">PARAMETERS</span></span>

### <span data-ttu-id="90d38-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90d38-110">-DefaultProfile</span></span>
<span data-ttu-id="90d38-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90d38-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90d38-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90d38-112">-Name</span></span>
<span data-ttu-id="90d38-113">Имя столбца Cassandra.</span><span class="sxs-lookup"><span data-stu-id="90d38-113">Name of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d38-114">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="90d38-114">-Type</span></span>
<span data-ttu-id="90d38-115">Тип столбца Cassandra.</span><span class="sxs-lookup"><span data-stu-id="90d38-115">Type of Cassandra Column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90d38-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d38-116">CommonParameters</span></span>
<span data-ttu-id="90d38-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90d38-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d38-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90d38-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d38-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90d38-119">INPUTS</span></span>

### <span data-ttu-id="90d38-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="90d38-120">None</span></span>

## <span data-ttu-id="90d38-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90d38-121">OUTPUTS</span></span>

### <span data-ttu-id="90d38-122">Microsoft. Azure. Commands. CosmosDB. Models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="90d38-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="90d38-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="90d38-123">NOTES</span></span>

## <span data-ttu-id="90d38-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90d38-124">RELATED LINKS</span></span>
