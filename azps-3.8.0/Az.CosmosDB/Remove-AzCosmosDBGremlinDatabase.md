---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbgremlindatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBGremlinDatabase.md
ms.openlocfilehash: 5c3150e2bdb81c8864116bc521b9f07f2ea43e1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073621"
---
# <span data-ttu-id="9f05d-101">Remove-AzCosmosDBGremlinDatabase</span><span class="sxs-lookup"><span data-stu-id="9f05d-101">Remove-AzCosmosDBGremlinDatabase</span></span>

## <span data-ttu-id="9f05d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f05d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f05d-103">Удаляет базу данных CosmosDB Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9f05d-103">Deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9f05d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f05d-104">SYNTAX</span></span>

### <span data-ttu-id="9f05d-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f05d-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f05d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f05d-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBGremlinDatabase -InputObject <PSGremlinDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f05d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f05d-107">DESCRIPTION</span></span>
<span data-ttu-id="9f05d-108">Командлет **Remove-AzCosmosDBGremlinDatabase** удаляет базу данных Gremlin CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="9f05d-108">The **Remove-AzCosmosDBGremlinDatabase** cmdlet deletes a CosmosDB Gremlin Database.</span></span>

## <span data-ttu-id="9f05d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f05d-109">EXAMPLES</span></span>

### <span data-ttu-id="9f05d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f05d-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBGremlinDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="9f05d-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="9f05d-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="9f05d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f05d-112">PARAMETERS</span></span>

### <span data-ttu-id="9f05d-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="9f05d-113">-AccountName</span></span>
<span data-ttu-id="9f05d-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="9f05d-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9f05d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f05d-115">-Confirm</span></span>
<span data-ttu-id="9f05d-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f05d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f05d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f05d-117">-DefaultProfile</span></span>
<span data-ttu-id="9f05d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f05d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f05d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f05d-119">-InputObject</span></span>
<span data-ttu-id="9f05d-120">Объект базы данных Gremlin.</span><span class="sxs-lookup"><span data-stu-id="9f05d-120">Gremlin Database object.</span></span>

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

### <span data-ttu-id="9f05d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f05d-121">-Name</span></span>
<span data-ttu-id="9f05d-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9f05d-122">Database name.</span></span>

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

### <span data-ttu-id="9f05d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9f05d-123">-PassThru</span></span>
<span data-ttu-id="9f05d-124">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="9f05d-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="9f05d-125">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="9f05d-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="9f05d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f05d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f05d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f05d-127">Name of resource group.</span></span>

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

### <span data-ttu-id="9f05d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f05d-128">-WhatIf</span></span>
<span data-ttu-id="9f05d-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f05d-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f05d-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f05d-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f05d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f05d-131">CommonParameters</span></span>
<span data-ttu-id="9f05d-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f05d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f05d-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f05d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f05d-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f05d-134">INPUTS</span></span>

### <span data-ttu-id="9f05d-135">Microsoft. Azure. Commands. CosmosDB. Models. PSGremlinDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="9f05d-135">Microsoft.Azure.Commands.CosmosDB.Models.PSGremlinDatabaseGetResults</span></span>

## <span data-ttu-id="9f05d-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f05d-136">OUTPUTS</span></span>

### <span data-ttu-id="9f05d-137">System. void</span><span class="sxs-lookup"><span data-stu-id="9f05d-137">System.Void</span></span>

### <span data-ttu-id="9f05d-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f05d-138">System.Boolean</span></span>

## <span data-ttu-id="9f05d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f05d-139">NOTES</span></span>

## <span data-ttu-id="9f05d-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f05d-140">RELATED LINKS</span></span>
