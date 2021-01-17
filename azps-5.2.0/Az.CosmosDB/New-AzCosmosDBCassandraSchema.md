---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415612"
---
# <span data-ttu-id="00a81-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="00a81-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="00a81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00a81-102">SYNOPSIS</span></span>
<span data-ttu-id="00a81-103">Создает новую схему Сергея Ильиной.</span><span class="sxs-lookup"><span data-stu-id="00a81-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="00a81-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="00a81-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00a81-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00a81-105">DESCRIPTION</span></span>
<span data-ttu-id="00a81-106">Новая **схема AzCosmosDBCassandraSchema** создает новую схему "Шашков".</span><span class="sxs-lookup"><span data-stu-id="00a81-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="00a81-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="00a81-107">EXAMPLES</span></span>

### <span data-ttu-id="00a81-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00a81-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="00a81-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00a81-109">PARAMETERS</span></span>

### <span data-ttu-id="00a81-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="00a81-110">-ClusterKey</span></span>
<span data-ttu-id="00a81-111">Массив объектов PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="00a81-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a81-112">-Column</span><span class="sxs-lookup"><span data-stu-id="00a81-112">-Column</span></span>
<span data-ttu-id="00a81-113">Объект PSColumn.</span><span class="sxs-lookup"><span data-stu-id="00a81-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00a81-114">-DefaultProfile</span></span>
<span data-ttu-id="00a81-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00a81-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00a81-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="00a81-116">-PartitionKey</span></span>
<span data-ttu-id="00a81-117">Массив строк, содержащих ключи разделов.</span><span class="sxs-lookup"><span data-stu-id="00a81-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00a81-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00a81-118">CommonParameters</span></span>
<span data-ttu-id="00a81-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00a81-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00a81-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00a81-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00a81-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="00a81-121">INPUTS</span></span>

### <span data-ttu-id="00a81-122">Нет</span><span class="sxs-lookup"><span data-stu-id="00a81-122">None</span></span>

## <span data-ttu-id="00a81-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="00a81-123">OUTPUTS</span></span>

### <span data-ttu-id="00a81-124">Microsoft.Azure.Commands.АsDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="00a81-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="00a81-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="00a81-125">NOTES</span></span>

## <span data-ttu-id="00a81-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00a81-126">RELATED LINKS</span></span>
