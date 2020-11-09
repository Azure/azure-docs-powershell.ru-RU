---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314483"
---
# <span data-ttu-id="e64af-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="e64af-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="e64af-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e64af-102">SYNOPSIS</span></span>
<span data-ttu-id="e64af-103">Обновляет CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="e64af-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="e64af-104">Выполняет операцию исправления на стороне клиента, считывая существующий UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="e64af-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="e64af-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e64af-105">SYNTAX</span></span>

### <span data-ttu-id="e64af-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e64af-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e64af-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e64af-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e64af-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e64af-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e64af-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e64af-109">DESCRIPTION</span></span>
<span data-ttu-id="e64af-110">Обновляет CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="e64af-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="e64af-111">Выполняет операцию исправления на стороне клиента, считывая существующий UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="e64af-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="e64af-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e64af-112">EXAMPLES</span></span>

### <span data-ttu-id="e64af-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e64af-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="e64af-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e64af-114">PARAMETERS</span></span>

### <span data-ttu-id="e64af-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="e64af-115">-AccountName</span></span>
<span data-ttu-id="e64af-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="e64af-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e64af-117">-Body</span><span class="sxs-lookup"><span data-stu-id="e64af-117">-Body</span></span>
<span data-ttu-id="e64af-118">Текст пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="e64af-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="e64af-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e64af-119">-Confirm</span></span>
<span data-ttu-id="e64af-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e64af-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e64af-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e64af-121">-ContainerName</span></span>
<span data-ttu-id="e64af-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="e64af-122">Container name.</span></span>

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

### <span data-ttu-id="e64af-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e64af-123">-DatabaseName</span></span>
<span data-ttu-id="e64af-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="e64af-124">Database name.</span></span>

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

### <span data-ttu-id="e64af-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64af-125">-DefaultProfile</span></span>
<span data-ttu-id="e64af-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e64af-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e64af-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e64af-127">-InputObject</span></span>
<span data-ttu-id="e64af-128">Объект пользовательской функции SQL</span><span class="sxs-lookup"><span data-stu-id="e64af-128">Sql User Defined Function Object</span></span>

```yaml
Type: PSSqlUserDefinedFunctionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e64af-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e64af-129">-Name</span></span>
<span data-ttu-id="e64af-130">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="e64af-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="e64af-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e64af-131">-ParentObject</span></span>
<span data-ttu-id="e64af-132">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="e64af-132">Sql Container object.</span></span>

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

### <span data-ttu-id="e64af-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e64af-133">-ResourceGroupName</span></span>
<span data-ttu-id="e64af-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e64af-134">Name of resource group.</span></span>

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

### <span data-ttu-id="e64af-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64af-135">-WhatIf</span></span>
<span data-ttu-id="e64af-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e64af-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e64af-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e64af-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e64af-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64af-138">CommonParameters</span></span>
<span data-ttu-id="e64af-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e64af-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64af-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e64af-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64af-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e64af-141">INPUTS</span></span>

### <span data-ttu-id="e64af-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="e64af-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="e64af-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="e64af-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="e64af-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e64af-144">OUTPUTS</span></span>

### <span data-ttu-id="e64af-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="e64af-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="e64af-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="e64af-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="e64af-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="e64af-147">NOTES</span></span>

## <span data-ttu-id="e64af-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e64af-148">RELATED LINKS</span></span>
