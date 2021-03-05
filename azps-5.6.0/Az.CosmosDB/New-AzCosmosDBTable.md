---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBTable.md
ms.openlocfilehash: d2a4dacb929587fb0f06c002ad26df3144f32f56
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960792"
---
# <span data-ttu-id="4d48a-101">New-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="4d48a-101">New-AzCosmosDBTable</span></span>

## <span data-ttu-id="4d48a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d48a-102">SYNOPSIS</span></span>
<span data-ttu-id="4d48a-103">Создает таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="4d48a-103">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="4d48a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4d48a-104">SYNTAX</span></span>

### <span data-ttu-id="4d48a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4d48a-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> -Name <String> [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d48a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d48a-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBTable -Name <String> [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d48a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4d48a-107">DESCRIPTION</span></span>
<span data-ttu-id="4d48a-108">Создает таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="4d48a-108">Creates a new CosmosDB Table.</span></span>

## <span data-ttu-id="4d48a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4d48a-109">EXAMPLES</span></span>

### <span data-ttu-id="4d48a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4d48a-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="4d48a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d48a-111">PARAMETERS</span></span>

### <span data-ttu-id="4d48a-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4d48a-112">-AccountName</span></span>
<span data-ttu-id="4d48a-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="4d48a-113">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-114">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="4d48a-114">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="4d48a-115">Максимальное значение пропускной способности, если включена автоматическая шкала.</span><span class="sxs-lookup"><span data-stu-id="4d48a-115">Maximum Throughput value if autoscale is enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d48a-116">-Confirm</span></span>
<span data-ttu-id="4d48a-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4d48a-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d48a-118">-DefaultProfile</span></span>
<span data-ttu-id="4d48a-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4d48a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d48a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4d48a-120">-Name</span></span>
<span data-ttu-id="4d48a-121">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="4d48a-121">Name of the Table.</span></span>

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

### <span data-ttu-id="4d48a-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4d48a-122">-ParentObject</span></span>
<span data-ttu-id="4d48a-123">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="4d48a-123">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d48a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d48a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d48a-125">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-126">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="4d48a-126">-Throughput</span></span>
<span data-ttu-id="4d48a-127">Пропускная способность таблицы (RU/s).</span><span class="sxs-lookup"><span data-stu-id="4d48a-127">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="4d48a-128">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="4d48a-128">Default value is 400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d48a-129">-WhatIf</span></span>
<span data-ttu-id="4d48a-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d48a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d48a-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4d48a-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d48a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d48a-132">CommonParameters</span></span>
<span data-ttu-id="4d48a-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d48a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d48a-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d48a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d48a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4d48a-135">INPUTS</span></span>

### <span data-ttu-id="4d48a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="4d48a-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="4d48a-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4d48a-137">OUTPUTS</span></span>

### <span data-ttu-id="4d48a-138">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4d48a-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="4d48a-139">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="4d48a-139">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="4d48a-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4d48a-140">NOTES</span></span>

## <span data-ttu-id="4d48a-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4d48a-141">RELATED LINKS</span></span>
