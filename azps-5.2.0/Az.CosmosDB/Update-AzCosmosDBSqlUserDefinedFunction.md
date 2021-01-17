---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: e197e648b06e2183572001ee12a7a8552a158009
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401388"
---
# <span data-ttu-id="9dc86-101">Update-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="9dc86-101">Update-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="9dc86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dc86-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc86-103">Обновляет Точки Sql UserDefinedFunction в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="9dc86-103">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="9dc86-104">Выполняет обновление на стороне клиента с помощью существующей userDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="9dc86-104">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="9dc86-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9dc86-105">SYNTAX</span></span>

### <span data-ttu-id="9dc86-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9dc86-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> [-Name <String>] [-Body <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dc86-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dc86-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -ParentObject <PSSqlContainerGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dc86-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dc86-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlUserDefinedFunction [-Name <String>] [-Body <String>]
 -InputObject <PSSqlUserDefinedFunctionGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dc86-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9dc86-109">DESCRIPTION</span></span>
<span data-ttu-id="9dc86-110">Обновляет Точки Sql UserDefinedFunction в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="9dc86-110">Updates the CosmosDB Sql UserDefinedFunction.</span></span> <span data-ttu-id="9dc86-111">Выполняет обновление на стороне клиента с помощью существующей userDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="9dc86-111">Performs a client side patch operation by reading the existing UserDefinedFunction.</span></span>

## <span data-ttu-id="9dc86-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9dc86-112">EXAMPLES</span></span>

### <span data-ttu-id="9dc86-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9dc86-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="9dc86-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dc86-114">PARAMETERS</span></span>

### <span data-ttu-id="9dc86-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9dc86-115">-AccountName</span></span>
<span data-ttu-id="9dc86-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="9dc86-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9dc86-117">-Body</span><span class="sxs-lookup"><span data-stu-id="9dc86-117">-Body</span></span>
<span data-ttu-id="9dc86-118">Тело пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="9dc86-118">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="9dc86-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9dc86-119">-Confirm</span></span>
<span data-ttu-id="9dc86-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9dc86-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dc86-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9dc86-121">-ContainerName</span></span>
<span data-ttu-id="9dc86-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="9dc86-122">Container name.</span></span>

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

### <span data-ttu-id="9dc86-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9dc86-123">-DatabaseName</span></span>
<span data-ttu-id="9dc86-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9dc86-124">Database name.</span></span>

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

### <span data-ttu-id="9dc86-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc86-125">-DefaultProfile</span></span>
<span data-ttu-id="9dc86-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9dc86-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dc86-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9dc86-127">-InputObject</span></span>
<span data-ttu-id="9dc86-128">Пользовательский объект функции Sql</span><span class="sxs-lookup"><span data-stu-id="9dc86-128">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="9dc86-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9dc86-129">-Name</span></span>
<span data-ttu-id="9dc86-130">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="9dc86-130">User Defined Function Name.</span></span>

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

### <span data-ttu-id="9dc86-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9dc86-131">-ParentObject</span></span>
<span data-ttu-id="9dc86-132">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="9dc86-132">Sql Container object.</span></span>

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

### <span data-ttu-id="9dc86-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dc86-133">-ResourceGroupName</span></span>
<span data-ttu-id="9dc86-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9dc86-134">Name of resource group.</span></span>

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

### <span data-ttu-id="9dc86-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dc86-135">-WhatIf</span></span>
<span data-ttu-id="9dc86-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dc86-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dc86-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9dc86-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dc86-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc86-138">CommonParameters</span></span>
<span data-ttu-id="9dc86-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dc86-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc86-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dc86-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc86-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9dc86-141">INPUTS</span></span>

### <span data-ttu-id="9dc86-142">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="9dc86-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="9dc86-143">Microsoft.Azure.Commands.GetsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="9dc86-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="9dc86-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9dc86-144">OUTPUTS</span></span>

### <span data-ttu-id="9dc86-145">Microsoft.Azure.Commands.GetsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="9dc86-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="9dc86-146">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="9dc86-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="9dc86-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9dc86-147">NOTES</span></span>

## <span data-ttu-id="9dc86-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9dc86-148">RELATED LINKS</span></span>
