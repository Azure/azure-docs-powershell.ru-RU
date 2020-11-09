---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: cc7c443ad4447abfa1c31ebb335d3d1ae602f1b3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314711"
---
# <span data-ttu-id="fda17-101">New-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="fda17-101">New-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="fda17-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fda17-102">SYNOPSIS</span></span>
<span data-ttu-id="fda17-103">Создание нового CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="fda17-103">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="fda17-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fda17-104">SYNTAX</span></span>

### <span data-ttu-id="fda17-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fda17-105">ByNameParameterSet (Default)</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -ContainerName <String> -Name <String> -Body <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fda17-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fda17-106">ByParentObjectParameterSet</span></span>
```
New-AzCosmosDBSqlUserDefinedFunction -Name <String> -Body <String> -ParentObject <PSSqlContainerGetResults>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda17-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fda17-107">DESCRIPTION</span></span>
<span data-ttu-id="fda17-108">Создание нового CosmosDB SQL UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="fda17-108">Creates a new CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="fda17-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fda17-109">EXAMPLES</span></span>

### <span data-ttu-id="fda17-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fda17-110">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUserDefinedFunction -AccountName MyAccountName -ResourceGroupName MyRgName -DatabaseName MyDatabaseName -ContainerName MyContainerName -Name myUDFName -Body myBody 
Name     : myTriggerName
Id       : /subscriptions/mySubId/resourceGroups/MyRgName/providers/Microsoft.DocumentDB/databaseAccounts/MyAccountName/sqlDatabases/MyDatabaseName/contain
           ers/MyContainerName/userDefinedFunctions/myUDFName
Location :
Tags     :
Resource : Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedPropertiesGetPropertiesResource
```

## <span data-ttu-id="fda17-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fda17-111">PARAMETERS</span></span>

### <span data-ttu-id="fda17-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="fda17-112">-AccountName</span></span>
<span data-ttu-id="fda17-113">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="fda17-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fda17-114">-Body</span><span class="sxs-lookup"><span data-stu-id="fda17-114">-Body</span></span>
<span data-ttu-id="fda17-115">Текст пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="fda17-115">The body of the User Defined Function.</span></span>

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

### <span data-ttu-id="fda17-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fda17-116">-Confirm</span></span>
<span data-ttu-id="fda17-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fda17-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda17-118">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="fda17-118">-ContainerName</span></span>
<span data-ttu-id="fda17-119">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="fda17-119">Container name.</span></span>

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

### <span data-ttu-id="fda17-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fda17-120">-DatabaseName</span></span>
<span data-ttu-id="fda17-121">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fda17-121">Database name.</span></span>

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

### <span data-ttu-id="fda17-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda17-122">-DefaultProfile</span></span>
<span data-ttu-id="fda17-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fda17-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fda17-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fda17-124">-Name</span></span>
<span data-ttu-id="fda17-125">Имя пользовательской функции.</span><span class="sxs-lookup"><span data-stu-id="fda17-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="fda17-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fda17-126">-ParentObject</span></span>
<span data-ttu-id="fda17-127">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="fda17-127">Sql Container object.</span></span>

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

### <span data-ttu-id="fda17-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda17-128">-ResourceGroupName</span></span>
<span data-ttu-id="fda17-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fda17-129">Name of resource group.</span></span>

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

### <span data-ttu-id="fda17-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda17-130">-WhatIf</span></span>
<span data-ttu-id="fda17-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fda17-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda17-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fda17-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda17-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda17-133">CommonParameters</span></span>
<span data-ttu-id="fda17-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fda17-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda17-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fda17-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda17-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fda17-136">INPUTS</span></span>

### <span data-ttu-id="fda17-137">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlContainerGetResults</span><span class="sxs-lookup"><span data-stu-id="fda17-137">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlContainerGetResults</span></span>

## <span data-ttu-id="fda17-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fda17-138">OUTPUTS</span></span>

### <span data-ttu-id="fda17-139">Microsoft. Azure. Commands. CosmosDB. Models. PSSqlUserDefinedFunctionGetResults</span><span class="sxs-lookup"><span data-stu-id="fda17-139">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUserDefinedFunctionGetResults</span></span>

### <span data-ttu-id="fda17-140">Microsoft. Azure. Commands. CosmosDB. Exceptions. ConflictingResourceException</span><span class="sxs-lookup"><span data-stu-id="fda17-140">Microsoft.Azure.Commands.CosmosDB.Exceptions.ConflictingResourceException</span></span>

## <span data-ttu-id="fda17-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fda17-141">NOTES</span></span>

## <span data-ttu-id="fda17-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fda17-142">RELATED LINKS</span></span>
