---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 6a1c155a33ef704895a76dc35bf342aa47cd47ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078376"
---
# <span data-ttu-id="b96cc-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="b96cc-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="b96cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b96cc-102">SYNOPSIS</span></span>
<span data-ttu-id="b96cc-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="b96cc-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="b96cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b96cc-104">SYNTAX</span></span>

### <span data-ttu-id="b96cc-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b96cc-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96cc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b96cc-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b96cc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b96cc-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccountGetResults>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b96cc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b96cc-108">DESCRIPTION</span></span>
<span data-ttu-id="b96cc-109">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="b96cc-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="b96cc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b96cc-110">EXAMPLES</span></span>

### <span data-ttu-id="b96cc-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b96cc-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="b96cc-112">FailoverPolicies обновил Region1 как FailoverPriority 1, region2 AS FailoverPriority 2 и region3 как FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="b96cc-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="b96cc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b96cc-113">PARAMETERS</span></span>

### <span data-ttu-id="b96cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b96cc-114">-AsJob</span></span>
<span data-ttu-id="b96cc-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b96cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b96cc-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b96cc-116">-Confirm</span></span>
<span data-ttu-id="b96cc-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b96cc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b96cc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96cc-118">-DefaultProfile</span></span>
<span data-ttu-id="b96cc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b96cc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b96cc-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="b96cc-120">-FailoverPolicy</span></span>
<span data-ttu-id="b96cc-121">Массив строк с именами областей, упорядоченных по приоритету отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="b96cc-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="b96cc-122">Например, eastus, westus</span><span class="sxs-lookup"><span data-stu-id="b96cc-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="b96cc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b96cc-123">-InputObject</span></span>
<span data-ttu-id="b96cc-124">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="b96cc-124">CosmosDB Account object</span></span>

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

### <span data-ttu-id="b96cc-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b96cc-125">-Name</span></span>
<span data-ttu-id="b96cc-126">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="b96cc-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="b96cc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96cc-127">-ResourceGroupName</span></span>
<span data-ttu-id="b96cc-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b96cc-128">Name of resource group.</span></span>

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

### <span data-ttu-id="b96cc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b96cc-129">-ResourceId</span></span>
<span data-ttu-id="b96cc-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="b96cc-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="b96cc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b96cc-131">-WhatIf</span></span>
<span data-ttu-id="b96cc-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b96cc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b96cc-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b96cc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b96cc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96cc-134">CommonParameters</span></span>
<span data-ttu-id="b96cc-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b96cc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96cc-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b96cc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96cc-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b96cc-137">INPUTS</span></span>

### <span data-ttu-id="b96cc-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="b96cc-138">None</span></span>

## <span data-ttu-id="b96cc-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b96cc-139">OUTPUTS</span></span>

### <span data-ttu-id="b96cc-140">System. void</span><span class="sxs-lookup"><span data-stu-id="b96cc-140">System.Void</span></span>

## <span data-ttu-id="b96cc-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="b96cc-141">NOTES</span></span>

## <span data-ttu-id="b96cc-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b96cc-142">RELATED LINKS</span></span>
