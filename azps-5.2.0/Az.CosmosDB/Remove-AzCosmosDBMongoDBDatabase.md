---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbmongodbdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBMongoDBDatabase.md
ms.openlocfilehash: 6f2490eee06ab9cded7634fec1c938d40b4feb50
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404767"
---
# <span data-ttu-id="3b1a5-101">Remove-AzCosmosDBMongoDBDatabase</span><span class="sxs-lookup"><span data-stu-id="3b1a5-101">Remove-AzCosmosDBMongoDBDatabase</span></span>

## <span data-ttu-id="3b1a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="3b1a5-103">Удаляет базу данных ВайссDB (MongoDB).</span><span class="sxs-lookup"><span data-stu-id="3b1a5-103">Deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="3b1a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b1a5-104">SYNTAX</span></span>

### <span data-ttu-id="3b1a5-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1a5-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b1a5-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b1a5-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBMongoDBDatabase -InputObject <PSMongoDBDatabaseGetResults> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b1a5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b1a5-107">DESCRIPTION</span></span>
<span data-ttu-id="3b1a5-108">При этом удаляется база данных **AzCosdbMongoDBDatabase.**</span><span class="sxs-lookup"><span data-stu-id="3b1a5-108">The **Remove-AzCosmosDBMongoDBDatabase** cmdlet deletes a CosmosDB MongoDB Database.</span></span>

## <span data-ttu-id="3b1a5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b1a5-109">EXAMPLES</span></span>

### <span data-ttu-id="3b1a5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3b1a5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBMongoDBDatabase -ResourceGroupName {rgName} -AccountName {accountName} -Name {dbName}
```

<span data-ttu-id="3b1a5-111">Если удаление прошло успешно, он возвращает объект типа bool(при -PassThru).</span><span class="sxs-lookup"><span data-stu-id="3b1a5-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="3b1a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b1a5-112">PARAMETERS</span></span>

### <span data-ttu-id="3b1a5-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3b1a5-113">-AccountName</span></span>
<span data-ttu-id="3b1a5-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="3b1a5-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3b1a5-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b1a5-115">-Confirm</span></span>
<span data-ttu-id="3b1a5-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b1a5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b1a5-117">-DefaultProfile</span></span>
<span data-ttu-id="3b1a5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b1a5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b1a5-119">-InputObject</span></span>
<span data-ttu-id="3b1a5-120">Объект базы данных Mongo.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-120">Mongo Database object.</span></span>

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

### <span data-ttu-id="3b1a5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3b1a5-121">-Name</span></span>
<span data-ttu-id="3b1a5-122">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-122">Database name.</span></span>

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

### <span data-ttu-id="3b1a5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b1a5-123">-PassThru</span></span>
<span data-ttu-id="3b1a5-124">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="3b1a5-125">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="3b1a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b1a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b1a5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-127">Name of resource group.</span></span>

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

### <span data-ttu-id="3b1a5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b1a5-128">-WhatIf</span></span>
<span data-ttu-id="3b1a5-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b1a5-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b1a5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b1a5-131">CommonParameters</span></span>
<span data-ttu-id="3b1a5-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b1a5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b1a5-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b1a5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b1a5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b1a5-134">INPUTS</span></span>

### <span data-ttu-id="3b1a5-135">Microsoft.Azure.Commands.GetsDB.Models.PSMongoDBDatabaseGetResults</span><span class="sxs-lookup"><span data-stu-id="3b1a5-135">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoDBDatabaseGetResults</span></span>

## <span data-ttu-id="3b1a5-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b1a5-136">OUTPUTS</span></span>

### <span data-ttu-id="3b1a5-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="3b1a5-137">System.Void</span></span>

### <span data-ttu-id="3b1a5-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3b1a5-138">System.Boolean</span></span>

## <span data-ttu-id="3b1a5-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b1a5-139">NOTES</span></span>

## <span data-ttu-id="3b1a5-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b1a5-140">RELATED LINKS</span></span>
