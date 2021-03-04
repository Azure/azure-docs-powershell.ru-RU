---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 4838a2de4a61d0c00371ab018d441dcd52bec699
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971304"
---
# <span data-ttu-id="6ead3-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="6ead3-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="6ead3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ead3-102">SYNOPSIS</span></span>
<span data-ttu-id="6ead3-103">Удаление Графа Гремлина (1АDB).</span><span class="sxs-lookup"><span data-stu-id="6ead3-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6ead3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ead3-104">SYNTAX</span></span>

### <span data-ttu-id="6ead3-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ead3-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ead3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ead3-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ead3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ead3-107">DESCRIPTION</span></span>
<span data-ttu-id="6ead3-108">С **помощью cmdlet Remove-AzCosmosDBGremlinGraph** удаляется диаграмма Гремлин Графа ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="6ead3-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="6ead3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ead3-109">EXAMPLES</span></span>

### <span data-ttu-id="6ead3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6ead3-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="6ead3-111">В случае успешного удаления cmdlet возвращает объект типа bool(когда -PassThru is passThru), который является истинным.</span><span class="sxs-lookup"><span data-stu-id="6ead3-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="6ead3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ead3-112">PARAMETERS</span></span>

### <span data-ttu-id="6ead3-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6ead3-113">-AccountName</span></span>
<span data-ttu-id="6ead3-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="6ead3-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6ead3-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ead3-115">-Confirm</span></span>
<span data-ttu-id="6ead3-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6ead3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ead3-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ead3-117">-DatabaseName</span></span>
<span data-ttu-id="6ead3-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6ead3-118">Database name.</span></span>

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

### <span data-ttu-id="6ead3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ead3-119">-DefaultProfile</span></span>
<span data-ttu-id="6ead3-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ead3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ead3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ead3-121">-InputObject</span></span>
<span data-ttu-id="6ead3-122">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="6ead3-122">Gremlin Graph object.</span></span>

```yaml
Type: PSGremlinGraphGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ead3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6ead3-123">-Name</span></span>
<span data-ttu-id="6ead3-124">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="6ead3-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="6ead3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ead3-125">-PassThru</span></span>
<span data-ttu-id="6ead3-126">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="6ead3-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="6ead3-127">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="6ead3-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="6ead3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ead3-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ead3-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ead3-129">Name of resource group.</span></span>

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

### <span data-ttu-id="6ead3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ead3-130">-WhatIf</span></span>
<span data-ttu-id="6ead3-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ead3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ead3-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ead3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ead3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ead3-133">CommonParameters</span></span>
<span data-ttu-id="6ead3-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ead3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ead3-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ead3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ead3-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ead3-136">INPUTS</span></span>

### <span data-ttu-id="6ead3-137">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="6ead3-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="6ead3-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ead3-138">OUTPUTS</span></span>

### <span data-ttu-id="6ead3-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="6ead3-139">System.Void</span></span>

### <span data-ttu-id="6ead3-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ead3-140">System.Boolean</span></span>

## <span data-ttu-id="6ead3-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ead3-141">NOTES</span></span>

## <span data-ttu-id="6ead3-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ead3-142">RELATED LINKS</span></span>
