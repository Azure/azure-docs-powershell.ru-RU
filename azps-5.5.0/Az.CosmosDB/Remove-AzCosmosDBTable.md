---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbtable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBTable.md
ms.openlocfilehash: ab8f0367f932a96d6296b5e6174bc3b6bbb651f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238433"
---
# <span data-ttu-id="fbb64-101">Remove-AzCosmosDBTable</span><span class="sxs-lookup"><span data-stu-id="fbb64-101">Remove-AzCosmosDBTable</span></span>

## <span data-ttu-id="fbb64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb64-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb64-103">Удаляет таблицу "Приобр".</span><span class="sxs-lookup"><span data-stu-id="fbb64-103">Deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="fbb64-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fbb64-104">SYNTAX</span></span>

### <span data-ttu-id="fbb64-105">ByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb64-105">ByNameParameterSet</span></span>
```
Remove-AzCosmosDBTable -AccountName <String> -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb64-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb64-106">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBTable -InputObject <PSTableGetResults> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbb64-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb64-107">DESCRIPTION</span></span>
<span data-ttu-id="fbb64-108">При **этом удаляется** таблица "БазсDB".</span><span class="sxs-lookup"><span data-stu-id="fbb64-108">The **Remove-AzCosmosDBTable** cmdlet deletes the CosmosDB Table.</span></span>

## <span data-ttu-id="fbb64-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fbb64-109">EXAMPLES</span></span>

### <span data-ttu-id="fbb64-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fbb64-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBTable -AccountName {account} -Name {tableName} -ResourceGroupName {rgName}
```

<span data-ttu-id="fbb64-111">Если удаление прошло успешно, cmdlet возвращает объект типа bool(когда -PassThru is passThru), который является истинным.</span><span class="sxs-lookup"><span data-stu-id="fbb64-111">The cmdlet returns an object of type bool(when -PassThru is passed) which is true, if the delete was successful.</span></span>

## <span data-ttu-id="fbb64-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb64-112">PARAMETERS</span></span>

### <span data-ttu-id="fbb64-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fbb64-113">-AccountName</span></span>
<span data-ttu-id="fbb64-114">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="fbb64-114">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="fbb64-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb64-115">-Confirm</span></span>
<span data-ttu-id="fbb64-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb64-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb64-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb64-117">-DefaultProfile</span></span>
<span data-ttu-id="fbb64-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb64-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbb64-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbb64-119">-InputObject</span></span>
<span data-ttu-id="fbb64-120">Объект базы данных Sql.</span><span class="sxs-lookup"><span data-stu-id="fbb64-120">Sql Database object.</span></span>

```yaml
Type: PSTableGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbb64-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fbb64-121">-Name</span></span>
<span data-ttu-id="fbb64-122">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="fbb64-122">Name of the Table.</span></span>

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

### <span data-ttu-id="fbb64-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbb64-123">-PassThru</span></span>
<span data-ttu-id="fbb64-124">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="fbb64-124">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="fbb64-125">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="fbb64-125">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="fbb64-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbb64-126">-ResourceGroupName</span></span>
<span data-ttu-id="fbb64-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbb64-127">Name of resource group.</span></span>

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

### <span data-ttu-id="fbb64-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb64-128">-WhatIf</span></span>
<span data-ttu-id="fbb64-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbb64-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb64-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fbb64-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb64-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb64-131">CommonParameters</span></span>
<span data-ttu-id="fbb64-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb64-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb64-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbb64-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb64-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fbb64-134">INPUTS</span></span>

### <span data-ttu-id="fbb64-135">Microsoft.Azure.Commands.GetsDB.Models.PSTableGetResults</span><span class="sxs-lookup"><span data-stu-id="fbb64-135">Microsoft.Azure.Commands.CosmosDB.Models.PSTableGetResults</span></span>

## <span data-ttu-id="fbb64-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fbb64-136">OUTPUTS</span></span>

### <span data-ttu-id="fbb64-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="fbb64-137">System.Void</span></span>

### <span data-ttu-id="fbb64-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fbb64-138">System.Boolean</span></span>

## <span data-ttu-id="fbb64-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fbb64-139">NOTES</span></span>

## <span data-ttu-id="fbb64-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbb64-140">RELATED LINKS</span></span>
