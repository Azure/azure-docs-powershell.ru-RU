---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBCollection.md
ms.openlocfilehash: 69d3fa5be2b5650a3d4093c63a20d43e098062b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404775"
---
# <span data-ttu-id="5adca-101">Remove-AzCosmosDBMongoDBCollection</span><span class="sxs-lookup"><span data-stu-id="5adca-101">Remove-AzCosmosDBMongoDBCollection</span></span>

## <span data-ttu-id="5adca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5adca-102">SYNOPSIS</span></span>
<span data-ttu-id="5adca-103">Удаляет коллекцию "Диски" (MongoDB).</span><span class="sxs-lookup"><span data-stu-id="5adca-103">Deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5adca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5adca-104">SYNTAX</span></span>

### <span data-ttu-id="5adca-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5adca-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBMongoDBCollection -ResourceGroupName <String> -AccountName <String> -DatabaseName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5adca-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5adca-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBCollection -InputObject <PSMongoDBCollectionGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5adca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5adca-107">DESCRIPTION</span></span>
<span data-ttu-id="5adca-108">Cmdlet **Remove-AzCosmosDBMongoDBCollection** удаляет коллекцию Вадима МонгоDB.</span><span class="sxs-lookup"><span data-stu-id="5adca-108">The **Remove-AzCosmosDBMongoDBCollection** cmdlet deletes a CosmosDB MongoDB Collection.</span></span>

## <span data-ttu-id="5adca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5adca-109">EXAMPLES</span></span>

### <span data-ttu-id="5adca-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5adca-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBCollection -ResourceGroupName {rgName} -AccountName {accountName} -DatabaseName {dbName} -Name {collectionName}
```

<span data-ttu-id="5adca-111">Если удаление прошло успешно, он возвращает объект типа bool(при -PassThru).</span><span class="sxs-lookup"><span data-stu-id="5adca-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="5adca-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5adca-112">PARAMETERS</span></span>

### <span data-ttu-id="5adca-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5adca-113">-AccountName</span></span>
<span data-ttu-id="5adca-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="5adca-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="5adca-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5adca-115">-Confirm</span></span>
<span data-ttu-id="5adca-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5adca-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5adca-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5adca-117">-DatabaseName</span></span>
<span data-ttu-id="5adca-118">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5adca-118">Database name.</span></span>

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

### <span data-ttu-id="5adca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5adca-119">-DefaultProfile</span></span>
<span data-ttu-id="5adca-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5adca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5adca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5adca-121">-InputObject</span></span>
<span data-ttu-id="5adca-122">Объект контейнера Sql.</span><span class="sxs-lookup"><span data-stu-id="5adca-122">Sql Container object.</span></span>

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

### <span data-ttu-id="5adca-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5adca-123">-Name</span></span>
<span data-ttu-id="5adca-124">Имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="5adca-124">Collection name.</span></span>

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

### <span data-ttu-id="5adca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5adca-125">-PassThru</span></span>
<span data-ttu-id="5adca-126">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="5adca-126">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="5adca-127">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="5adca-127">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="5adca-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5adca-128">-ResourceGroupName</span></span>
<span data-ttu-id="5adca-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5adca-129">Name of resource group.</span></span>

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

### <span data-ttu-id="5adca-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5adca-130">-WhatIf</span></span>
<span data-ttu-id="5adca-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5adca-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5adca-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5adca-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5adca-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5adca-133">CommonParameters</span></span>
<span data-ttu-id="5adca-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5adca-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5adca-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5adca-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5adca-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5adca-136">INPUTS</span></span>

### <span data-ttu-id="5adca-137">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBCollectionGetResults</span><span class="sxs-lookup"><span data-stu-id="5adca-137">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBCollectionGetResults</span></span>

## <span data-ttu-id="5adca-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5adca-138">OUTPUTS</span></span>

### <span data-ttu-id="5adca-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="5adca-139">System.Void</span></span>

### <span data-ttu-id="5adca-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5adca-140">System.Boolean</span></span>

## <span data-ttu-id="5adca-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5adca-141">NOTES</span></span>

## <span data-ttu-id="5adca-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5adca-142">RELATED LINKS</span></span>
