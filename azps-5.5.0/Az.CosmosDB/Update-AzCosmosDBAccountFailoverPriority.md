---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100211297"
---
# <span data-ttu-id="43fe2-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="43fe2-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="43fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="43fe2-103">{{ Заполнить в synopsis }}</span><span class="sxs-lookup"><span data-stu-id="43fe2-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="43fe2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="43fe2-104">SYNTAX</span></span>

### <span data-ttu-id="43fe2-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43fe2-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43fe2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fe2-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43fe2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fe2-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43fe2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43fe2-108">DESCRIPTION</span></span>
<span data-ttu-id="43fe2-109">{{ Заполнить в описании }}</span><span class="sxs-lookup"><span data-stu-id="43fe2-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="43fe2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="43fe2-110">EXAMPLES</span></span>

### <span data-ttu-id="43fe2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43fe2-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="43fe2-112">FailoverPolicies обновлено с регионом1 как FailoverPriority 1, region2 как FailoverPriority 2 и region3 как FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="43fe2-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="43fe2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43fe2-113">PARAMETERS</span></span>

### <span data-ttu-id="43fe2-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43fe2-114">-AsJob</span></span>
<span data-ttu-id="43fe2-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="43fe2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="43fe2-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="43fe2-116">-Confirm</span></span>
<span data-ttu-id="43fe2-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43fe2-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43fe2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fe2-118">-DefaultProfile</span></span>
<span data-ttu-id="43fe2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43fe2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43fe2-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="43fe2-120">-FailoverPolicy</span></span>
<span data-ttu-id="43fe2-121">Массив строк с названиями регионов, упорядоченный по приоритету отбойного решения.</span><span class="sxs-lookup"><span data-stu-id="43fe2-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="43fe2-122">E.g eastus, westus</span><span class="sxs-lookup"><span data-stu-id="43fe2-122">E.g eastus, westus</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43fe2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43fe2-123">-InputObject</span></span>
<span data-ttu-id="43fe2-124">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="43fe2-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="43fe2-125">-Name</span><span class="sxs-lookup"><span data-stu-id="43fe2-125">-Name</span></span>
<span data-ttu-id="43fe2-126">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="43fe2-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="43fe2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43fe2-127">-ResourceGroupName</span></span>
<span data-ttu-id="43fe2-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43fe2-128">Name of resource group.</span></span>

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

### <span data-ttu-id="43fe2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43fe2-129">-ResourceId</span></span>
<span data-ttu-id="43fe2-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="43fe2-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="43fe2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43fe2-131">-WhatIf</span></span>
<span data-ttu-id="43fe2-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43fe2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43fe2-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="43fe2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43fe2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fe2-134">CommonParameters</span></span>
<span data-ttu-id="43fe2-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43fe2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fe2-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43fe2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fe2-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="43fe2-137">INPUTS</span></span>

### <span data-ttu-id="43fe2-138">Нет</span><span class="sxs-lookup"><span data-stu-id="43fe2-138">None</span></span>

## <span data-ttu-id="43fe2-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="43fe2-139">OUTPUTS</span></span>

### <span data-ttu-id="43fe2-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="43fe2-140">System.Void</span></span>

## <span data-ttu-id="43fe2-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="43fe2-141">NOTES</span></span>

## <span data-ttu-id="43fe2-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43fe2-142">RELATED LINKS</span></span>
