---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: da512c08120c65f68c39c5072a3e770886ec5031
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314720"
---
# <span data-ttu-id="16213-101">New-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="16213-101">New-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="16213-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16213-102">SYNOPSIS</span></span>
<span data-ttu-id="16213-103">Создает новый триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="16213-103">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="16213-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16213-104">SYNTAX</span></span>

### <span data-ttu-id="16213-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16213-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16213-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16213-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16213-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16213-107">DESCRIPTION</span></span>
<span data-ttu-id="16213-108">Создает новый триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="16213-108">Creates a new CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="16213-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16213-109">EXAMPLES</span></span>

### <span data-ttu-id="16213-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16213-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="16213-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16213-111">PARAMETERS</span></span>

### <span data-ttu-id="16213-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="16213-112">-AccountName</span></span>
<span data-ttu-id="16213-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="16213-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="16213-114">-Body</span><span class="sxs-lookup"><span data-stu-id="16213-114">-Body</span></span>
<span data-ttu-id="16213-115">Основной текст триггера.</span><span class="sxs-lookup"><span data-stu-id="16213-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="16213-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16213-116">-Confirm</span></span>
<span data-ttu-id="16213-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="16213-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16213-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="16213-118">-ContainerName</span></span>
<span data-ttu-id="16213-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="16213-119">Container name.</span></span>

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

### <span data-ttu-id="16213-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16213-120">-DatabaseName</span></span>
<span data-ttu-id="16213-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="16213-121">Database name.</span></span>

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

### <span data-ttu-id="16213-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16213-122">-DefaultProfile</span></span>
<span data-ttu-id="16213-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16213-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16213-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="16213-124">-Name</span></span>
<span data-ttu-id="16213-125">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="16213-125">Trigger name.</span></span>

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

### <span data-ttu-id="16213-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="16213-126">-ParentObject</span></span>
<span data-ttu-id="16213-127">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="16213-127">Sql Container object.</span></span>

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

### <span data-ttu-id="16213-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16213-128">-ResourceGroupName</span></span>
<span data-ttu-id="16213-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16213-129">Name of resource group.</span></span>

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

### <span data-ttu-id="16213-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="16213-130">-TriggerOperation</span></span>
<span data-ttu-id="16213-131">Операция, с которой связан триггер.</span><span class="sxs-lookup"><span data-stu-id="16213-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="16213-132">Возможные значения: "все", "создать", "Обновить", "Удалить", "заменить"</span><span class="sxs-lookup"><span data-stu-id="16213-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="16213-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="16213-133">-TriggerType</span></span>
<span data-ttu-id="16213-134">Тип триггера.</span><span class="sxs-lookup"><span data-stu-id="16213-134">Type of the Trigger.</span></span>
<span data-ttu-id="16213-135">Возможные значения: "Pre", "Post"</span><span class="sxs-lookup"><span data-stu-id="16213-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="16213-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16213-136">-WhatIf</span></span>
<span data-ttu-id="16213-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="16213-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16213-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="16213-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16213-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16213-139">CommonParameters</span></span>
<span data-ttu-id="16213-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16213-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16213-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="16213-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16213-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16213-142">INPUTS</span></span>

### <span data-ttu-id="16213-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="16213-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="16213-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16213-144">OUTPUTS</span></span>

### <span data-ttu-id="16213-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="16213-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="16213-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="16213-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="16213-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="16213-147">NOTES</span></span>

## <span data-ttu-id="16213-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16213-148">RELATED LINKS</span></span>