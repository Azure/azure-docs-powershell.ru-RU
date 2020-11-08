---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: bb0d19d7b2ba0d0af9c5686f1ac6d5cf30dbfc7d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078368"
---
# <span data-ttu-id="7e92b-101">New-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="7e92b-101">New-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="7e92b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e92b-102">SYNOPSIS</span></span>
<span data-ttu-id="7e92b-103">Создание новой CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="7e92b-103">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="7e92b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e92b-104">SYNTAX</span></span>

### <span data-ttu-id="7e92b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e92b-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e92b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e92b-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e92b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e92b-107">DESCRIPTION</span></span>
<span data-ttu-id="7e92b-108">Создание новой CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="7e92b-108">Creates a new CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="7e92b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e92b-109">EXAMPLES</span></span>

### <span data-ttu-id="7e92b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7e92b-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlStoredProcedure -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name mySprocrName -Body myBody 
Name     : mySprocName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/storedProcedures/mySprocName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetPropertiesResource
```

## <span data-ttu-id="7e92b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e92b-111">PARAMETERS</span></span>

### <span data-ttu-id="7e92b-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7e92b-112">-AccountName</span></span>
<span data-ttu-id="7e92b-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="7e92b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="7e92b-114">-Body</span><span class="sxs-lookup"><span data-stu-id="7e92b-114">-Body</span></span>
<span data-ttu-id="7e92b-115">Текст хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="7e92b-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="7e92b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e92b-116">-Confirm</span></span>
<span data-ttu-id="7e92b-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e92b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e92b-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="7e92b-118">-ContainerName</span></span>
<span data-ttu-id="7e92b-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="7e92b-119">Container name.</span></span>

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

### <span data-ttu-id="7e92b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7e92b-120">-DatabaseName</span></span>
<span data-ttu-id="7e92b-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e92b-121">Database name.</span></span>

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

### <span data-ttu-id="7e92b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e92b-122">-DefaultProfile</span></span>
<span data-ttu-id="7e92b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e92b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e92b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e92b-124">-Name</span></span>
<span data-ttu-id="7e92b-125">Имя сохраненного Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="7e92b-125">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="7e92b-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7e92b-126">-ParentObject</span></span>
<span data-ttu-id="7e92b-127">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="7e92b-127">Sql Container object.</span></span>

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

### <span data-ttu-id="7e92b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e92b-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e92b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e92b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="7e92b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e92b-130">-WhatIf</span></span>
<span data-ttu-id="7e92b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e92b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e92b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e92b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e92b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e92b-133">CommonParameters</span></span>
<span data-ttu-id="7e92b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e92b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e92b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e92b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e92b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e92b-136">INPUTS</span></span>

### <span data-ttu-id="7e92b-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="7e92b-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="7e92b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e92b-138">OUTPUTS</span></span>

### <span data-ttu-id="7e92b-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="7e92b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

### <span data-ttu-id="7e92b-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="7e92b-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="7e92b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e92b-141">NOTES</span></span>

## <span data-ttu-id="7e92b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e92b-142">RELATED LINKS</span></span>
