---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314888"
---
# <span data-ttu-id="daebb-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="daebb-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="daebb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="daebb-102">SYNOPSIS</span></span>
<span data-ttu-id="daebb-103">Создание нового столбца CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="daebb-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="daebb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="daebb-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="daebb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="daebb-105">DESCRIPTION</span></span>
<span data-ttu-id="daebb-106">**New-AzCosmosDBCassandraColumn** создает новый столбец CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="daebb-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="daebb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="daebb-107">EXAMPLES</span></span>

### <span data-ttu-id="daebb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="daebb-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="daebb-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="daebb-109">PARAMETERS</span></span>

### <span data-ttu-id="daebb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daebb-110">-DefaultProfile</span></span>
<span data-ttu-id="daebb-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="daebb-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="daebb-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="daebb-112">-Name</span></span>
<span data-ttu-id="daebb-113">Имя столбца Cassandra.</span><span class="sxs-lookup"><span data-stu-id="daebb-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="daebb-114">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="daebb-114">-Type</span></span>
<span data-ttu-id="daebb-115">Тип столбца Cassandra.</span><span class="sxs-lookup"><span data-stu-id="daebb-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="daebb-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daebb-116">CommonParameters</span></span>
<span data-ttu-id="daebb-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="daebb-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daebb-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="daebb-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daebb-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="daebb-119">INPUTS</span></span>

### <span data-ttu-id="daebb-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="daebb-120">None</span></span>

## <span data-ttu-id="daebb-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="daebb-121">OUTPUTS</span></span>

### <span data-ttu-id="daebb-122">Microsoft. Azure. Commands. CosmosDB. Models. PSColumn</span><span class="sxs-lookup"><span data-stu-id="daebb-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="daebb-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="daebb-123">NOTES</span></span>

## <span data-ttu-id="daebb-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="daebb-124">RELATED LINKS</span></span>
