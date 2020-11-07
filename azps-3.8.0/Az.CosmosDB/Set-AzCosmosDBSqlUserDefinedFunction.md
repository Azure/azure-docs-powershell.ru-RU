---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/set-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Set-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 27363873996505a15e8eccd3dcb3620a2f88c1a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911799"
---
# <span data-ttu-id="59e9a-101">Set-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="59e9a-101">Set-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="59e9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="59e9a-103">Создает новый или обновляет существующий CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="59e9a-103">Creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="59e9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59e9a-104">SYNTAX</span></span>

### <span data-ttu-id="59e9a-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59e9a-105">ByNameParameterSet (Default)</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59e9a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59e9a-106">ByParentObjectParameterSet</span></span>
```
Set-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -InputObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59e9a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59e9a-107">DESCRIPTION</span></span>
<span data-ttu-id="59e9a-108">Командлет **Set-AzCosmosDBSqlUserDefinedFunction** создает новый или обновляет существующий CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="59e9a-108">The **Set-AzCosmosDBSqlUserDefinedFunction** cmdlet creates a new or updates an existing CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="59e9a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59e9a-109">EXAMPLES</span></span>

### <span data-ttu-id="59e9a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="59e9a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCosmosDBSqlUserDefinedFunction -AccountName {accountName} -ResourceGroupName {resourceGroupName} -DatabaseName {databaseName} -Name {udfName} -ContainerName {containerName} -Body {sampleBody}

Name                               : {udfName}
Id                                 : {udfId}
SqlUserDefinedFunctionGetResultsId :
Body                               :
_rid                               :
_ts                                :
_etag                              :
```

## <span data-ttu-id="59e9a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59e9a-111">PARAMETERS</span></span>

### <span data-ttu-id="59e9a-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="59e9a-112">-AccountName</span></span>
<span data-ttu-id="59e9a-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="59e9a-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="59e9a-114">-Body</span><span class="sxs-lookup"><span data-stu-id="59e9a-114">-Body</span></span>
<span data-ttu-id="59e9a-115">Текст пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="59e9a-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="59e9a-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59e9a-116">-Confirm</span></span>
<span data-ttu-id="59e9a-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="59e9a-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59e9a-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="59e9a-118">-ContainerName</span></span>
<span data-ttu-id="59e9a-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="59e9a-119">Container name.</span></span>

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

### <span data-ttu-id="59e9a-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59e9a-120">-DatabaseName</span></span>
<span data-ttu-id="59e9a-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="59e9a-121">Database name.</span></span>

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

### <span data-ttu-id="59e9a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e9a-122">-DefaultProfile</span></span>
<span data-ttu-id="59e9a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59e9a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59e9a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59e9a-124">-InputObject</span></span>
<span data-ttu-id="59e9a-125">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="59e9a-125">Sql Container object.</span></span>

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

### <span data-ttu-id="59e9a-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59e9a-126">-Name</span></span>
<span data-ttu-id="59e9a-127">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="59e9a-127">User Defined Function Name.</span></span>

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

### <span data-ttu-id="59e9a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e9a-128">-ResourceGroupName</span></span>
<span data-ttu-id="59e9a-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59e9a-129">Name of resource group.</span></span>

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

### <span data-ttu-id="59e9a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59e9a-130">-WhatIf</span></span>
<span data-ttu-id="59e9a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="59e9a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59e9a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="59e9a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59e9a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e9a-133">CommonParameters</span></span>
<span data-ttu-id="59e9a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59e9a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e9a-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="59e9a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e9a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59e9a-136">INPUTS</span></span>

### <span data-ttu-id="59e9a-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="59e9a-137">None</span></span>

## <span data-ttu-id="59e9a-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59e9a-138">OUTPUTS</span></span>

### <span data-ttu-id="59e9a-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="59e9a-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

## <span data-ttu-id="59e9a-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="59e9a-140">NOTES</span></span>

## <span data-ttu-id="59e9a-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59e9a-141">RELATED LINKS</span></span>
