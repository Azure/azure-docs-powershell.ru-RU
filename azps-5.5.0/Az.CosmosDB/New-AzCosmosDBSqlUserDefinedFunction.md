---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238506"
---
# <span data-ttu-id="57306-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="57306-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="57306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57306-102">SYNOPSIS</span></span>
<span data-ttu-id="57306-103">Создание нового интерфейса Sql UserDefinedFunction в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="57306-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="57306-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57306-104">SYNTAX</span></span>

### <span data-ttu-id="57306-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57306-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57306-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57306-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57306-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57306-107">DESCRIPTION</span></span>
<span data-ttu-id="57306-108">Создание нового интерфейса Sql UserDefinedFunction в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="57306-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="57306-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57306-109">EXAMPLES</span></span>

### <span data-ttu-id="57306-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57306-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="57306-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57306-111">PARAMETERS</span></span>

### <span data-ttu-id="57306-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="57306-112">-AccountName</span></span>
<span data-ttu-id="57306-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="57306-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="57306-114">-Body</span><span class="sxs-lookup"><span data-stu-id="57306-114">-Body</span></span>
<span data-ttu-id="57306-115">Тело пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="57306-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="57306-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57306-116">-Confirm</span></span>
<span data-ttu-id="57306-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="57306-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57306-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="57306-118">-ContainerName</span></span>
<span data-ttu-id="57306-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="57306-119">Container name.</span></span>

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

### <span data-ttu-id="57306-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="57306-120">-DatabaseName</span></span>
<span data-ttu-id="57306-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="57306-121">Database name.</span></span>

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

### <span data-ttu-id="57306-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57306-122">-DefaultProfile</span></span>
<span data-ttu-id="57306-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57306-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57306-124">-Name</span><span class="sxs-lookup"><span data-stu-id="57306-124">-Name</span></span>
<span data-ttu-id="57306-125">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="57306-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="57306-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="57306-126">-ParentObject</span></span>
<span data-ttu-id="57306-127">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="57306-127">Sql Container object.</span></span>

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

### <span data-ttu-id="57306-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57306-128">-ResourceGroupName</span></span>
<span data-ttu-id="57306-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="57306-129">Name of resource group.</span></span>

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

### <span data-ttu-id="57306-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57306-130">-WhatIf</span></span>
<span data-ttu-id="57306-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57306-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57306-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57306-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57306-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57306-133">CommonParameters</span></span>
<span data-ttu-id="57306-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57306-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57306-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57306-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57306-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57306-136">INPUTS</span></span>

### <span data-ttu-id="57306-137">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="57306-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="57306-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57306-138">OUTPUTS</span></span>

### <span data-ttu-id="57306-139">Microsoft.Azure.Commands.GetsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="57306-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="57306-140">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="57306-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="57306-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57306-141">NOTES</span></span>

## <span data-ttu-id="57306-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57306-142">RELATED LINKS</span></span>
