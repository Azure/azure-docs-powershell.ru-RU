---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqltrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlTrigger.md
ms.openlocfilehash: a67b2a665f763c32876177414a347270f557c914
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065020"
---
# <span data-ttu-id="5525d-101">Set-AzCosmosDBSqlTrigger</span><span class="sxs-lookup"><span data-stu-id="5525d-101">Set-AzCosmosDBSqlTrigger</span></span>

## <span data-ttu-id="5525d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5525d-102">SYNOPSIS</span></span>
<span data-ttu-id="5525d-103">Создает новый или обновляет существующий триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5525d-103">Creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5525d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5525d-104">SYNTAX</span></span>

### <span data-ttu-id="5525d-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5525d-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlTrigger -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5525d-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5525d-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlTrigger -Name <String> -Body <String> [-TriggerOperation <String>] [-TriggerType <String>]
 -InputObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5525d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5525d-107">DESCRIPTION</span></span>
<span data-ttu-id="5525d-108">Командлет **Set-AzCosmosDBSqlTrigger** создает новый или обновляет существующий триггер SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5525d-108">The **Set-AzCosmosDBSqlTrigger** cmdlet creates a new or updates an existing CosmosDB Sql Trigger.</span></span>

## <span data-ttu-id="5525d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5525d-109">EXAMPLES</span></span>

### <span data-ttu-id="5525d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5525d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlTrigger -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {triggerName} -ContainerName {containerName} -Body {sampleBody}

Name                   : {triggerName}
Id                     : {triggerId}
SqlTriggerGetResultsId :
Body                   :
TriggerType            :
TriggerOperation       :
_rid                   :
_ts                    :
_etag                  :
```

## <span data-ttu-id="5525d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5525d-111">PARAMETERS</span></span>

### <span data-ttu-id="5525d-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5525d-112">-AccountName</span></span>
<span data-ttu-id="5525d-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5525d-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5525d-114">-Body</span><span class="sxs-lookup"><span data-stu-id="5525d-114">-Body</span></span>
<span data-ttu-id="5525d-115">Основной текст триггера.</span><span class="sxs-lookup"><span data-stu-id="5525d-115">The body of the Trigger.</span></span>

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

### <span data-ttu-id="5525d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5525d-116">-Confirm</span></span>
<span data-ttu-id="5525d-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5525d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5525d-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="5525d-118">-ContainerName</span></span>
<span data-ttu-id="5525d-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="5525d-119">Container name.</span></span>

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

### <span data-ttu-id="5525d-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5525d-120">-DatabaseName</span></span>
<span data-ttu-id="5525d-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5525d-121">Database name.</span></span>

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

### <span data-ttu-id="5525d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5525d-122">-DefaultProfile</span></span>
<span data-ttu-id="5525d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5525d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5525d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5525d-124">-InputObject</span></span>
<span data-ttu-id="5525d-125">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="5525d-125">Sql Container object.</span></span>

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

### <span data-ttu-id="5525d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5525d-126">-Name</span></span>
<span data-ttu-id="5525d-127">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="5525d-127">Trigger name.</span></span>

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

### <span data-ttu-id="5525d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5525d-128">-ResourceGroupName</span></span>
<span data-ttu-id="5525d-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5525d-129">Name of resource group.</span></span>

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

### <span data-ttu-id="5525d-130">-TriggerOperation</span><span class="sxs-lookup"><span data-stu-id="5525d-130">-TriggerOperation</span></span>
<span data-ttu-id="5525d-131">Операция, с которой связан триггер.</span><span class="sxs-lookup"><span data-stu-id="5525d-131">The operation the trigger is associated with.</span></span>
<span data-ttu-id="5525d-132">Возможные значения: "все", "создать", "Обновить", "Удалить", "заменить"</span><span class="sxs-lookup"><span data-stu-id="5525d-132">Possible values include: 'All', 'Create', 'Update', 'Delete', 'Replace'</span></span>

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

### <span data-ttu-id="5525d-133">-TriggerType</span><span class="sxs-lookup"><span data-stu-id="5525d-133">-TriggerType</span></span>
<span data-ttu-id="5525d-134">Тип триггера.</span><span class="sxs-lookup"><span data-stu-id="5525d-134">Type of the Trigger.</span></span>
<span data-ttu-id="5525d-135">Возможные значения: "Pre", "Post"</span><span class="sxs-lookup"><span data-stu-id="5525d-135">Possible values include: 'Pre', 'Post'</span></span>

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

### <span data-ttu-id="5525d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5525d-136">-WhatIf</span></span>
<span data-ttu-id="5525d-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5525d-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5525d-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5525d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5525d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5525d-139">CommonParameters</span></span>
<span data-ttu-id="5525d-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5525d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5525d-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5525d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5525d-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5525d-142">INPUTS</span></span>

### <span data-ttu-id="5525d-143">Ничего</span><span class="sxs-lookup"><span data-stu-id="5525d-143">None</span></span>

## <span data-ttu-id="5525d-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5525d-144">OUTPUTS</span></span>

### <span data-ttu-id="5525d-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlTriggerGetResults</span><span class="sxs-lookup"><span data-stu-id="5525d-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlTriggerGetResults</span></span>

## <span data-ttu-id="5525d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="5525d-146">NOTES</span></span>

## <span data-ttu-id="5525d-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5525d-147">RELATED LINKS</span></span>
