---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: 6fcb529b2e2ad87a2bc83421e3c5b59ae22655f6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418164"
---
# <span data-ttu-id="78a7d-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="78a7d-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="78a7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78a7d-102">SYNOPSIS</span></span>
<span data-ttu-id="78a7d-103">Обновляет триггер SQL -2016.</span><span class="sxs-lookup"><span data-stu-id="78a7d-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="78a7d-104">Выполняет обновление на стороне клиента, считыв существующий триггер.</span><span class="sxs-lookup"><span data-stu-id="78a7d-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="78a7d-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="78a7d-105">SYNTAX</span></span>

### <span data-ttu-id="78a7d-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="78a7d-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a7d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a7d-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78a7d-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="78a7d-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78a7d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="78a7d-109">DESCRIPTION</span></span>
<span data-ttu-id="78a7d-110">Обновляет триггер SQL -2016.</span><span class="sxs-lookup"><span data-stu-id="78a7d-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="78a7d-111">Выполняет обновление на стороне клиента, считыв существующий триггер.</span><span class="sxs-lookup"><span data-stu-id="78a7d-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="78a7d-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="78a7d-112">EXAMPLES</span></span>

### <span data-ttu-id="78a7d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="78a7d-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="78a7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78a7d-114">PARAMETERS</span></span>

### <span data-ttu-id="78a7d-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="78a7d-115">-AccountName</span></span>
<span data-ttu-id="78a7d-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="78a7d-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="78a7d-117">-Body</span><span class="sxs-lookup"><span data-stu-id="78a7d-117">-Body</span></span>
<span data-ttu-id="78a7d-118">Тело триггера.</span><span class="sxs-lookup"><span data-stu-id="78a7d-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="78a7d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78a7d-119">-Confirm</span></span>
<span data-ttu-id="78a7d-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a7d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78a7d-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="78a7d-121">-ContainerName</span></span>
<span data-ttu-id="78a7d-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="78a7d-122">Container name.</span></span>

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

### <span data-ttu-id="78a7d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="78a7d-123">-DatabaseName</span></span>
<span data-ttu-id="78a7d-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="78a7d-124">Database name.</span></span>

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

### <span data-ttu-id="78a7d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a7d-125">-DefaultProfile</span></span>
<span data-ttu-id="78a7d-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="78a7d-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78a7d-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78a7d-127">-InputObject</span></span>
<span data-ttu-id="78a7d-128">Объект триггера Sql</span><span class="sxs-lookup"><span data-stu-id="78a7d-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="78a7d-129">-Name</span><span class="sxs-lookup"><span data-stu-id="78a7d-129">-Name</span></span>
<span data-ttu-id="78a7d-130">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="78a7d-130">Trigger name.</span></span>

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

### <span data-ttu-id="78a7d-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="78a7d-131">-ParentObject</span></span>
<span data-ttu-id="78a7d-132">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="78a7d-132">Sql Container object.</span></span>

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

### <span data-ttu-id="78a7d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78a7d-133">-ResourceGroupName</span></span>
<span data-ttu-id="78a7d-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="78a7d-134">Name of resource group.</span></span>

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

### <span data-ttu-id="78a7d-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="78a7d-135">-TriggerOperation</span></span>
<span data-ttu-id="78a7d-136">Операция, с помощью которая связана с триггером.</span><span class="sxs-lookup"><span data-stu-id="78a7d-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="78a7d-137">Возможные значения: "Все", "Создать", "Обновить", "Удалить", "Заменить"</span><span class="sxs-lookup"><span data-stu-id="78a7d-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="78a7d-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="78a7d-138">-TriggerType</span></span>
<span data-ttu-id="78a7d-139">Тип триггера.</span><span class="sxs-lookup"><span data-stu-id="78a7d-139">Type of the Trigger.</span></span>
<span data-ttu-id="78a7d-140">Возможные значения: Pre, 'Post'</span><span class="sxs-lookup"><span data-stu-id="78a7d-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="78a7d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78a7d-141">-WhatIf</span></span>
<span data-ttu-id="78a7d-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a7d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78a7d-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="78a7d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78a7d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a7d-144">CommonParameters</span></span>
<span data-ttu-id="78a7d-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a7d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a7d-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78a7d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a7d-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="78a7d-147">INPUTS</span></span>

### <span data-ttu-id="78a7d-148">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="78a7d-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="78a7d-149">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="78a7d-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="78a7d-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="78a7d-150">OUTPUTS</span></span>

### <span data-ttu-id="78a7d-151">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="78a7d-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="78a7d-152">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="78a7d-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="78a7d-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="78a7d-153">NOTES</span></span>

## <span data-ttu-id="78a7d-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="78a7d-154">RELATED LINKS</span></span>
