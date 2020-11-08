---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountRegion.md
ms.openlocfilehash: bfbbc0b4d5fbaac1dc6ad5f18af2cb201e5124c8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236844"
---
# <span data-ttu-id="2d14e-101">Update-AzCosmosDBAccountRegion</span><span class="sxs-lookup"><span data-stu-id="2d14e-101">Update-AzCosmosDBAccountRegion</span></span>

## <span data-ttu-id="2d14e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d14e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d14e-103">Обновление регионов учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2d14e-103">Update Regions of a CosmosDB Account.</span></span>

## <span data-ttu-id="2d14e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d14e-104">SYNTAX</span></span>

### <span data-ttu-id="2d14e-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d14e-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountRegion -ResourceGroupName <String> -Name <String> [-Location <String[]>]
 [-LocationObject <PSLocation[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d14e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d14e-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d14e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d14e-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountRegion [-Location <String[]>] [-LocationObject <PSLocation[]>]
 -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d14e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d14e-108">DESCRIPTION</span></span>
<span data-ttu-id="2d14e-109">Обновление регионов учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="2d14e-109">Update Regions of a CosmosDB Account.</span></span> <span data-ttu-id="2d14e-110">Расположение может быть предоставлено как объект типа PSLocation или строки названия расположения, упорядоченного по приоритету отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="2d14e-110">Location can be provided either as an object of type PSLocation or as strings of Location Name ordered by failover priority.</span></span>
<span data-ttu-id="2d14e-111">В параметре LocationObject ожидается список текущих местоположений (включена отработка отказа prioritiies), добавленных новым LocationObjects, соответствующим новым местам, которые нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="2d14e-111">LocationObject parameter expects the list of current locations (failover prioritiies included) appended by the new LocationObjects corresponding to new locations to be added.</span></span>
<span data-ttu-id="2d14e-112">Для параметра Location ожидается список текущих расположений (приоритет отработки отказа) и новое расположение.</span><span class="sxs-lookup"><span data-stu-id="2d14e-112">Location parameter expects the list of current location(ordered by failover priority) and the new locations.</span></span> <span data-ttu-id="2d14e-113">Обратите внимание, что поддерживается только добавление областей.</span><span class="sxs-lookup"><span data-stu-id="2d14e-113">Please note, we only support Addition of Regions.</span></span> <span data-ttu-id="2d14e-114">Укажите либо расположение, либо LocationObject.</span><span class="sxs-lookup"><span data-stu-id="2d14e-114">Please provide either Location or LocationObject.</span></span>

## <span data-ttu-id="2d14e-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d14e-115">EXAMPLES</span></span>

### <span data-ttu-id="2d14e-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d14e-116">Example 1</span></span>
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

## <span data-ttu-id="2d14e-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d14e-117">PARAMETERS</span></span>

### <span data-ttu-id="2d14e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d14e-118">-AsJob</span></span>
<span data-ttu-id="2d14e-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2d14e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d14e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d14e-120">-Confirm</span></span>
<span data-ttu-id="2d14e-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d14e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d14e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d14e-122">-DefaultProfile</span></span>
<span data-ttu-id="2d14e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d14e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d14e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2d14e-124">-InputObject</span></span>
<span data-ttu-id="2d14e-125">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d14e-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2d14e-126">-Location</span><span class="sxs-lookup"><span data-stu-id="2d14e-126">-Location</span></span>
<span data-ttu-id="2d14e-127">Имя добавляемого расположения.</span><span class="sxs-lookup"><span data-stu-id="2d14e-127">Name of the location to be added.</span></span>

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

### <span data-ttu-id="2d14e-128">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="2d14e-128">-LocationObject</span></span>
<span data-ttu-id="2d14e-129">Добавьте расположение в учетную запись базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2d14e-129">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="2d14e-130">Массив объектов PSLocation.</span><span class="sxs-lookup"><span data-stu-id="2d14e-130">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="2d14e-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d14e-131">-Name</span></span>
<span data-ttu-id="2d14e-132">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="2d14e-132">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2d14e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d14e-133">-ResourceGroupName</span></span>
<span data-ttu-id="2d14e-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d14e-134">Name of resource group.</span></span>

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

### <span data-ttu-id="2d14e-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d14e-135">-ResourceId</span></span>
<span data-ttu-id="2d14e-136">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="2d14e-136">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="2d14e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d14e-137">-WhatIf</span></span>
<span data-ttu-id="2d14e-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d14e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d14e-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d14e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d14e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d14e-140">CommonParameters</span></span>
<span data-ttu-id="2d14e-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d14e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d14e-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d14e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d14e-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d14e-143">INPUTS</span></span>

### <span data-ttu-id="2d14e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2d14e-144">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2d14e-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d14e-145">OUTPUTS</span></span>

### <span data-ttu-id="2d14e-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="2d14e-146">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="2d14e-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d14e-147">NOTES</span></span>

## <span data-ttu-id="2d14e-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d14e-148">RELATED LINKS</span></span>
