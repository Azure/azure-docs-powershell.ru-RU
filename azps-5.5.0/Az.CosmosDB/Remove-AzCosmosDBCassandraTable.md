---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233012"
---
# <span data-ttu-id="a57a9-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="a57a9-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="a57a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a57a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a57a9-103">Удаляет таблицу Климова, которая была удалена из таблицы Климова.</span><span class="sxs-lookup"><span data-stu-id="a57a9-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="a57a9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a57a9-104">SYNTAX</span></span>

### <span data-ttu-id="a57a9-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a57a9-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a57a9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a57a9-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a57a9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a57a9-107">DESCRIPTION</span></span>
<span data-ttu-id="a57a9-108">В **таблице Remove-AzCosmosDBCassandraTable** удаляется таблица Вадима Кузьмина.</span><span class="sxs-lookup"><span data-stu-id="a57a9-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="a57a9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a57a9-109">EXAMPLES</span></span>

### <span data-ttu-id="a57a9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a57a9-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="a57a9-111">Если удаление прошло успешно, cmdlet возвращает объект типа bool(когда -PassThru is passThru), который является истинным.</span><span class="sxs-lookup"><span data-stu-id="a57a9-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="a57a9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a57a9-112">PARAMETERS</span></span>

### <span data-ttu-id="a57a9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a57a9-113">-AccountName</span></span>
<span data-ttu-id="a57a9-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="a57a9-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="a57a9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a57a9-115">-Confirm</span></span>
<span data-ttu-id="a57a9-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a57a9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a57a9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a57a9-117">-DefaultProfile</span></span>
<span data-ttu-id="a57a9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a57a9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a57a9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a57a9-119">-InputObject</span></span>
<span data-ttu-id="a57a9-120">Объект "Таблица", "Александра".</span><span class="sxs-lookup"><span data-stu-id="a57a9-120">Cassandra Table object.</span></span>

```yaml
Type: PSCassandraTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a57a9-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="a57a9-121">-KeyspaceName</span></span>
<span data-ttu-id="a57a9-122">Имя Клавишной области Александры.</span><span class="sxs-lookup"><span data-stu-id="a57a9-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="a57a9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a57a9-123">-Name</span></span>
<span data-ttu-id="a57a9-124">Имя таблицы Александры.</span><span class="sxs-lookup"><span data-stu-id="a57a9-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="a57a9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a57a9-125">-PassThru</span></span>
<span data-ttu-id="a57a9-126">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="a57a9-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="a57a9-127">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="a57a9-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="a57a9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a57a9-128">-ResourceGroupName</span></span>
<span data-ttu-id="a57a9-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a57a9-129">Name of resource group.</span></span>

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

### <span data-ttu-id="a57a9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a57a9-130">-WhatIf</span></span>
<span data-ttu-id="a57a9-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a57a9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a57a9-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a57a9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a57a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a57a9-133">CommonParameters</span></span>
<span data-ttu-id="a57a9-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a57a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a57a9-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a57a9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a57a9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a57a9-136">INPUTS</span></span>

### <span data-ttu-id="a57a9-137">Microsoft.Azure.Commands.GetsDB.Models.PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="a57a9-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="a57a9-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a57a9-138">OUTPUTS</span></span>

### <span data-ttu-id="a57a9-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="a57a9-139">System.Void</span></span>

### <span data-ttu-id="a57a9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a57a9-140">System.Boolean</span></span>

## <span data-ttu-id="a57a9-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a57a9-141">NOTES</span></span>

## <span data-ttu-id="a57a9-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a57a9-142">RELATED LINKS</span></span>
