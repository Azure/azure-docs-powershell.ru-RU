---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508785"
---
# <span data-ttu-id="6afcf-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="6afcf-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="6afcf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afcf-102">SYNOPSIS</span></span>
<span data-ttu-id="6afcf-103">Создается новая модель Sql StoredProcedure, создав ее.</span><span class="sxs-lookup"><span data-stu-id="6afcf-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="6afcf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6afcf-104">SYNTAX</span></span>

### <span data-ttu-id="6afcf-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6afcf-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6afcf-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6afcf-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6afcf-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6afcf-107">DESCRIPTION</span></span>
<span data-ttu-id="6afcf-108">Создается новая модель Sql StoredProcedure, создав ее.</span><span class="sxs-lookup"><span data-stu-id="6afcf-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="6afcf-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6afcf-109">EXAMPLES</span></span>

### <span data-ttu-id="6afcf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6afcf-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="6afcf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6afcf-111">PARAMETERS</span></span>

### <span data-ttu-id="6afcf-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6afcf-112">-AccountName</span></span>
<span data-ttu-id="6afcf-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="6afcf-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="6afcf-114">-Body</span><span class="sxs-lookup"><span data-stu-id="6afcf-114">-Body</span></span>
<span data-ttu-id="6afcf-115">Тело хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="6afcf-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="6afcf-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6afcf-116">-Confirm</span></span>
<span data-ttu-id="6afcf-117">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6afcf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6afcf-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="6afcf-118">-ContainerName</span></span>
<span data-ttu-id="6afcf-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="6afcf-119">Container name.</span></span>

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

### <span data-ttu-id="6afcf-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6afcf-120">-DatabaseName</span></span>
<span data-ttu-id="6afcf-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6afcf-121">Database name.</span></span>

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

### <span data-ttu-id="6afcf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afcf-122">-DefaultProfile</span></span>
<span data-ttu-id="6afcf-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6afcf-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6afcf-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6afcf-124">-Name</span></span>
<span data-ttu-id="6afcf-125">Имя хранимой prcodecure.</span><span class="sxs-lookup"><span data-stu-id="6afcf-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="6afcf-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6afcf-126">-ParentObject</span></span>
<span data-ttu-id="6afcf-127">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="6afcf-127">Sql Container object.</span></span>

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

### <span data-ttu-id="6afcf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6afcf-128">-ResourceGroupName</span></span>
<span data-ttu-id="6afcf-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6afcf-129">Name of resource group.</span></span>

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

### <span data-ttu-id="6afcf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6afcf-130">-WhatIf</span></span>
<span data-ttu-id="6afcf-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6afcf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6afcf-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6afcf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6afcf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afcf-133">CommonParameters</span></span>
<span data-ttu-id="6afcf-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afcf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afcf-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6afcf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afcf-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6afcf-136">INPUTS</span></span>

### <span data-ttu-id="6afcf-137">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="6afcf-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="6afcf-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6afcf-138">OUTPUTS</span></span>

### <span data-ttu-id="6afcf-139">Microsoft.Azure.Commands.GetsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="6afcf-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="6afcf-140">Microsoft.Azure.Commands.НицаDB.Exceptions.ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="6afcf-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="6afcf-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6afcf-141">NOTES</span></span>

## <span data-ttu-id="6afcf-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6afcf-142">RELATED LINKS</span></span>
