---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 009048c5f37936d469fe88c5e75cab8270efa81c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314912"
---
# <span data-ttu-id="4c90e-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="4c90e-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="4c90e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c90e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c90e-103">Используйте этот параметр для переноса пропускной способности автомасштабирования на пропускную способность вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="4c90e-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="4c90e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c90e-104">SYNTAX</span></span>

### <span data-ttu-id="4c90e-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c90e-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c90e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c90e-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c90e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c90e-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c90e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c90e-108">DESCRIPTION</span></span>
<span data-ttu-id="4c90e-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="4c90e-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="4c90e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c90e-110">EXAMPLES</span></span>

### <span data-ttu-id="4c90e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4c90e-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```


## <span data-ttu-id="4c90e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c90e-112">PARAMETERS</span></span>

### <span data-ttu-id="4c90e-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4c90e-113">-AccountName</span></span>
<span data-ttu-id="4c90e-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4c90e-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4c90e-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c90e-115">-Confirm</span></span>
<span data-ttu-id="4c90e-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c90e-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c90e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c90e-117">-DefaultProfile</span></span>
<span data-ttu-id="4c90e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c90e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c90e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c90e-119">-InputObject</span></span>
<span data-ttu-id="4c90e-120">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="4c90e-120">Table Object.</span></span>

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

### <span data-ttu-id="4c90e-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c90e-121">-Name</span></span>
<span data-ttu-id="4c90e-122">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="4c90e-122">Name of the Table.</span></span>

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

### <span data-ttu-id="4c90e-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4c90e-123">-ParentObject</span></span>
<span data-ttu-id="4c90e-124">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="4c90e-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="4c90e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c90e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c90e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c90e-126">Name of resource group.</span></span>

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

### <span data-ttu-id="4c90e-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="4c90e-127">-ThroughputType</span></span>
<span data-ttu-id="4c90e-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="4c90e-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="4c90e-129">Возможные значения: Автомасштабирование, вручную.</span><span class="sxs-lookup"><span data-stu-id="4c90e-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="4c90e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c90e-130">-WhatIf</span></span>
<span data-ttu-id="4c90e-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c90e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c90e-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c90e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c90e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c90e-133">CommonParameters</span></span>
<span data-ttu-id="4c90e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c90e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c90e-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c90e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c90e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c90e-136">INPUTS</span></span>

### <span data-ttu-id="4c90e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="4c90e-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="4c90e-138">Microsoft. Azure. Commands. CosmosDB. Models. PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="4c90e-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="4c90e-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c90e-139">OUTPUTS</span></span>

### <span data-ttu-id="4c90e-140">Microsoft. Azure. Commands. CosmosDB. Models. PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="4c90e-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="4c90e-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c90e-141">NOTES</span></span>

## <span data-ttu-id="4c90e-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c90e-142">RELATED LINKS</span></span>
