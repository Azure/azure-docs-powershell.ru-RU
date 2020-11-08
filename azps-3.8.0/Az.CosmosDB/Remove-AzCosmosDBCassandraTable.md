---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbcassandratable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBCassandraTable.md
ms.openlocfilehash: 7e176ebe2185f2a8c049155e04197b333fabd83c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073714"
---
# <span data-ttu-id="bbe78-101">Remove-AzCosmosDBCassandraTable</span><span class="sxs-lookup"><span data-stu-id="bbe78-101">Remove-AzCosmosDBCassandraTable</span></span>

## <span data-ttu-id="bbe78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bbe78-102">SYNOPSIS</span></span>
<span data-ttu-id="bbe78-103">Удаляет таблицу CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bbe78-103">Deletes a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="bbe78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bbe78-104">SYNTAX</span></span>

### <span data-ttu-id="bbe78-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bbe78-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBCassandraTable -ResourceGroupName <String> -AccountName <String> -KeyspaceName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbe78-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbe78-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBCassandraTable -InputObject <PSCassandraTableGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbe78-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe78-107">DESCRIPTION</span></span>
<span data-ttu-id="bbe78-108">Таблица **Remove-AzCosmosDBCassandraTable** удаляет CosmosDB Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bbe78-108">The **Remove-AzCosmosDBCassandraTable** delete a CosmosDB Cassandra Table.</span></span>

## <span data-ttu-id="bbe78-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bbe78-109">EXAMPLES</span></span>

### <span data-ttu-id="bbe78-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bbe78-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBCassandraTable -ResourceGroupName {resourceGroup} -AccountName {account} -KeyspaceName {keyspace} -Name {tableName}
```

<span data-ttu-id="bbe78-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="bbe78-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="bbe78-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bbe78-112">PARAMETERS</span></span>

### <span data-ttu-id="bbe78-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="bbe78-113">-AccountName</span></span>
<span data-ttu-id="bbe78-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="bbe78-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="bbe78-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbe78-115">-Confirm</span></span>
<span data-ttu-id="bbe78-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bbe78-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbe78-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbe78-117">-DefaultProfile</span></span>
<span data-ttu-id="bbe78-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bbe78-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbe78-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbe78-119">-InputObject</span></span>
<span data-ttu-id="bbe78-120">Объект таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bbe78-120">Cassandra Table object.</span></span>

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

### <span data-ttu-id="bbe78-121">-KeyspaceName</span><span class="sxs-lookup"><span data-stu-id="bbe78-121">-KeyspaceName</span></span>
<span data-ttu-id="bbe78-122">Cassandra keyspace имя.</span><span class="sxs-lookup"><span data-stu-id="bbe78-122">Cassandra Keyspace Name.</span></span>

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

### <span data-ttu-id="bbe78-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bbe78-123">-Name</span></span>
<span data-ttu-id="bbe78-124">Имя таблицы Cassandra.</span><span class="sxs-lookup"><span data-stu-id="bbe78-124">Cassandra Table Name.</span></span>

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

### <span data-ttu-id="bbe78-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbe78-125">-PassThru</span></span>
<span data-ttu-id="bbe78-126">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="bbe78-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="bbe78-127">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="bbe78-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="bbe78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbe78-128">-ResourceGroupName</span></span>
<span data-ttu-id="bbe78-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bbe78-129">Name of resource group.</span></span>

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

### <span data-ttu-id="bbe78-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbe78-130">-WhatIf</span></span>
<span data-ttu-id="bbe78-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bbe78-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbe78-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bbe78-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbe78-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbe78-133">CommonParameters</span></span>
<span data-ttu-id="bbe78-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bbe78-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbe78-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bbe78-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbe78-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bbe78-136">INPUTS</span></span>

### <span data-ttu-id="bbe78-137">Microsoft. Azure. Commands. CosmosDB. Models. PSCassandraTableGetResults</span><span class="sxs-lookup"><span data-stu-id="bbe78-137">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraTableGetResults</span></span>

## <span data-ttu-id="bbe78-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bbe78-138">OUTPUTS</span></span>

### <span data-ttu-id="bbe78-139">System. void</span><span class="sxs-lookup"><span data-stu-id="bbe78-139">System.Void</span></span>

### <span data-ttu-id="bbe78-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bbe78-140">System.Boolean</span></span>

## <span data-ttu-id="bbe78-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="bbe78-141">NOTES</span></span>

## <span data-ttu-id="bbe78-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bbe78-142">RELATED LINKS</span></span>
