---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397567"
---
# <span data-ttu-id="333c0-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="333c0-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="333c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="333c0-102">SYNOPSIS</span></span>
<span data-ttu-id="333c0-103">Создает новый интерфейс Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="333c0-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="333c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="333c0-104">SYNTAX</span></span>

### <span data-ttu-id="333c0-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="333c0-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333c0-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="333c0-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333c0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="333c0-107">DESCRIPTION</span></span>
<span data-ttu-id="333c0-108">Создает новый интерфейс Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="333c0-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="333c0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="333c0-109">EXAMPLES</span></span>

### <span data-ttu-id="333c0-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="333c0-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="333c0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="333c0-111">PARAMETERS</span></span>

### <span data-ttu-id="333c0-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="333c0-112">-AccountName</span></span>
<span data-ttu-id="333c0-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="333c0-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="333c0-114">-Body</span><span class="sxs-lookup"><span data-stu-id="333c0-114">-Body</span></span>
<span data-ttu-id="333c0-115">Тело пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="333c0-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="333c0-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="333c0-116">-Confirm</span></span>
<span data-ttu-id="333c0-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="333c0-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333c0-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="333c0-118">-ContainerName</span></span>
<span data-ttu-id="333c0-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="333c0-119">Container name.</span></span>

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

### <span data-ttu-id="333c0-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="333c0-120">-DatabaseName</span></span>
<span data-ttu-id="333c0-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="333c0-121">Database name.</span></span>

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

### <span data-ttu-id="333c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333c0-122">-DefaultProfile</span></span>
<span data-ttu-id="333c0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="333c0-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333c0-124">-Name</span><span class="sxs-lookup"><span data-stu-id="333c0-124">-Name</span></span>
<span data-ttu-id="333c0-125">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="333c0-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="333c0-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="333c0-126">-ParentObject</span></span>
<span data-ttu-id="333c0-127">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="333c0-127">Sql Container object.</span></span>

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

### <span data-ttu-id="333c0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333c0-128">-ResourceGroupName</span></span>
<span data-ttu-id="333c0-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="333c0-129">Name of resource group.</span></span>

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

### <span data-ttu-id="333c0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333c0-130">-WhatIf</span></span>
<span data-ttu-id="333c0-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="333c0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333c0-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="333c0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333c0-133">CommonParameters</span></span>
<span data-ttu-id="333c0-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333c0-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="333c0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333c0-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="333c0-136">INPUTS</span></span>

### <span data-ttu-id="333c0-137">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="333c0-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="333c0-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="333c0-138">OUTPUTS</span></span>

### <span data-ttu-id="333c0-139">Microsoft.Azure.Commands.GetsDB.Models.PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="333c0-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="333c0-140">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="333c0-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="333c0-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="333c0-141">NOTES</span></span>

## <span data-ttu-id="333c0-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="333c0-142">RELATED LINKS</span></span>
