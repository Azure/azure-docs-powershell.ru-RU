---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/invoke-azcosmosdbtablethroughputmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Invoke-AzCosmosDBTableThroughputMigration.md
ms.openlocfilehash: 2511ddc7174d4b76ec6d5df5bcbcd334f423a882
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996848"
---
# <span data-ttu-id="782e9-101">Invoke-AzCosmosDBTableThroughputMigration</span><span class="sxs-lookup"><span data-stu-id="782e9-101">Invoke-AzCosmosDBTableThroughputMigration</span></span>

## <span data-ttu-id="782e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782e9-102">SYNOPSIS</span></span>
<span data-ttu-id="782e9-103">Используйте этот метод для переноса пропускной способности для автоматической передачи по шкале, которая передается вручную и наоборот.</span><span class="sxs-lookup"><span data-stu-id="782e9-103">Use this to migrate autoscale throughput to manual throughput and vice versa.</span></span>

## <span data-ttu-id="782e9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="782e9-104">SYNTAX</span></span>

### <span data-ttu-id="782e9-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="782e9-105">ByNameParameterSet (Default)</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ResourceGroupName <String> -AccountName <String>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="782e9-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="782e9-106">ByParentObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -ParentObject <PSDatabaseAccountGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="782e9-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="782e9-107">ByObjectParameterSet</span></span>
```
Invoke-AzCosmosDBTableThroughputMigration [-Name <String>] -InputObject <PSTableGetResults>
 -ThroughputType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="782e9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="782e9-108">DESCRIPTION</span></span>
<span data-ttu-id="782e9-109">Параметр ThroughpyteType определяет пропускную способность, на которую вы хотите перейти.</span><span class="sxs-lookup"><span data-stu-id="782e9-109">ThroughpyteType paramter defines the throughput to which you want to migrate to.</span></span>

## <span data-ttu-id="782e9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="782e9-110">EXAMPLES</span></span>

### <span data-ttu-id="782e9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="782e9-111">Example 1</span></span>
```powershell
PS C:\>
      $NewTable =  New-AzCosmosDBTable -AccountName myAccountName -ResourceGroupName myRgName -Name myTableName -Throughput  700
      $AutoscaleThroughput = Invoke-AzCosmosDBTableThroughputMigration -InputObject $NewTable -ThroughputType Autoscale
```

## <span data-ttu-id="782e9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="782e9-112">PARAMETERS</span></span>

### <span data-ttu-id="782e9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="782e9-113">-AccountName</span></span>
<span data-ttu-id="782e9-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="782e9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="782e9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="782e9-115">-Confirm</span></span>
<span data-ttu-id="782e9-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="782e9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="782e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782e9-117">-DefaultProfile</span></span>
<span data-ttu-id="782e9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="782e9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="782e9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="782e9-119">-InputObject</span></span>
<span data-ttu-id="782e9-120">Объект Table.</span><span class="sxs-lookup"><span data-stu-id="782e9-120">Table Object.</span></span>

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

### <span data-ttu-id="782e9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="782e9-121">-Name</span></span>
<span data-ttu-id="782e9-122">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="782e9-122">Name of the Table.</span></span>

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

### <span data-ttu-id="782e9-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="782e9-123">-ParentObject</span></span>
<span data-ttu-id="782e9-124">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="782e9-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="782e9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="782e9-125">-ResourceGroupName</span></span>
<span data-ttu-id="782e9-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="782e9-126">Name of resource group.</span></span>

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

### <span data-ttu-id="782e9-127">-ThroughputType</span><span class="sxs-lookup"><span data-stu-id="782e9-127">-ThroughputType</span></span>
<span data-ttu-id="782e9-128">Тип пропускной способности для миграции.</span><span class="sxs-lookup"><span data-stu-id="782e9-128">Throughput type to migrate to.</span></span>
<span data-ttu-id="782e9-129">Возможные значения: "Автомасштаб", "Вручную".</span><span class="sxs-lookup"><span data-stu-id="782e9-129">Possible values are: Autoscale, Manual.</span></span>

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

### <span data-ttu-id="782e9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="782e9-130">-WhatIf</span></span>
<span data-ttu-id="782e9-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="782e9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="782e9-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="782e9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="782e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782e9-133">CommonParameters</span></span>
<span data-ttu-id="782e9-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782e9-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="782e9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782e9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="782e9-136">INPUTS</span></span>

### <span data-ttu-id="782e9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span><span class="sxs-lookup"><span data-stu-id="782e9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountGetResults</span></span>

### <span data-ttu-id="782e9-138">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="782e9-138">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="782e9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="782e9-139">OUTPUTS</span></span>

### <span data-ttu-id="782e9-140">Microsoft.Azure.Commands.OughsDB.Models.PSThroughputSettingsGetResults</span><span class="sxs-lookup"><span data-stu-id="782e9-140">Microsoft.Azure.Commands.CosmosDB.Models.PSThroughputSettingsGetResults</span></span>

## <span data-ttu-id="782e9-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="782e9-141">NOTES</span></span>

## <span data-ttu-id="782e9-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="782e9-142">RELATED LINKS</span></span>
