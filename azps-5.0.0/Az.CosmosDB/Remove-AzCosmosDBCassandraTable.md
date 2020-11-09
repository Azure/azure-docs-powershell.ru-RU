---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314675"
---
# <span data-ttu-id="377be-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="377be-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="377be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="377be-102">SYNOPSIS</span></span>
<span data-ttu-id="377be-103">Удаляет таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="377be-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="377be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="377be-104">SYNTAX</span></span>

### <span data-ttu-id="377be-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="377be-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="377be-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="377be-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="377be-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="377be-107">DESCRIPTION</span></span>
<span data-ttu-id="377be-108">Таблица **Remove-AzCosmosDBCassandraTable** удаляет CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="377be-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="377be-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="377be-109">EXAMPLES</span></span>

### <span data-ttu-id="377be-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="377be-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="377be-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="377be-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="377be-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="377be-112">PARAMETERS</span></span>

### <span data-ttu-id="377be-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="377be-113">-AccountName</span></span>
<span data-ttu-id="377be-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="377be-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="377be-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="377be-115">-Confirm</span></span>
<span data-ttu-id="377be-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="377be-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="377be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="377be-117">-DefaultProfile</span></span>
<span data-ttu-id="377be-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="377be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="377be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="377be-119">-InputObject</span></span>
<span data-ttu-id="377be-120">Объект таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="377be-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="377be-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="377be-121">-KeyspaceName</span></span>
<span data-ttu-id="377be-122">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="377be-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="377be-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="377be-123">-Name</span></span>
<span data-ttu-id="377be-124">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="377be-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="377be-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="377be-125">-PassThru</span></span>
<span data-ttu-id="377be-126">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="377be-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="377be-127">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="377be-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="377be-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="377be-128">-ResourceGroupName</span></span>
<span data-ttu-id="377be-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="377be-129">Name of resource group.</span></span>

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

### <span data-ttu-id="377be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="377be-130">-WhatIf</span></span>
<span data-ttu-id="377be-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="377be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="377be-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="377be-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="377be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="377be-133">CommonParameters</span></span>
<span data-ttu-id="377be-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="377be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="377be-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="377be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="377be-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="377be-136">INPUTS</span></span>

### <span data-ttu-id="377be-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="377be-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="377be-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="377be-138">OUTPUTS</span></span>

### <span data-ttu-id="377be-139">System. void</span><span class="sxs-lookup"><span data-stu-id="377be-139">System.Void</span></span>

### <span data-ttu-id="377be-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="377be-140">System.Boolean</span></span>

## <span data-ttu-id="377be-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="377be-141">NOTES</span></span>

## <span data-ttu-id="377be-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="377be-142">RELATED LINKS</span></span>
