---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: b7a709cf7ce9aca894f19229cc2d13d4c30f8744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236834"
---
# <span data-ttu-id="d41dc-101">Update-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="d41dc-101">Update-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="d41dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d41dc-102">SYNOPSIS</span></span>
<span data-ttu-id="d41dc-103">Обновляет CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="d41dc-103">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="d41dc-104">Выполняет операцию исправления на стороне клиента путем чтения существующей хранимой программы.</span><span class="sxs-lookup"><span data-stu-id="d41dc-104">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="d41dc-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d41dc-105">SYNTAX</span></span>

### <span data-ttu-id="d41dc-106">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d41dc-106">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> [-Name <String>] [-Body <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d41dc-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d41dc-107">ByParentObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>] -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d41dc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d41dc-108">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBSqlStoredProcedure [-Name <String>] [-Body <String>]
 -InputObject <PSSqlStoredProcedureGetResults> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d41dc-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d41dc-109">DESCRIPTION</span></span>
<span data-ttu-id="d41dc-110">Обновляет CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="d41dc-110">Updates the CosmosDB Sql StoredProcedure.</span></span> <span data-ttu-id="d41dc-111">Выполняет операцию исправления на стороне клиента путем чтения существующей хранимой программы.</span><span class="sxs-lookup"><span data-stu-id="d41dc-111">Performs a client side patch operation by reading the existing StoredProcedure.</span></span>

## <span data-ttu-id="d41dc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d41dc-112">EXAMPLES</span></span>

### <span data-ttu-id="d41dc-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d41dc-113">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="d41dc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d41dc-114">PARAMETERS</span></span>

### <span data-ttu-id="d41dc-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="d41dc-115">-AccountName</span></span>
<span data-ttu-id="d41dc-116">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="d41dc-116">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="d41dc-117">-Body</span><span class="sxs-lookup"><span data-stu-id="d41dc-117">-Body</span></span>
<span data-ttu-id="d41dc-118">Текст хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="d41dc-118">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="d41dc-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d41dc-119">-Confirm</span></span>
<span data-ttu-id="d41dc-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d41dc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d41dc-121">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d41dc-121">-ContainerName</span></span>
<span data-ttu-id="d41dc-122">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="d41dc-122">Container name.</span></span>

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

### <span data-ttu-id="d41dc-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d41dc-123">-DatabaseName</span></span>
<span data-ttu-id="d41dc-124">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d41dc-124">Database name.</span></span>

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

### <span data-ttu-id="d41dc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41dc-125">-DefaultProfile</span></span>
<span data-ttu-id="d41dc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d41dc-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d41dc-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d41dc-127">-InputObject</span></span>
<span data-ttu-id="d41dc-128">Объект хранимой процедуры SQL</span><span class="sxs-lookup"><span data-stu-id="d41dc-128">Sql Stored Procedure Object</span></span>

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

### <span data-ttu-id="d41dc-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d41dc-129">-Name</span></span>
<span data-ttu-id="d41dc-130">Имя сохраненного Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="d41dc-130">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="d41dc-131">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d41dc-131">-ParentObject</span></span>
<span data-ttu-id="d41dc-132">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="d41dc-132">Sql Container object.</span></span>

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

### <span data-ttu-id="d41dc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d41dc-133">-ResourceGroupName</span></span>
<span data-ttu-id="d41dc-134">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d41dc-134">Name of resource group.</span></span>

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

### <span data-ttu-id="d41dc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d41dc-135">-WhatIf</span></span>
<span data-ttu-id="d41dc-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d41dc-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d41dc-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d41dc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d41dc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41dc-138">CommonParameters</span></span>
<span data-ttu-id="d41dc-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d41dc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41dc-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d41dc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41dc-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d41dc-141">INPUTS</span></span>

### <span data-ttu-id="d41dc-142">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="d41dc-142">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

### <span data-ttu-id="d41dc-143">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d41dc-143">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="d41dc-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d41dc-144">OUTPUTS</span></span>

### <span data-ttu-id="d41dc-145">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="d41dc-145">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="d41dc-146">Microsoft. Azure. Commands. CosmosDB. Exceptions. ResourceNotFoundException</span><span class="sxs-lookup"><span data-stu-id="d41dc-146">Microsoft.Azure.Commands.CosmosDB.Exceptions.ResourceNotFoundException</span></span>

## <span data-ttu-id="d41dc-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="d41dc-147">NOTES</span></span>

## <span data-ttu-id="d41dc-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d41dc-148">RELATED LINKS</span></span>
