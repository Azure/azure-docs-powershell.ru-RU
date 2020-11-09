---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlingraph
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinGraph.md
ms.openlocfilehash: 560fcaa33e635eefd4ba94c5c7cbd05cba1cc304
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314660"
---
# <span data-ttu-id="47b2b-101">Remove-AzCosmosDBGremlinGraph</span><span class="sxs-lookup"><span data-stu-id="47b2b-101">Remove-AzCosmosDBGremlinGraph</span></span>

## <span data-ttu-id="47b2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="47b2b-103">Удаление CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="47b2b-103">Deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="47b2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47b2b-104">SYNTAX</span></span>

### <span data-ttu-id="47b2b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="47b2b-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBGremlinGraph -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="47b2b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47b2b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinGraph -InputObject <PSGremlinGraphGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47b2b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b2b-107">DESCRIPTION</span></span>
<span data-ttu-id="47b2b-108">Командлет **Remove-AzCosmosDBGremlinGraph** удаляет CosmosDB Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="47b2b-108">The **Remove-AzCosmosDBGremlinGraph** cmdlet deletes a CosmosDB Gremlin Graph.</span></span>

## <span data-ttu-id="47b2b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47b2b-109">EXAMPLES</span></span>

### <span data-ttu-id="47b2b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="47b2b-110">Example 1</span></span>
```powershell
Remove-AzCosmosDBGremlinGraph -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {graphName}
```

<span data-ttu-id="47b2b-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="47b2b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="47b2b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47b2b-112">PARAMETERS</span></span>

### <span data-ttu-id="47b2b-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="47b2b-113">-AccountName</span></span>
<span data-ttu-id="47b2b-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="47b2b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="47b2b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47b2b-115">-Confirm</span></span>
<span data-ttu-id="47b2b-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47b2b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47b2b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47b2b-117">-DatabaseName</span></span>
<span data-ttu-id="47b2b-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="47b2b-118">Database name.</span></span>

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

### <span data-ttu-id="47b2b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47b2b-119">-DefaultProfile</span></span>
<span data-ttu-id="47b2b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47b2b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47b2b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47b2b-121">-InputObject</span></span>
<span data-ttu-id="47b2b-122">Объект Gremlin Graph.</span><span class="sxs-lookup"><span data-stu-id="47b2b-122">Gremlin Graph object.</span></span>

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

### <span data-ttu-id="47b2b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47b2b-123">-Name</span></span>
<span data-ttu-id="47b2b-124">Имя графа Gremlin.</span><span class="sxs-lookup"><span data-stu-id="47b2b-124">Gremlin Graph Name.</span></span>

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

### <span data-ttu-id="47b2b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47b2b-125">-PassThru</span></span>
<span data-ttu-id="47b2b-126">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="47b2b-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="47b2b-127">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="47b2b-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="47b2b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47b2b-128">-ResourceGroupName</span></span>
<span data-ttu-id="47b2b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="47b2b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="47b2b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47b2b-130">-WhatIf</span></span>
<span data-ttu-id="47b2b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47b2b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47b2b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47b2b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47b2b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47b2b-133">CommonParameters</span></span>
<span data-ttu-id="47b2b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47b2b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47b2b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47b2b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47b2b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47b2b-136">INPUTS</span></span>

### <span data-ttu-id="47b2b-137">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinGraphGetResults</span><span class="sxs-lookup"><span data-stu-id="47b2b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinGraphGetResults</span></span>

## <span data-ttu-id="47b2b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47b2b-138">OUTPUTS</span></span>

### <span data-ttu-id="47b2b-139">System. void</span><span class="sxs-lookup"><span data-stu-id="47b2b-139">System.Void</span></span>

### <span data-ttu-id="47b2b-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47b2b-140">System.Boolean</span></span>

## <span data-ttu-id="47b2b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="47b2b-141">NOTES</span></span>

## <span data-ttu-id="47b2b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47b2b-142">RELATED LINKS</span></span>
