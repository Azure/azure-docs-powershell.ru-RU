---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBTable.md
ms.openlocfilehash: efc177e5255f4325fc2ecbfe88e94bb32708c45a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236830"
---
# <span data-ttu-id="fcf10-101">Update-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="fcf10-101">Update-AzCosmosDBTable</span></span>

## <span data-ttu-id="fcf10-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcf10-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf10-103">Обновляет таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="fcf10-103">Updates the CosmosDB Table.</span></span> <span data-ttu-id="fcf10-104">Выполняет операцию исправления на стороне клиента, считывая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="fcf10-104">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="fcf10-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcf10-105">SYNTAX</span></span>

### <span data-ttu-id="fcf10-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcf10-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBTable -ResourceGroupName <String> -AccountName <String> [-Name <String>] [-Throughput <Int32>]
 [-AutoscaleMaxThroughput <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcf10-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcf10-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -ParentObject <PSDatabaseAccountGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcf10-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcf10-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBTable [-Name <String>] [-Throughput <Int32>] [-AutoscaleMaxThroughput <Int32>]
 -InputObject <PSTableGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcf10-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf10-109">DESCRIPTION</span></span>
<span data-ttu-id="fcf10-110">Обновляет таблицу CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="fcf10-110">Updates the CosmosDB Table.</span></span> <span data-ttu-id="fcf10-111">Выполняет операцию исправления на стороне клиента, считывая существующую таблицу.</span><span class="sxs-lookup"><span data-stu-id="fcf10-111">Performs a client side patch operation by reading the existing Table.</span></span>

## <span data-ttu-id="fcf10-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcf10-112">EXAMPLES</span></span>

### <span data-ttu-id="fcf10-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fcf10-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBTable -AccountName myAcccountName -Name myTableName -ResourceGroupName myRgName Throughput 800

Name     : myTableName
Id       : /subscriptions/mySubscriptionId/resourceGroups/myResourcegroupName/providers/Microsoft.DocumentDB/databaseAccounts/myAccountName/Tables/myTableName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetPropertiesResource
```

## <span data-ttu-id="fcf10-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcf10-114">PARAMETERS</span></span>

### <span data-ttu-id="fcf10-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="fcf10-115">-AccountName</span></span>
<span data-ttu-id="fcf10-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="fcf10-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fcf10-117">-AutoscaleMaxThroughput</span><span class="sxs-lookup"><span data-stu-id="fcf10-117">-AutoscaleMaxThroughput</span></span>
<span data-ttu-id="fcf10-118">Максимальное значение пропускной способности, если включено Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="fcf10-118">Maximum Throughput value if autoscale is enabled.</span></span>

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

### <span data-ttu-id="fcf10-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcf10-119">-Confirm</span></span>
<span data-ttu-id="fcf10-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fcf10-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf10-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf10-121">-DefaultProfile</span></span>
<span data-ttu-id="fcf10-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf10-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf10-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcf10-123">-InputObject</span></span>
<span data-ttu-id="fcf10-124">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="fcf10-124">Table Object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fcf10-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fcf10-125">-Name</span></span>
<span data-ttu-id="fcf10-126">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="fcf10-126">Name of the Table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcf10-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fcf10-127">-ParentObject</span></span>
<span data-ttu-id="fcf10-128">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="fcf10-128">CosmosDB Account object</span></span>

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

### <span data-ttu-id="fcf10-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf10-129">-ResourceGroupName</span></span>
<span data-ttu-id="fcf10-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fcf10-130">Name of resource group.</span></span>

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

### <span data-ttu-id="fcf10-131">-Пропускная способность</span><span class="sxs-lookup"><span data-stu-id="fcf10-131">-Throughput</span></span>
<span data-ttu-id="fcf10-132">Пропускная способность таблицы (RU/с).</span><span class="sxs-lookup"><span data-stu-id="fcf10-132">The throughput of Table (RU/s).</span></span>
<span data-ttu-id="fcf10-133">Значение по умолчанию — 400.</span><span class="sxs-lookup"><span data-stu-id="fcf10-133">Default value is 400.</span></span>

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

### <span data-ttu-id="fcf10-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf10-134">-WhatIf</span></span>
<span data-ttu-id="fcf10-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fcf10-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf10-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fcf10-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf10-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf10-137">CommonParameters</span></span>
<span data-ttu-id="fcf10-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcf10-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf10-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcf10-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf10-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcf10-140">INPUTS</span></span>

### <span data-ttu-id="fcf10-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="fcf10-141">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

### <span data-ttu-id="fcf10-142">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fcf10-142">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="fcf10-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf10-143">OUTPUTS</span></span>

### <span data-ttu-id="fcf10-144">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fcf10-144">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

### <span data-ttu-id="fcf10-145">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="fcf10-145">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="fcf10-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcf10-146">NOTES</span></span>

## <span data-ttu-id="fcf10-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcf10-147">RELATED LINKS</span></span>
