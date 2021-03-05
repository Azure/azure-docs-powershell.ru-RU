---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: bebf801316d18b29f6444b0b369833ae547e78d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009731"
---
# <span data-ttu-id="3461a-101">Update-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="3461a-101">Update-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="3461a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3461a-102">SYNOPSIS</span></span>
<span data-ttu-id="3461a-103">Обновляет триггер SQL -10DB.</span><span class="sxs-lookup"><span data-stu-id="3461a-103">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="3461a-104">Выполняет обновление на стороне клиента, считыв существующий триггер.</span><span class="sxs-lookup"><span data-stu-id="3461a-104">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="3461a-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3461a-105">SYNTAX</span></span>

### <span data-ttu-id="3461a-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3461a-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3461a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3461a-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3461a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3461a-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlTrigger [-Name <String>] [-Body <String>] [-TriggerOperation <String>]
 [-TriggerType <String>] -InputObject <PSSqlTriggerGetResults> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3461a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3461a-109">DESCRIPTION</span></span>
<span data-ttu-id="3461a-110">Обновляет триггер SQL -10DB.</span><span class="sxs-lookup"><span data-stu-id="3461a-110">Updates the CosmosDB Sql Trigger.</span></span> <span data-ttu-id="3461a-111">Выполняет обновление на стороне клиента, считыв существующий триггер.</span><span class="sxs-lookup"><span data-stu-id="3461a-111">Performs a client side patch operation by reading the existing Trigger.</span></span>

## <span data-ttu-id="3461a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3461a-112">EXAMPLES</span></span>

### <span data-ttu-id="3461a-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3461a-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlTrigger -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myTriggerName -Body myTriggerBody -TriggerOperation All -TriggerType Pre

Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/triggers/myTriggerName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetPropertiesResource
```

## <span data-ttu-id="3461a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3461a-114">PARAMETERS</span></span>

### <span data-ttu-id="3461a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3461a-115">-AccountName</span></span>
<span data-ttu-id="3461a-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="3461a-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3461a-117">-Body</span><span class="sxs-lookup"><span data-stu-id="3461a-117">-Body</span></span>
<span data-ttu-id="3461a-118">Тело триггера.</span><span class="sxs-lookup"><span data-stu-id="3461a-118">The body of the Trigger.</span></span>

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

### <span data-ttu-id="3461a-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3461a-119">-Confirm</span></span>
<span data-ttu-id="3461a-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3461a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3461a-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="3461a-121">-ContainerName</span></span>
<span data-ttu-id="3461a-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="3461a-122">Container name.</span></span>

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

### <span data-ttu-id="3461a-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3461a-123">-DatabaseName</span></span>
<span data-ttu-id="3461a-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3461a-124">Database name.</span></span>

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

### <span data-ttu-id="3461a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3461a-125">-DefaultProfile</span></span>
<span data-ttu-id="3461a-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3461a-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3461a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3461a-127">-InputObject</span></span>
<span data-ttu-id="3461a-128">Объект-триггер Sql</span><span class="sxs-lookup"><span data-stu-id="3461a-128">Sql trigger Object</span></span>

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

### <span data-ttu-id="3461a-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3461a-129">-Name</span></span>
<span data-ttu-id="3461a-130">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="3461a-130">Trigger name.</span></span>

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

### <span data-ttu-id="3461a-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3461a-131">-ParentObject</span></span>
<span data-ttu-id="3461a-132">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="3461a-132">Sql Container object.</span></span>

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

### <span data-ttu-id="3461a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3461a-133">-ResourceGroupName</span></span>
<span data-ttu-id="3461a-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3461a-134">Name of resource group.</span></span>

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

### <span data-ttu-id="3461a-135">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="3461a-135">-TriggerOperation</span></span>
<span data-ttu-id="3461a-136">Операция, с помощью которая связана с триггером.</span><span class="sxs-lookup"><span data-stu-id="3461a-136">The operation the trigger is associated with.</span></span>
<span data-ttu-id="3461a-137">Возможные значения: "Все", "Создать", "Обновить", "Удалить", "Заменить"</span><span class="sxs-lookup"><span data-stu-id="3461a-137">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="3461a-138">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="3461a-138">-TriggerType</span></span>
<span data-ttu-id="3461a-139">Тип триггера.</span><span class="sxs-lookup"><span data-stu-id="3461a-139">Type of the Trigger.</span></span>
<span data-ttu-id="3461a-140">Возможные значения: Pre, 'Post'</span><span class="sxs-lookup"><span data-stu-id="3461a-140">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="3461a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3461a-141">-WhatIf</span></span>
<span data-ttu-id="3461a-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3461a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3461a-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3461a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3461a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3461a-144">CommonParameters</span></span>
<span data-ttu-id="3461a-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3461a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3461a-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3461a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3461a-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3461a-147">INPUTS</span></span>

### <span data-ttu-id="3461a-148">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="3461a-148">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="3461a-149">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="3461a-149">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="3461a-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3461a-150">OUTPUTS</span></span>

### <span data-ttu-id="3461a-151">Microsoft.Azure.Commands.GetsDB.Models.PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="3461a-151">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

### <span data-ttu-id="3461a-152">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="3461a-152">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="3461a-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3461a-153">NOTES</span></span>

## <span data-ttu-id="3461a-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3461a-154">RELATED LINKS</span></span>
