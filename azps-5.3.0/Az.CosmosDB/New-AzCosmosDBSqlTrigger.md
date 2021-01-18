---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519253"
---
# <span data-ttu-id="a7186-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="a7186-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="a7186-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7186-102">SYNOPSIS</span></span>
<span data-ttu-id="a7186-103">Создается новый триггер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="a7186-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a7186-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7186-104">SYNTAX</span></span>

### <span data-ttu-id="a7186-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7186-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7186-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7186-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7186-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7186-107">DESCRIPTION</span></span>
<span data-ttu-id="a7186-108">Создается новый триггер SqlDb.</span><span class="sxs-lookup"><span data-stu-id="a7186-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="a7186-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7186-109">EXAMPLES</span></span>

### <span data-ttu-id="a7186-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7186-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="a7186-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7186-111">PARAMETERS</span></span>

### <span data-ttu-id="a7186-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a7186-112">-AccountName</span></span>
<span data-ttu-id="a7186-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="a7186-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a7186-114">-Body</span><span class="sxs-lookup"><span data-stu-id="a7186-114">-Body</span></span>
<span data-ttu-id="a7186-115">Тело триггера.</span><span class="sxs-lookup"><span data-stu-id="a7186-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="a7186-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7186-116">-Confirm</span></span>
<span data-ttu-id="a7186-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7186-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7186-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a7186-118">-ContainerName</span></span>
<span data-ttu-id="a7186-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="a7186-119">Container name.</span></span>

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

### <span data-ttu-id="a7186-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a7186-120">-DatabaseName</span></span>
<span data-ttu-id="a7186-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="a7186-121">Database name.</span></span>

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

### <span data-ttu-id="a7186-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7186-122">-DefaultProfile</span></span>
<span data-ttu-id="a7186-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7186-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7186-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a7186-124">-Name</span></span>
<span data-ttu-id="a7186-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="a7186-125">Trigger name.</span></span>

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

### <span data-ttu-id="a7186-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7186-126">-ParentObject</span></span>
<span data-ttu-id="a7186-127">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="a7186-127">Sql Container object.</span></span>

```yaml
Type: PSSqlContainerGetResults
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7186-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7186-128">-ResourceGroupName</span></span>
<span data-ttu-id="a7186-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7186-129">Name of resource group.</span></span>

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

### <span data-ttu-id="a7186-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="a7186-130">-TriggerOperation</span></span>
<span data-ttu-id="a7186-131">Операция, с помощью которая связана с триггером.</span><span class="sxs-lookup"><span data-stu-id="a7186-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="a7186-132">Возможные значения: "Все", "Создать", "Обновить", "Удалить", "Заменить"</span><span class="sxs-lookup"><span data-stu-id="a7186-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="a7186-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="a7186-133">-TriggerType</span></span>
<span data-ttu-id="a7186-134">Тип триггера.</span><span class="sxs-lookup"><span data-stu-id="a7186-134">Type of the Trigger.</span></span>
<span data-ttu-id="a7186-135">Возможные значения: Pre, 'Post'</span><span class="sxs-lookup"><span data-stu-id="a7186-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="a7186-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7186-136">-WhatIf</span></span>
<span data-ttu-id="a7186-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7186-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7186-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7186-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7186-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7186-139">CommonParameters</span></span>
<span data-ttu-id="a7186-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7186-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7186-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7186-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7186-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7186-142">INPUTS</span></span>

### <span data-ttu-id="a7186-143">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="a7186-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="a7186-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7186-144">OUTPUTS</span></span>

### <span data-ttu-id="a7186-145">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="a7186-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="a7186-146">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="a7186-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="a7186-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7186-147">NOTES</span></span>

## <span data-ttu-id="a7186-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7186-148">RELATED LINKS</span></span>
