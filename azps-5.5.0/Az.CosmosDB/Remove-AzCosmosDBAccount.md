---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/remove-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Remove-AzCosmosDBAccount.md
ms.openlocfilehash: d10ed161ddab638e32126374d106eeffe3969a8e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230825"
---
# <span data-ttu-id="e0260-101">Remove-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e0260-101">Remove-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e0260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0260-102">SYNOPSIS</span></span>
<span data-ttu-id="e0260-103">Удалите учетную запись ADB.</span><span class="sxs-lookup"><span data-stu-id="e0260-103">Remove a CosmosDB Account.</span></span>

## <span data-ttu-id="e0260-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0260-104">SYNTAX</span></span>

### <span data-ttu-id="e0260-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0260-105">ByNameParameterSet (Default)</span></span>
```
Remove-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0260-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0260-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCosmosDBAccount -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0260-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0260-107">ByObjectParameterSet</span></span>
```
Remove-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0260-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0260-108">DESCRIPTION</span></span>
<span data-ttu-id="e0260-109">Удалите учетную запись Скайп с заданным именем в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0260-109">Remove a CosmosDB Account with a given Name in the given ResourceGroup.</span></span>

## <span data-ttu-id="e0260-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0260-110">EXAMPLES</span></span>

### <span data-ttu-id="e0260-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0260-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCosmosDBAccount -ResourceGroupName rg -Name dbname  -PassThru

True
```

<span data-ttu-id="e0260-112">Учетная запись с именем учетной записи в resourceGroup rg будет удалена.</span><span class="sxs-lookup"><span data-stu-id="e0260-112">The Account with account name dbname in ResourceGroup rg is deleted.</span></span> 

## <span data-ttu-id="e0260-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0260-113">PARAMETERS</span></span>

### <span data-ttu-id="e0260-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0260-114">-AsJob</span></span>
<span data-ttu-id="e0260-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e0260-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e0260-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0260-116">-Confirm</span></span>
<span data-ttu-id="e0260-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0260-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0260-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0260-118">-DefaultProfile</span></span>
<span data-ttu-id="e0260-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0260-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0260-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0260-120">-InputObject</span></span>
<span data-ttu-id="e0260-121">Объект "Учетная запись базы данных"</span><span class="sxs-lookup"><span data-stu-id="e0260-121">The Database Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e0260-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e0260-122">-Name</span></span>
<span data-ttu-id="e0260-123">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="e0260-123">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e0260-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0260-124">-PassThru</span></span>
<span data-ttu-id="e0260-125">Если пользователь хочет получить выходные данные, должен быть установлено истинное.</span><span class="sxs-lookup"><span data-stu-id="e0260-125">To be set to true if the user wants to receive an output.</span></span>
<span data-ttu-id="e0260-126">Результат является истинным, если операция прошла успешно и если она не произошла, произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="e0260-126">The output is true if the operation was successful and an error is thrown if not.</span></span>

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

### <span data-ttu-id="e0260-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0260-127">-ResourceGroupName</span></span>
<span data-ttu-id="e0260-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e0260-128">Name of resource group.</span></span>

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

### <span data-ttu-id="e0260-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0260-129">-ResourceId</span></span>
<span data-ttu-id="e0260-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="e0260-130">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0260-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0260-131">-WhatIf</span></span>
<span data-ttu-id="e0260-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0260-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0260-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e0260-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0260-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0260-134">CommonParameters</span></span>
<span data-ttu-id="e0260-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0260-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0260-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0260-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0260-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0260-137">INPUTS</span></span>

### <span data-ttu-id="e0260-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e0260-138">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e0260-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0260-139">OUTPUTS</span></span>

### <span data-ttu-id="e0260-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="e0260-140">System.Void</span></span>

## <span data-ttu-id="e0260-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0260-141">NOTES</span></span>

## <span data-ttu-id="e0260-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0260-142">RELATED LINKS</span></span>
