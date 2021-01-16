---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbsqluserdefinedfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBSqlUserDefinedFunction.md
ms.openlocfilehash: 37da28136e8c0a794e263cff4c2b9f9c0d6ce69f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406311"
---
# <span data-ttu-id="b1b12-101">Remove-AzCosmosDBSqlUserDefinedFunction</span><span class="sxs-lookup"><span data-stu-id="b1b12-101">Remove-AzCosmosDBSqlUserDefinedFunction</span></span>

## <span data-ttu-id="b1b12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b12-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b12-103">Удаление Точки Sql UserDefinedFunction.</span><span class="sxs-lookup"><span data-stu-id="b1b12-103">Deletes the CosmosDB Sql UserDefinedFunction.</span></span>

## <span data-ttu-id="b1b12-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1b12-104">SYNTAX</span></span>

### <span data-ttu-id="b1b12-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b12-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName <String> -AccountName <String>
 -DatabaseName <String> -ContainerName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1b12-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1b12-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBSqlUserDefinedFunction -InputObject <PSSqlUserDefinedFunctionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1b12-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1b12-107">DESCRIPTION</span></span>
<span data-ttu-id="b1b12-108">Для удаления **AzCosmosDBSqlUserDefinedFunction** удаляется Sql UserDefinedFunction, соответствующий заданным названиям ресурсов, AccountName и DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="b1b12-108">The **Remove-AzCosmosDBSqlUserDefinedFunction** cmdlet deletes the CosmosDB Sql UserDefinedFunction corresponding to the given ResourceGroupName, AccountName and DatabaseName.</span></span>

## <span data-ttu-id="b1b12-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1b12-109">EXAMPLES</span></span>

### <span data-ttu-id="b1b12-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1b12-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBSqlUserDefinedFunction -ResourceGroupName {resourceGroupName} -AccountName {accountName} -DatabaseName {databaseName} -ContainerName {containerName} -Name {userDefinedFunctionName}
```

## <span data-ttu-id="b1b12-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1b12-111">PARAMETERS</span></span>

### <span data-ttu-id="b1b12-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b1b12-112">-AccountName</span></span>
<span data-ttu-id="b1b12-113">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="b1b12-113">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b1b12-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1b12-114">-Confirm</span></span>
<span data-ttu-id="b1b12-115">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b12-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1b12-116">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="b1b12-116">-ContainerName</span></span>
<span data-ttu-id="b1b12-117">Имя контейнера.</span><span class="sxs-lookup"><span data-stu-id="b1b12-117">Container name.</span></span>

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

### <span data-ttu-id="b1b12-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1b12-118">-DatabaseName</span></span>
<span data-ttu-id="b1b12-119">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b1b12-119">Database name.</span></span>

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

### <span data-ttu-id="b1b12-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b12-120">-DefaultProfile</span></span>
<span data-ttu-id="b1b12-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b12-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b12-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1b12-122">-InputObject</span></span>
<span data-ttu-id="b1b12-123">Пользовательский объект функции Sql</span><span class="sxs-lookup"><span data-stu-id="b1b12-123">Sql User Defined Function Object</span></span>

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

### <span data-ttu-id="b1b12-124">-Name</span><span class="sxs-lookup"><span data-stu-id="b1b12-124">-Name</span></span>
<span data-ttu-id="b1b12-125">Имя определяемой пользователем функции.</span><span class="sxs-lookup"><span data-stu-id="b1b12-125">User Defined Function Name.</span></span>

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

### <span data-ttu-id="b1b12-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1b12-126">-PassThru</span></span>
<span data-ttu-id="b1b12-127">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="b1b12-127">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b1b12-128">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="b1b12-128">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b1b12-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b12-129">-ResourceGroupName</span></span>
<span data-ttu-id="b1b12-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b1b12-130">Name of resource group.</span></span>

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

### <span data-ttu-id="b1b12-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1b12-131">-WhatIf</span></span>
<span data-ttu-id="b1b12-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1b12-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1b12-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1b12-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1b12-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b12-134">CommonParameters</span></span>
<span data-ttu-id="b1b12-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b12-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b12-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1b12-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b12-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1b12-137">INPUTS</span></span>

### <span data-ttu-id="b1b12-138">Нет</span><span class="sxs-lookup"><span data-stu-id="b1b12-138">None</span></span>

## <span data-ttu-id="b1b12-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1b12-139">OUTPUTS</span></span>

### <span data-ttu-id="b1b12-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="b1b12-140">System.Void</span></span>

### <span data-ttu-id="b1b12-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1b12-141">System.Boolean</span></span>

## <span data-ttu-id="b1b12-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1b12-142">NOTES</span></span>

## <span data-ttu-id="b1b12-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1b12-143">RELATED LINKS</span></span>