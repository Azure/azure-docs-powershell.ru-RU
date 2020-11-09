---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314486"
---
# <span data-ttu-id="f0ce9-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="f0ce9-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="f0ce9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0ce9-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ce9-103">Обновляет триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="f0ce9-104">Выполняет операцию исправления на стороне клиента, считывая существующий триггер.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="f0ce9-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0ce9-105">SYNTAX</span></span>

### <span data-ttu-id="f0ce9-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0ce9-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ce9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ce9-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0ce9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0ce9-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0ce9-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0ce9-109">DESCRIPTION</span></span>
<span data-ttu-id="f0ce9-110">Обновляет триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="f0ce9-111">Выполняет операцию исправления на стороне клиента, считывая существующий триггер.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="f0ce9-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0ce9-112">EXAMPLES</span></span>

### <span data-ttu-id="f0ce9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0ce9-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="f0ce9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0ce9-114">PARAMETERS</span></span>

### <span data-ttu-id="f0ce9-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f0ce9-115">-AccountName</span></span>
<span data-ttu-id="f0ce9-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f0ce9-117">-Body</span><span class="sxs-lookup"><span data-stu-id="f0ce9-117">-Body</span></span>
<span data-ttu-id="f0ce9-118">Основной текст триггера.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="f0ce9-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0ce9-119">-Confirm</span></span>
<span data-ttu-id="f0ce9-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0ce9-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f0ce9-121">-ContainerName</span></span>
<span data-ttu-id="f0ce9-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-122">Container name.</span></span>

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

### <span data-ttu-id="f0ce9-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f0ce9-123">-DatabaseName</span></span>
<span data-ttu-id="f0ce9-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-124">Database name.</span></span>

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

### <span data-ttu-id="f0ce9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ce9-125">-DefaultProfile</span></span>
<span data-ttu-id="f0ce9-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ce9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0ce9-127">-InputObject</span></span>
<span data-ttu-id="f0ce9-128">Объект триггера SQL</span><span class="sxs-lookup"><span data-stu-id="f0ce9-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="f0ce9-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0ce9-129">-Name</span></span>
<span data-ttu-id="f0ce9-130">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-130">Trigger name.</span></span>

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

### <span data-ttu-id="f0ce9-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f0ce9-131">-ParentObject</span></span>
<span data-ttu-id="f0ce9-132">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-132">Sql Container object.</span></span>

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

### <span data-ttu-id="f0ce9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ce9-133">-ResourceGroupName</span></span>
<span data-ttu-id="f0ce9-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-134">Name of resource group.</span></span>

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

### <span data-ttu-id="f0ce9-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="f0ce9-135">-TriggerOperation</span></span>
<span data-ttu-id="f0ce9-136">Операция, с которой связан триггер.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="f0ce9-137">Возможные значения: "все", "создать", "Обновить", "Удалить", "заменить"</span><span class="sxs-lookup"><span data-stu-id="f0ce9-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="f0ce9-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="f0ce9-138">-TriggerType</span></span>
<span data-ttu-id="f0ce9-139">Тип триггера.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-139">Type of the Trigger.</span></span>
<span data-ttu-id="f0ce9-140">Возможные значения: "Pre", "Post"</span><span class="sxs-lookup"><span data-stu-id="f0ce9-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="f0ce9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0ce9-141">-WhatIf</span></span>
<span data-ttu-id="f0ce9-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0ce9-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0ce9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ce9-144">CommonParameters</span></span>
<span data-ttu-id="f0ce9-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0ce9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ce9-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0ce9-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ce9-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0ce9-147">INPUTS</span></span>

### <span data-ttu-id="f0ce9-148">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="f0ce9-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="f0ce9-149">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f0ce9-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="f0ce9-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0ce9-150">OUTPUTS</span></span>

### <span data-ttu-id="f0ce9-151">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="f0ce9-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="f0ce9-152">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f0ce9-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f0ce9-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0ce9-153">NOTES</span></span>

## <span data-ttu-id="f0ce9-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0ce9-154">RELATED LINKS</span></span>
