---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqlstoredprocedure
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlStoredProcedure.md
ms.openlocfilehash: 2914284849fa9a00e3cb2d0b1c96c1efd905e9e2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065021"
---
# <span data-ttu-id="45f7b-101">Set-AzCosmosDBSqlStoredProcedure</span><span class="sxs-lookup"><span data-stu-id="45f7b-101">Set-AzCosmosDBSqlStoredProcedure</span></span>

## <span data-ttu-id="45f7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45f7b-102">SYNOPSIS</span></span>
<span data-ttu-id="45f7b-103">Создает новый или обновляет существующую CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="45f7b-103">Creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="45f7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45f7b-104">SYNTAX</span></span>

### <span data-ttu-id="45f7b-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45f7b-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45f7b-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="45f7b-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlStoredProcedure -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45f7b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45f7b-107">DESCRIPTION</span></span>
<span data-ttu-id="45f7b-108">Командлет **Set-AzCosmosDBSqlStoredProcedure** создает новый или обновляет существующий объект CosmosDB SQL StoredProcedure.</span><span class="sxs-lookup"><span data-stu-id="45f7b-108">The **Set-AzCosmosDBSqlStoredProcedure** cmdlet creates a new or updates an existing CosmosDB Sql StoredProcedure.</span></span>

## <span data-ttu-id="45f7b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45f7b-109">EXAMPLES</span></span>

### <span data-ttu-id="45f7b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45f7b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlStoredProcedure -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {storedProcedureName} -ContainerName {containerName} -Body {sampleBody}

Name                           : {storedProcedureName}
Id                             : {storedProcedureId}
SqlStoredProcedureGetResultsId :
Body                           :
_rid                           :
_ts                            :
_etag                          :
```

## <span data-ttu-id="45f7b-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45f7b-111">PARAMETERS</span></span>

### <span data-ttu-id="45f7b-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="45f7b-112">-AccountName</span></span>
<span data-ttu-id="45f7b-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="45f7b-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="45f7b-114">-Body</span><span class="sxs-lookup"><span data-stu-id="45f7b-114">-Body</span></span>
<span data-ttu-id="45f7b-115">Текст хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="45f7b-115">The body of the Stored Procedure.</span></span>

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

### <span data-ttu-id="45f7b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45f7b-116">-Confirm</span></span>
<span data-ttu-id="45f7b-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45f7b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45f7b-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="45f7b-118">-ContainerName</span></span>
<span data-ttu-id="45f7b-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="45f7b-119">Container name.</span></span>

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

### <span data-ttu-id="45f7b-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45f7b-120">-DatabaseName</span></span>
<span data-ttu-id="45f7b-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="45f7b-121">Database name.</span></span>

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

### <span data-ttu-id="45f7b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45f7b-122">-DefaultProfile</span></span>
<span data-ttu-id="45f7b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45f7b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45f7b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45f7b-124">-InputObject</span></span>
<span data-ttu-id="45f7b-125">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="45f7b-125">Sql Container object.</span></span>

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

### <span data-ttu-id="45f7b-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45f7b-126">-Name</span></span>
<span data-ttu-id="45f7b-127">Имя сохраненного Prcodecure.</span><span class="sxs-lookup"><span data-stu-id="45f7b-127">Stored Prcodecure Name.</span></span>

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

### <span data-ttu-id="45f7b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45f7b-128">-ResourceGroupName</span></span>
<span data-ttu-id="45f7b-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45f7b-129">Name of resource group.</span></span>

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

### <span data-ttu-id="45f7b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45f7b-130">-WhatIf</span></span>
<span data-ttu-id="45f7b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45f7b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45f7b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45f7b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45f7b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45f7b-133">CommonParameters</span></span>
<span data-ttu-id="45f7b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45f7b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45f7b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45f7b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45f7b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45f7b-136">INPUTS</span></span>

### <span data-ttu-id="45f7b-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="45f7b-137">None</span></span>

## <span data-ttu-id="45f7b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45f7b-138">OUTPUTS</span></span>

### <span data-ttu-id="45f7b-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlStoredProcedureGetResults</span><span class="sxs-lookup"><span data-stu-id="45f7b-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlStoredProcedureGetResults</span></span>

## <span data-ttu-id="45f7b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="45f7b-140">NOTES</span></span>

## <span data-ttu-id="45f7b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45f7b-141">RELATED LINKS</span></span>
