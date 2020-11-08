---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244613"
---
# <span data-ttu-id="4df37-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="4df37-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="4df37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4df37-102">SYNOPSIS</span></span>
<span data-ttu-id="4df37-103">Удаляет коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="4df37-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="4df37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4df37-104">SYNTAX</span></span>

### <span data-ttu-id="4df37-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4df37-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4df37-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4df37-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4df37-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4df37-107">DESCRIPTION</span></span>
<span data-ttu-id="4df37-108">Командлет **Remove-AzCosmosDBMongoDBCollection** удаляет коллекцию CosmosDB MongoDB.</span><span class="sxs-lookup"><span data-stu-id="4df37-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="4df37-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4df37-109">EXAMPLES</span></span>

### <span data-ttu-id="4df37-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4df37-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="4df37-111">Командлет возвращает объект типа bool (параметр when-PassThru передается), который имеет значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="4df37-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="4df37-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4df37-112">PARAMETERS</span></span>

### <span data-ttu-id="4df37-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4df37-113">-AccountName</span></span>
<span data-ttu-id="4df37-114">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="4df37-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="4df37-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4df37-115">-Confirm</span></span>
<span data-ttu-id="4df37-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4df37-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df37-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4df37-117">-DatabaseName</span></span>
<span data-ttu-id="4df37-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="4df37-118">Database name.</span></span>

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

### <span data-ttu-id="4df37-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df37-119">-DefaultProfile</span></span>
<span data-ttu-id="4df37-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4df37-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df37-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4df37-121">-InputObject</span></span>
<span data-ttu-id="4df37-122">Объект контейнера SQL.</span><span class="sxs-lookup"><span data-stu-id="4df37-122">Sql Container object.</span></span>

```yaml
Type: PSMongoDBCollectionGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4df37-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4df37-123">-Name</span></span>
<span data-ttu-id="4df37-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="4df37-124">Collection name.</span></span>

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

### <span data-ttu-id="4df37-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df37-125">-PassThru</span></span>
<span data-ttu-id="4df37-126">Имеет значение true, если пользователь хочет получить вывод.</span><span class="sxs-lookup"><span data-stu-id="4df37-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="4df37-127">Вывод имеет значение истина, если операция была выполнена успешно, и в противном случае возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="4df37-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="4df37-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df37-128">-ResourceGroupName</span></span>
<span data-ttu-id="4df37-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4df37-129">Name of resource group.</span></span>

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

### <span data-ttu-id="4df37-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df37-130">-WhatIf</span></span>
<span data-ttu-id="4df37-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4df37-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df37-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4df37-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df37-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df37-133">CommonParameters</span></span>
<span data-ttu-id="4df37-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4df37-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df37-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4df37-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df37-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4df37-136">INPUTS</span></span>

### <span data-ttu-id="4df37-137">Microsoft. Azure. Commands. CosmosDB. Models. PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="4df37-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="4df37-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4df37-138">OUTPUTS</span></span>

### <span data-ttu-id="4df37-139">System. void</span><span class="sxs-lookup"><span data-stu-id="4df37-139">System.Void</span></span>

### <span data-ttu-id="4df37-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4df37-140">System.Boolean</span></span>

## <span data-ttu-id="4df37-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4df37-141">NOTES</span></span>

## <span data-ttu-id="4df37-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4df37-142">RELATED LINKS</span></span>
