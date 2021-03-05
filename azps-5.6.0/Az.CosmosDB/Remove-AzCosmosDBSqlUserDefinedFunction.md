---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 7e7ffd7c06217b4e2d12aaf75684c85f8ab12e9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983256"
---
# <span data-ttu-id="f7d18-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="f7d18-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="f7d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d18-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d18-103">Удаление Точки Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="f7d18-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="f7d18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7d18-104">SYNTAX</span></span>

### <span data-ttu-id="f7d18-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7d18-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d18-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7d18-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d18-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7d18-107">DESCRIPTION</span></span>
<span data-ttu-id="f7d18-108">Для удаления **AzCosmosDBSqlUserDefinedFunction** удаляется Sql UserDefinedFunction, соответствующий заданным названиям ресурсов, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f7d18-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="f7d18-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7d18-109">EXAMPLES</span></span>

### <span data-ttu-id="f7d18-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7d18-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="f7d18-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7d18-111">PARAMETERS</span></span>

### <span data-ttu-id="f7d18-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f7d18-112">-AccountName</span></span>
<span data-ttu-id="f7d18-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="f7d18-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="f7d18-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d18-114">-Confirm</span></span>
<span data-ttu-id="f7d18-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d18-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d18-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="f7d18-116">-ContainerName</span></span>
<span data-ttu-id="f7d18-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="f7d18-117">Container name.</span></span>

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

### <span data-ttu-id="f7d18-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f7d18-118">-DatabaseName</span></span>
<span data-ttu-id="f7d18-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="f7d18-119">Database name.</span></span>

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

### <span data-ttu-id="f7d18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d18-120">-DefaultProfile</span></span>
<span data-ttu-id="f7d18-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7d18-122">-InputObject</span></span>
<span data-ttu-id="f7d18-123">Пользовательский объект функции Sql</span><span class="sxs-lookup"><span data-stu-id="f7d18-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="f7d18-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d18-124">-Name</span></span>
<span data-ttu-id="f7d18-125">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="f7d18-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="f7d18-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7d18-126">-PassThru</span></span>
<span data-ttu-id="f7d18-127">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="f7d18-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="f7d18-128">Результат является истинным, если операция прошла успешно и если она не произошла, вы ошибку.</span><span class="sxs-lookup"><span data-stu-id="f7d18-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d18-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d18-129">-ResourceGroupName</span></span>
<span data-ttu-id="f7d18-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7d18-130">Name of resource group.</span></span>

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

### <span data-ttu-id="f7d18-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d18-131">-WhatIf</span></span>
<span data-ttu-id="f7d18-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d18-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7d18-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f7d18-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d18-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d18-134">CommonParameters</span></span>
<span data-ttu-id="f7d18-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d18-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d18-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7d18-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d18-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d18-137">INPUTS</span></span>

### <span data-ttu-id="f7d18-138">Нет</span><span class="sxs-lookup"><span data-stu-id="f7d18-138">None</span></span>

## <span data-ttu-id="f7d18-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d18-139">OUTPUTS</span></span>

### <span data-ttu-id="f7d18-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="f7d18-140">System.Void</span></span>

### <span data-ttu-id="f7d18-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7d18-141">System.Boolean</span></span>

## <span data-ttu-id="f7d18-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7d18-142">NOTES</span></span>

## <span data-ttu-id="f7d18-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7d18-143">RELATED LINKS</span></span>
