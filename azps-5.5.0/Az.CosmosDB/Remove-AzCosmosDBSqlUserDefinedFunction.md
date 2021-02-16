---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238443"
---
# <span data-ttu-id="2dc9c-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="2dc9c-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="2dc9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dc9c-102">SYNOPSIS</span></span>
<span data-ttu-id="2dc9c-103">Удаление Точки Sql UserDefinedFunction в SqlDb.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="2dc9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2dc9c-104">SYNTAX</span></span>

### <span data-ttu-id="2dc9c-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dc9c-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dc9c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2dc9c-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dc9c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dc9c-107">DESCRIPTION</span></span>
<span data-ttu-id="2dc9c-108">Для удаления **AzCosmosDBSqlUserDefinedFunction** удаляется Sql UserDefinedFunction, соответствующий заданным названиям ресурсов, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="2dc9c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2dc9c-109">EXAMPLES</span></span>

### <span data-ttu-id="2dc9c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2dc9c-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="2dc9c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dc9c-111">PARAMETERS</span></span>

### <span data-ttu-id="2dc9c-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2dc9c-112">-AccountName</span></span>
<span data-ttu-id="2dc9c-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="2dc9c-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="2dc9c-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dc9c-114">-Confirm</span></span>
<span data-ttu-id="2dc9c-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dc9c-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2dc9c-116">-ContainerName</span></span>
<span data-ttu-id="2dc9c-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-117">Container name.</span></span>

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

### <span data-ttu-id="2dc9c-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2dc9c-118">-DatabaseName</span></span>
<span data-ttu-id="2dc9c-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-119">Database name.</span></span>

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

### <span data-ttu-id="2dc9c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dc9c-120">-DefaultProfile</span></span>
<span data-ttu-id="2dc9c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dc9c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dc9c-122">-InputObject</span></span>
<span data-ttu-id="2dc9c-123">Пользовательский объект функции Sql</span><span class="sxs-lookup"><span data-stu-id="2dc9c-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="2dc9c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2dc9c-124">-Name</span></span>
<span data-ttu-id="2dc9c-125">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="2dc9c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2dc9c-126">-PassThru</span></span>
<span data-ttu-id="2dc9c-127">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="2dc9c-128">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="2dc9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dc9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="2dc9c-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-130">Name of resource group.</span></span>

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

### <span data-ttu-id="2dc9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dc9c-131">-WhatIf</span></span>
<span data-ttu-id="2dc9c-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dc9c-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dc9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dc9c-134">CommonParameters</span></span>
<span data-ttu-id="2dc9c-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dc9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dc9c-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dc9c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dc9c-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2dc9c-137">INPUTS</span></span>

### <span data-ttu-id="2dc9c-138">Нет</span><span class="sxs-lookup"><span data-stu-id="2dc9c-138">None</span></span>

## <span data-ttu-id="2dc9c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2dc9c-139">OUTPUTS</span></span>

### <span data-ttu-id="2dc9c-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="2dc9c-140">System.Void</span></span>

### <span data-ttu-id="2dc9c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2dc9c-141">System.Boolean</span></span>

## <span data-ttu-id="2dc9c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2dc9c-142">NOTES</span></span>

## <span data-ttu-id="2dc9c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dc9c-143">RELATED LINKS</span></span>
