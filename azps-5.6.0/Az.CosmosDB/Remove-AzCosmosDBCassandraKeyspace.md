---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/remove-azcosmosdbcassandrakeyspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraKeyspace.md
ms.openlocfilehash: 849f716787c01c5810af74c37e97bbdb0bd2ef13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954755"
---
# <span data-ttu-id="373a2-101">Remove-AzCosmosDBCassandraKeyspace</span><span class="sxs-lookup"><span data-stu-id="373a2-101">Remove-AzCosmosDBCassandraKeyspace</span></span>

## <span data-ttu-id="373a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="373a2-102">SYNOPSIS</span></span>
<span data-ttu-id="373a2-103">Удаление Ключа Климова Вадима Вадимова.</span><span class="sxs-lookup"><span data-stu-id="373a2-103">Deletes a CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="373a2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="373a2-104">SYNTAX</span></span>

### <span data-ttu-id="373a2-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="373a2-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="373a2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="373a2-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraKeyspace -InputObject <PSCassandraKeyspaceGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="373a2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="373a2-107">DESCRIPTION</span></span>
<span data-ttu-id="373a2-108">С **его учетной** записью будет удалена существующая клавишная область Вадима Ильиной.</span><span class="sxs-lookup"><span data-stu-id="373a2-108">The **Remove-AzCosmosDBCassandraKeyspace** cmdlet deletes an existing CosmosDB Cassandra Keyspace.</span></span>

## <span data-ttu-id="373a2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="373a2-109">EXAMPLES</span></span>

### <span data-ttu-id="373a2-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="373a2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraKeyspace -ResourceGroupName {resourceGroupName} -AccountName {accountName} -Name {keyspaceName}
```

<span data-ttu-id="373a2-111">В случае успешного удаления cmdlet возвращает объект типа bool(когда -PassThru is passThru), который является истинным.</span><span class="sxs-lookup"><span data-stu-id="373a2-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true if the delete was successful.</span></span>

## <span data-ttu-id="373a2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="373a2-112">PARAMETERS</span></span>

### <span data-ttu-id="373a2-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="373a2-113">-AccountName</span></span>
<span data-ttu-id="373a2-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="373a2-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="373a2-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="373a2-115">-Confirm</span></span>
<span data-ttu-id="373a2-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="373a2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373a2-117">-DefaultProfile</span></span>
<span data-ttu-id="373a2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="373a2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373a2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373a2-119">-InputObject</span></span>
<span data-ttu-id="373a2-120">Объект "Клавишная область" Вадима.</span><span class="sxs-lookup"><span data-stu-id="373a2-120">Cassandra Keyspace object.</span></span>

```yaml
Type: PSCassandraKeyspaceGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="373a2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="373a2-121">-Name</span></span>
<span data-ttu-id="373a2-122">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="373a2-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="373a2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="373a2-123">-PassThru</span></span>
<span data-ttu-id="373a2-124">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="373a2-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="373a2-125">Результат является истинным, если операция прошла успешно и если она не произошла, вы ошибку.</span><span class="sxs-lookup"><span data-stu-id="373a2-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="373a2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373a2-126">-ResourceGroupName</span></span>
<span data-ttu-id="373a2-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="373a2-127">Name of resource group.</span></span>

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

### <span data-ttu-id="373a2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373a2-128">-WhatIf</span></span>
<span data-ttu-id="373a2-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="373a2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="373a2-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="373a2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="373a2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373a2-131">CommonParameters</span></span>
<span data-ttu-id="373a2-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="373a2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373a2-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="373a2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373a2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="373a2-134">INPUTS</span></span>

### <span data-ttu-id="373a2-135">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraKeyspaceGetResults</span><span class="sxs-lookup"><span data-stu-id="373a2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraKeyspaceGetResults</span></span>

## <span data-ttu-id="373a2-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="373a2-136">OUTPUTS</span></span>

### <span data-ttu-id="373a2-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="373a2-137">System.Void</span></span>

### <span data-ttu-id="373a2-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="373a2-138">System.Boolean</span></span>

## <span data-ttu-id="373a2-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="373a2-139">NOTES</span></span>

## <span data-ttu-id="373a2-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="373a2-140">RELATED LINKS</span></span>
