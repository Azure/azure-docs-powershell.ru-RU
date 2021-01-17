---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400900"
---
# <span data-ttu-id="aa471-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="aa471-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="aa471-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa471-102">SYNOPSIS</span></span>
<span data-ttu-id="aa471-103">Обновление областей учетной записи ВайссDB.</span><span class="sxs-lookup"><span data-stu-id="aa471-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="aa471-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa471-104">SYNTAX</span></span>

### <span data-ttu-id="aa471-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aa471-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa471-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa471-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa471-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa471-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa471-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa471-108">DESCRIPTION</span></span>
<span data-ttu-id="aa471-109">Обновление областей учетной записи ВайссDB.</span><span class="sxs-lookup"><span data-stu-id="aa471-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="aa471-110">Расположение можно указать как объект psLocation типа или как строки с именем расположения, упорядоченным по приоритету отбойного действия.</span><span class="sxs-lookup"><span data-stu-id="aa471-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="aa471-111">Параметр LocationObject ожидает список текущих расположений (включаемого приоритетов отладки) с новыми расположениями LocationObjects, которые будут добавлены в новые расположения.</span><span class="sxs-lookup"><span data-stu-id="aa471-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="aa471-112">Параметр расположения ожидает список текущего расположения (упорядоченного по приоритету отсказки) и новых расположений.</span><span class="sxs-lookup"><span data-stu-id="aa471-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="aa471-113">Обратите внимание, что мы поддерживаем только добавление регионов.</span><span class="sxs-lookup"><span data-stu-id="aa471-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="aa471-114">Укайте расположение или LocationObject.</span><span class="sxs-lookup"><span data-stu-id="aa471-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="aa471-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa471-115">EXAMPLES</span></span>

### <span data-ttu-id="aa471-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa471-116">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountRegion -ResourceGroupName rg1 -Name dbname -Location "location1, location2"

Kind                          : GlobalDocumentDB
ProvisioningState             : Succeeded
DocumentEndpoint              : https://dbname.documents.azure.com:443/
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {dbname-location1}
ReadLocations                 : {dbname-location2}
FailoverPolicies              : {dbname-location1, dbname-location2}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : location1
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/rg1/providers/Microsoft.DocumentDB/databaseAccounts/dbname
Name                          : dbname
Type                          : Microsoft.DocumentDB/databaseAccounts
```

## <span data-ttu-id="aa471-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa471-117">PARAMETERS</span></span>

### <span data-ttu-id="aa471-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa471-118">-AsJob</span></span>
<span data-ttu-id="aa471-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aa471-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa471-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa471-120">-Confirm</span></span>
<span data-ttu-id="aa471-121">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa471-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa471-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa471-122">-DefaultProfile</span></span>
<span data-ttu-id="aa471-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa471-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa471-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa471-124">-InputObject</span></span>
<span data-ttu-id="aa471-125">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa471-125">ResourceId of the resource.</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aa471-126">-Location</span><span class="sxs-lookup"><span data-stu-id="aa471-126">-Location</span></span>
<span data-ttu-id="aa471-127">Имя добавляемого расположения.</span><span class="sxs-lookup"><span data-stu-id="aa471-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="aa471-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="aa471-128">-LocationObject</span></span>
<span data-ttu-id="aa471-129">Добавьте расположение в учетную запись базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="aa471-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="aa471-130">Массив объектов PSLocation.</span><span class="sxs-lookup"><span data-stu-id="aa471-130">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa471-131">-Name</span><span class="sxs-lookup"><span data-stu-id="aa471-131">-Name</span></span>
<span data-ttu-id="aa471-132">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="aa471-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aa471-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa471-133">-ResourceGroupName</span></span>
<span data-ttu-id="aa471-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa471-134">Name of resource group.</span></span>

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

### <span data-ttu-id="aa471-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa471-135">-ResourceId</span></span>
<span data-ttu-id="aa471-136">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="aa471-136">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa471-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa471-137">-WhatIf</span></span>
<span data-ttu-id="aa471-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa471-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa471-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa471-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa471-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa471-140">CommonParameters</span></span>
<span data-ttu-id="aa471-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa471-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa471-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa471-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa471-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa471-143">INPUTS</span></span>

### <span data-ttu-id="aa471-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="aa471-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="aa471-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa471-145">OUTPUTS</span></span>

### <span data-ttu-id="aa471-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="aa471-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="aa471-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa471-147">NOTES</span></span>

## <span data-ttu-id="aa471-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa471-148">RELATED LINKS</span></span>
