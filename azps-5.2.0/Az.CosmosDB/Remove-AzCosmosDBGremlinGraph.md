---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404780"
---
# <span data-ttu-id="edb16-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="edb16-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="edb16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb16-102">SYNOPSIS</span></span>
<span data-ttu-id="edb16-103">Удаление Графа Гремлина (1АDB).</span><span class="sxs-lookup"><span data-stu-id="edb16-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="edb16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="edb16-104">SYNTAX</span></span>

### <span data-ttu-id="edb16-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="edb16-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="edb16-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edb16-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edb16-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="edb16-107">DESCRIPTION</span></span>
<span data-ttu-id="edb16-108">С **помощью cmdlet Remove-AzCosmosDBGremlinGraph** удаляется диаграмма Гремлин Графа ВайсDB.</span><span class="sxs-lookup"><span data-stu-id="edb16-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="edb16-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="edb16-109">EXAMPLES</span></span>

### <span data-ttu-id="edb16-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="edb16-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="edb16-111">Если удаление прошло успешно, он возвращает объект типа bool(при -PassThru).</span><span class="sxs-lookup"><span data-stu-id="edb16-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="edb16-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edb16-112">PARAMETERS</span></span>

### <span data-ttu-id="edb16-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="edb16-113">-AccountName</span></span>
<span data-ttu-id="edb16-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="edb16-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="edb16-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="edb16-115">-Confirm</span></span>
<span data-ttu-id="edb16-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="edb16-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edb16-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="edb16-117">-DatabaseName</span></span>
<span data-ttu-id="edb16-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="edb16-118">Database name.</span></span>

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

### <span data-ttu-id="edb16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb16-119">-DefaultProfile</span></span>
<span data-ttu-id="edb16-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="edb16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb16-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edb16-121">-InputObject</span></span>
<span data-ttu-id="edb16-122">Объект Гремлин График.</span><span class="sxs-lookup"><span data-stu-id="edb16-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="edb16-123">-Name</span><span class="sxs-lookup"><span data-stu-id="edb16-123">-Name</span></span>
<span data-ttu-id="edb16-124">Имя графика Гремлин.</span><span class="sxs-lookup"><span data-stu-id="edb16-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="edb16-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="edb16-125">-PassThru</span></span>
<span data-ttu-id="edb16-126">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="edb16-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="edb16-127">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="edb16-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="edb16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edb16-128">-ResourceGroupName</span></span>
<span data-ttu-id="edb16-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="edb16-129">Name of resource group.</span></span>

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

### <span data-ttu-id="edb16-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edb16-130">-WhatIf</span></span>
<span data-ttu-id="edb16-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edb16-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edb16-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="edb16-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edb16-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb16-133">CommonParameters</span></span>
<span data-ttu-id="edb16-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edb16-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb16-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edb16-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb16-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="edb16-136">INPUTS</span></span>

### <span data-ttu-id="edb16-137">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="edb16-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="edb16-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="edb16-138">OUTPUTS</span></span>

### <span data-ttu-id="edb16-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="edb16-139">System.Void</span></span>

### <span data-ttu-id="edb16-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="edb16-140">System.Boolean</span></span>

## <span data-ttu-id="edb16-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="edb16-141">NOTES</span></span>

## <span data-ttu-id="edb16-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="edb16-142">RELATED LINKS</span></span>
