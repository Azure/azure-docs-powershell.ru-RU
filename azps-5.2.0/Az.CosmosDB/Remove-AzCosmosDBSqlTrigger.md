---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 8aca11c8ce56c42842e96fa1e3623979612ffec7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409068"
---
# <span data-ttu-id="dd2bf-101">Remove-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="dd2bf-101">Remove-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="dd2bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2bf-103">Удаление триггера SQL в КDB.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-103">Deletes the CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="dd2bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dd2bf-104">SYNTAX</span></span>

### <span data-ttu-id="dd2bf-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd2bf-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd2bf-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd2bf-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlTrigger -InputObject <PSSqlTriggerGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2bf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dd2bf-107">DESCRIPTION</span></span>
<span data-ttu-id="dd2bf-108">Для **удаления SQL-триггера AzCosmosDBSqlTrigger** удаляется Sql-триггер ВайтсDB, соответствующий заданным названиям группы ресурсов, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-108">The **Remove-AzCosmosDBSqlTrigger** cmdlet deletes the CosmosDB Sql Trigger corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="dd2bf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dd2bf-109">EXAMPLES</span></span>

### <span data-ttu-id="dd2bf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dd2bf-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlTrigger -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {triggerName}
```

## <span data-ttu-id="dd2bf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd2bf-111">PARAMETERS</span></span>

### <span data-ttu-id="dd2bf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dd2bf-112">-AccountName</span></span>
<span data-ttu-id="dd2bf-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="dd2bf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="dd2bf-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd2bf-114">-Confirm</span></span>
<span data-ttu-id="dd2bf-115">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd2bf-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="dd2bf-116">-ContainerName</span></span>
<span data-ttu-id="dd2bf-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-117">Container name.</span></span>

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

### <span data-ttu-id="dd2bf-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd2bf-118">-DatabaseName</span></span>
<span data-ttu-id="dd2bf-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-119">Database name.</span></span>

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

### <span data-ttu-id="dd2bf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2bf-120">-DefaultProfile</span></span>
<span data-ttu-id="dd2bf-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd2bf-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd2bf-122">-InputObject</span></span>
<span data-ttu-id="dd2bf-123">Объект триггера Sql</span><span class="sxs-lookup"><span data-stu-id="dd2bf-123">Sql trigger Object</span></span>

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

### <span data-ttu-id="dd2bf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dd2bf-124">-Name</span></span>
<span data-ttu-id="dd2bf-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-125">Trigger name.</span></span>

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

### <span data-ttu-id="dd2bf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dd2bf-126">-PassThru</span></span>
<span data-ttu-id="dd2bf-127">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="dd2bf-128">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="dd2bf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2bf-129">-ResourceGroupName</span></span>
<span data-ttu-id="dd2bf-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-130">Name of resource group.</span></span>

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

### <span data-ttu-id="dd2bf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2bf-131">-WhatIf</span></span>
<span data-ttu-id="dd2bf-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2bf-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd2bf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2bf-134">CommonParameters</span></span>
<span data-ttu-id="dd2bf-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2bf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2bf-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd2bf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2bf-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dd2bf-137">INPUTS</span></span>

### <span data-ttu-id="dd2bf-138">Нет</span><span class="sxs-lookup"><span data-stu-id="dd2bf-138">None</span></span>

## <span data-ttu-id="dd2bf-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd2bf-139">OUTPUTS</span></span>

### <span data-ttu-id="dd2bf-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="dd2bf-140">System.Void</span></span>

### <span data-ttu-id="dd2bf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dd2bf-141">System.Boolean</span></span>

## <span data-ttu-id="dd2bf-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dd2bf-142">NOTES</span></span>

## <span data-ttu-id="dd2bf-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dd2bf-143">RELATED LINKS</span></span>
