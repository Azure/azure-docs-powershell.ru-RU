---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242561"
---
# <span data-ttu-id="b219b-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="b219b-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="b219b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b219b-102">SYNOPSIS</span></span>
<span data-ttu-id="b219b-103">Удаляет базу данных CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="b219b-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="b219b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b219b-104">SYNTAX</span></span>

### <span data-ttu-id="b219b-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b219b-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b219b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b219b-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b219b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b219b-107">DESCRIPTION</span></span>
<span data-ttu-id="b219b-108">Командлет **Remove-AzCosmosDBMongoDBDatabase** удаляет базу данных MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="b219b-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="b219b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b219b-109">EXAMPLES</span></span>

### <span data-ttu-id="b219b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b219b-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="b219b-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="b219b-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="b219b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b219b-112">PARAMETERS</span></span>

### <span data-ttu-id="b219b-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b219b-113">-AccountName</span></span>
<span data-ttu-id="b219b-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b219b-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b219b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b219b-115">-Confirm</span></span>
<span data-ttu-id="b219b-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b219b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b219b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b219b-117">-DefaultProfile</span></span>
<span data-ttu-id="b219b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b219b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b219b-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b219b-119">-InputObject</span></span>
<span data-ttu-id="b219b-120">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="b219b-120">Mongo Database object.</span></span>

```yaml
Type: PSMongoDBDatabaseGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b219b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b219b-121">-Name</span></span>
<span data-ttu-id="b219b-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b219b-122">Database name.</span></span>

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

### <span data-ttu-id="b219b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b219b-123">-PassThru</span></span>
<span data-ttu-id="b219b-124">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="b219b-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="b219b-125">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b219b-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="b219b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b219b-126">-ResourceGroupName</span></span>
<span data-ttu-id="b219b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b219b-127">Name of resource group.</span></span>

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

### <span data-ttu-id="b219b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b219b-128">-WhatIf</span></span>
<span data-ttu-id="b219b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b219b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b219b-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b219b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b219b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b219b-131">CommonParameters</span></span>
<span data-ttu-id="b219b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b219b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b219b-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b219b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b219b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b219b-134">INPUTS</span></span>

### <span data-ttu-id="b219b-135">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="b219b-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="b219b-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b219b-136">OUTPUTS</span></span>

### <span data-ttu-id="b219b-137">System. void</span><span class="sxs-lookup"><span data-stu-id="b219b-137">System.Void</span></span>

### <span data-ttu-id="b219b-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b219b-138">System.Boolean</span></span>

## <span data-ttu-id="b219b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="b219b-139">NOTES</span></span>

## <span data-ttu-id="b219b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b219b-140">RELATED LINKS</span></span>
