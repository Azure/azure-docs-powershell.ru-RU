---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238446"
---
# <span data-ttu-id="d0282-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="d0282-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="d0282-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0282-102">SYNOPSIS</span></span>
<span data-ttu-id="d0282-103">Удаление триггера SQL вБОКDB.</span><span class="sxs-lookup"><span data-stu-id="d0282-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="d0282-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d0282-104">SYNTAX</span></span>

### <span data-ttu-id="d0282-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0282-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0282-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0282-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0282-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0282-107">DESCRIPTION</span></span>
<span data-ttu-id="d0282-108">Для **удаления SQL-триггера AzCosmosDBSqlTrigger** удаляется Sql Trigger, соответствующий заданным названиям группы ресурсов, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="d0282-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="d0282-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d0282-109">EXAMPLES</span></span>

### <span data-ttu-id="d0282-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0282-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="d0282-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0282-111">PARAMETERS</span></span>

### <span data-ttu-id="d0282-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d0282-112">-AccountName</span></span>
<span data-ttu-id="d0282-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="d0282-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d0282-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0282-114">-Confirm</span></span>
<span data-ttu-id="d0282-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d0282-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0282-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d0282-116">-ContainerName</span></span>
<span data-ttu-id="d0282-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="d0282-117">Container name.</span></span>

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

### <span data-ttu-id="d0282-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0282-118">-DatabaseName</span></span>
<span data-ttu-id="d0282-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d0282-119">Database name.</span></span>

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

### <span data-ttu-id="d0282-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0282-120">-DefaultProfile</span></span>
<span data-ttu-id="d0282-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0282-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0282-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0282-122">-InputObject</span></span>
<span data-ttu-id="d0282-123">Объект-триггер Sql</span><span class="sxs-lookup"><span data-stu-id="d0282-123">Sql trigger Object</span></span>

```yaml
Type: PSSqlTriggerGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0282-124">-Name</span><span class="sxs-lookup"><span data-stu-id="d0282-124">-Name</span></span>
<span data-ttu-id="d0282-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="d0282-125">Trigger name.</span></span>

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

### <span data-ttu-id="d0282-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0282-126">-PassThru</span></span>
<span data-ttu-id="d0282-127">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="d0282-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="d0282-128">Результат является истинным, если операция прошла успешно и если она не произошла, вы ошибку.</span><span class="sxs-lookup"><span data-stu-id="d0282-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="d0282-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0282-129">-ResourceGroupName</span></span>
<span data-ttu-id="d0282-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d0282-130">Name of resource group.</span></span>

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

### <span data-ttu-id="d0282-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0282-131">-WhatIf</span></span>
<span data-ttu-id="d0282-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0282-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0282-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d0282-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0282-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0282-134">CommonParameters</span></span>
<span data-ttu-id="d0282-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0282-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0282-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0282-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0282-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d0282-137">INPUTS</span></span>

### <span data-ttu-id="d0282-138">Нет</span><span class="sxs-lookup"><span data-stu-id="d0282-138">None</span></span>

## <span data-ttu-id="d0282-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0282-139">OUTPUTS</span></span>

### <span data-ttu-id="d0282-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="d0282-140">System.Void</span></span>

### <span data-ttu-id="d0282-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0282-141">System.Boolean</span></span>

## <span data-ttu-id="d0282-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d0282-142">NOTES</span></span>

## <span data-ttu-id="d0282-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0282-143">RELATED LINKS</span></span>
