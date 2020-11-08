---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079752"
---
# <span data-ttu-id="85aae-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="85aae-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="85aae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85aae-102">SYNOPSIS</span></span>
<span data-ttu-id="85aae-103">Создание новой схемы CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="85aae-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="85aae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85aae-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85aae-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85aae-105">DESCRIPTION</span></span>
<span data-ttu-id="85aae-106">**New-AzCosmosDBCassandraSchema** создает новую схему CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="85aae-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="85aae-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85aae-107">EXAMPLES</span></span>

### <span data-ttu-id="85aae-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85aae-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="85aae-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85aae-109">PARAMETERS</span></span>

### <span data-ttu-id="85aae-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="85aae-110">-ClusterKey</span></span>
<span data-ttu-id="85aae-111">Массив объектов PSClusterKey.</span><span class="sxs-lookup"><span data-stu-id="85aae-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="85aae-112">-Столбец</span><span class="sxs-lookup"><span data-stu-id="85aae-112">-Column</span></span>
<span data-ttu-id="85aae-113">Объект PSColumn.</span><span class="sxs-lookup"><span data-stu-id="85aae-113">PSColumn object.</span></span>

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

### <span data-ttu-id="85aae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85aae-114">-DefaultProfile</span></span>
<span data-ttu-id="85aae-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85aae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85aae-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="85aae-116">-PartitionKey</span></span>
<span data-ttu-id="85aae-117">Массив строк, содержащий ключи секционирования.</span><span class="sxs-lookup"><span data-stu-id="85aae-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="85aae-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85aae-118">CommonParameters</span></span>
<span data-ttu-id="85aae-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85aae-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85aae-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85aae-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85aae-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85aae-121">INPUTS</span></span>

### <span data-ttu-id="85aae-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="85aae-122">None</span></span>

## <span data-ttu-id="85aae-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85aae-123">OUTPUTS</span></span>

### <span data-ttu-id="85aae-124">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="85aae-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="85aae-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="85aae-125">NOTES</span></span>

## <span data-ttu-id="85aae-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85aae-126">RELATED LINKS</span></span>
