---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233004"
---
# <span data-ttu-id="619af-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="619af-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="619af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="619af-102">SYNOPSIS</span></span>
<span data-ttu-id="619af-103">Удаление базы данных "ГрадсDB Гремлин".</span><span class="sxs-lookup"><span data-stu-id="619af-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="619af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="619af-104">SYNTAX</span></span>

### <span data-ttu-id="619af-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="619af-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="619af-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="619af-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="619af-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="619af-107">DESCRIPTION</span></span>
<span data-ttu-id="619af-108">Для **удаления базы данных AzCosmosDBGremlinDatabase** удаляется база данных AzsDB Гремлин.</span><span class="sxs-lookup"><span data-stu-id="619af-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="619af-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="619af-109">EXAMPLES</span></span>

### <span data-ttu-id="619af-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="619af-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="619af-111">Если удаление прошло успешно, cmdlet возвращает объект типа bool(когда -PassThru is passThru), который является истинным.</span><span class="sxs-lookup"><span data-stu-id="619af-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="619af-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="619af-112">PARAMETERS</span></span>

### <span data-ttu-id="619af-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="619af-113">-AccountName</span></span>
<span data-ttu-id="619af-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="619af-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="619af-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="619af-115">-Confirm</span></span>
<span data-ttu-id="619af-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="619af-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="619af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619af-117">-DefaultProfile</span></span>
<span data-ttu-id="619af-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="619af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="619af-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="619af-119">-InputObject</span></span>
<span data-ttu-id="619af-120">Объект базы данных Гремлин.</span><span class="sxs-lookup"><span data-stu-id="619af-120">Gremlin Database object.</span></span>

```yaml
Type: PSGremlinDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="619af-121">-Name</span><span class="sxs-lookup"><span data-stu-id="619af-121">-Name</span></span>
<span data-ttu-id="619af-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="619af-122">Database name.</span></span>

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

### <span data-ttu-id="619af-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="619af-123">-PassThru</span></span>
<span data-ttu-id="619af-124">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="619af-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="619af-125">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="619af-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="619af-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="619af-126">-ResourceGroupName</span></span>
<span data-ttu-id="619af-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="619af-127">Name of resource group.</span></span>

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

### <span data-ttu-id="619af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="619af-128">-WhatIf</span></span>
<span data-ttu-id="619af-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="619af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="619af-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="619af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="619af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619af-131">CommonParameters</span></span>
<span data-ttu-id="619af-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="619af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619af-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="619af-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619af-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="619af-134">INPUTS</span></span>

### <span data-ttu-id="619af-135">Microsoft.Azure.Commands.GetsDB.Models.PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="619af-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="619af-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="619af-136">OUTPUTS</span></span>

### <span data-ttu-id="619af-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="619af-137">System.Void</span></span>

### <span data-ttu-id="619af-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="619af-138">System.Boolean</span></span>

## <span data-ttu-id="619af-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="619af-139">NOTES</span></span>

## <span data-ttu-id="619af-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="619af-140">RELATED LINKS</span></span>
