---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418159"
---
# <span data-ttu-id="f4b36-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="f4b36-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="f4b36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4b36-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b36-103">Обновляет Sql StoredProcedure вбокDb.</span><span class="sxs-lookup"><span data-stu-id="f4b36-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="f4b36-104">Выполняет обновление на стороне клиента, считыв существующее исправление StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="f4b36-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="f4b36-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f4b36-105">SYNTAX</span></span>

### <span data-ttu-id="f4b36-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f4b36-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b36-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b36-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4b36-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f4b36-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4b36-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b36-109">DESCRIPTION</span></span>
<span data-ttu-id="f4b36-110">Обновляет Sql StoredProcedure вНося изменения вБОКDB.</span><span class="sxs-lookup"><span data-stu-id="f4b36-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="f4b36-111">Выполняет обновление на стороне клиента, считыв существующее исправление StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="f4b36-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="f4b36-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f4b36-112">EXAMPLES</span></span>

### <span data-ttu-id="f4b36-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f4b36-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="f4b36-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4b36-114">PARAMETERS</span></span>

### <span data-ttu-id="f4b36-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f4b36-115">-AccountName</span></span>
<span data-ttu-id="f4b36-116">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="f4b36-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f4b36-117">-Body</span><span class="sxs-lookup"><span data-stu-id="f4b36-117">-Body</span></span>
<span data-ttu-id="f4b36-118">Тело хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="f4b36-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="f4b36-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4b36-119">-Confirm</span></span>
<span data-ttu-id="f4b36-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b36-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b36-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f4b36-121">-ContainerName</span></span>
<span data-ttu-id="f4b36-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="f4b36-122">Container name.</span></span>

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

### <span data-ttu-id="f4b36-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f4b36-123">-DatabaseName</span></span>
<span data-ttu-id="f4b36-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f4b36-124">Database name.</span></span>

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

### <span data-ttu-id="f4b36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b36-125">-DefaultProfile</span></span>
<span data-ttu-id="f4b36-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b36-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4b36-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4b36-127">-InputObject</span></span>
<span data-ttu-id="f4b36-128">Объект хранимой процедуры Sql</span><span class="sxs-lookup"><span data-stu-id="f4b36-128">Sql Stored Procedure Object</span></span>

```yaml
Type: PSSqlStoredProcedureGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4b36-129">-Name</span><span class="sxs-lookup"><span data-stu-id="f4b36-129">-Name</span></span>
<span data-ttu-id="f4b36-130">Имя хранимой prcodecure.</span><span class="sxs-lookup"><span data-stu-id="f4b36-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="f4b36-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f4b36-131">-ParentObject</span></span>
<span data-ttu-id="f4b36-132">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="f4b36-132">Sql Container object.</span></span>

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

### <span data-ttu-id="f4b36-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4b36-133">-ResourceGroupName</span></span>
<span data-ttu-id="f4b36-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f4b36-134">Name of resource group.</span></span>

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

### <span data-ttu-id="f4b36-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b36-135">-WhatIf</span></span>
<span data-ttu-id="f4b36-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4b36-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4b36-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f4b36-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b36-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b36-138">CommonParameters</span></span>
<span data-ttu-id="f4b36-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4b36-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b36-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4b36-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b36-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4b36-141">INPUTS</span></span>

### <span data-ttu-id="f4b36-142">Microsoft.Azure.Commands.GetsDB.Models.PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="f4b36-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="f4b36-143">Microsoft.Azure.Commands.GetsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="f4b36-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="f4b36-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f4b36-144">OUTPUTS</span></span>

### <span data-ttu-id="f4b36-145">Microsoft.Azure.Commands.GetsDB.Models.PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="f4b36-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="f4b36-146">Microsoft.Azure.Commands.НицаDB.Exceptions.ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="f4b36-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="f4b36-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f4b36-147">NOTES</span></span>

## <span data-ttu-id="f4b36-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4b36-148">RELATED LINKS</span></span>
