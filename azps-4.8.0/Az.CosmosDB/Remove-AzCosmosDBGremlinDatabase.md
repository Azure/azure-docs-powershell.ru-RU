---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079734"
---
# <span data-ttu-id="5a37f-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="5a37f-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="5a37f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a37f-102">SYNOPSIS</span></span>
<span data-ttu-id="5a37f-103">Удаляет базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5a37f-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5a37f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a37f-104">SYNTAX</span></span>

### <span data-ttu-id="5a37f-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a37f-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a37f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5a37f-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a37f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a37f-107">DESCRIPTION</span></span>
<span data-ttu-id="5a37f-108">Командлет **Remove-AzCosmosDBGremlinDatabase** удаляет базу данных Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="5a37f-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="5a37f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a37f-109">EXAMPLES</span></span>

### <span data-ttu-id="5a37f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a37f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="5a37f-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="5a37f-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="5a37f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a37f-112">PARAMETERS</span></span>

### <span data-ttu-id="5a37f-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="5a37f-113">-AccountName</span></span>
<span data-ttu-id="5a37f-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="5a37f-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5a37f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a37f-115">-Confirm</span></span>
<span data-ttu-id="5a37f-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a37f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a37f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a37f-117">-DefaultProfile</span></span>
<span data-ttu-id="5a37f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a37f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a37f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a37f-119">-InputObject</span></span>
<span data-ttu-id="5a37f-120">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="5a37f-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="5a37f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a37f-121">-Name</span></span>
<span data-ttu-id="5a37f-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5a37f-122">Database name.</span></span>

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

### <span data-ttu-id="5a37f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a37f-123">-PassThru</span></span>
<span data-ttu-id="5a37f-124">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="5a37f-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5a37f-125">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="5a37f-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5a37f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a37f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a37f-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a37f-127">Name of resource group.</span></span>

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

### <span data-ttu-id="5a37f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a37f-128">-WhatIf</span></span>
<span data-ttu-id="5a37f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a37f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a37f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a37f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a37f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a37f-131">CommonParameters</span></span>
<span data-ttu-id="5a37f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a37f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a37f-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5a37f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a37f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a37f-134">INPUTS</span></span>

### <span data-ttu-id="5a37f-135">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="5a37f-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="5a37f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a37f-136">OUTPUTS</span></span>

### <span data-ttu-id="5a37f-137">System. void</span><span class="sxs-lookup"><span data-stu-id="5a37f-137">System.Void</span></span>

### <span data-ttu-id="5a37f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5a37f-138">System.Boolean</span></span>

## <span data-ttu-id="5a37f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a37f-139">NOTES</span></span>

## <span data-ttu-id="5a37f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a37f-140">RELATED LINKS</span></span>
