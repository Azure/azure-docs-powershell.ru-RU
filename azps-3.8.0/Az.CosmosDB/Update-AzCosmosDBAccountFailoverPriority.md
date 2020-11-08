---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccountfailoverpriority
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccountFailoverPriority.md
ms.openlocfilehash: 4a6c93c0946780420cffb8b5cb6d2e9331d55bae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065018"
---
# <span data-ttu-id="aadf5-101">Update-AzCosmosDBAccountFailoverPriority</span><span class="sxs-lookup"><span data-stu-id="aadf5-101">Update-AzCosmosDBAccountFailoverPriority</span></span>

## <span data-ttu-id="aadf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aadf5-102">SYNOPSIS</span></span>
<span data-ttu-id="aadf5-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="aadf5-103">{{ Fill in the Synopsis }}</span></span>

## <span data-ttu-id="aadf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aadf5-104">SYNTAX</span></span>

### <span data-ttu-id="aadf5-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aadf5-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName <String> -Name <String> -FailoverPolicy <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aadf5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadf5-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -ResourceId <String> -FailoverPolicy <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aadf5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aadf5-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccountFailoverPriority -FailoverPolicy <String[]> -InputObject <PSDatabaseAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aadf5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aadf5-108">DESCRIPTION</span></span>
<span data-ttu-id="aadf5-109">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="aadf5-109">{{ Fill in the Description }}</span></span>

## <span data-ttu-id="aadf5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aadf5-110">EXAMPLES</span></span>

### <span data-ttu-id="aadf5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aadf5-111">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccountFailoverPriority -ResourceGroupName rg -Name dbname -FailoverPolicy "region1, region2, region3"
```

<span data-ttu-id="aadf5-112">FailoverPolicies обновил Region1 как FailoverPriority 1, region2 AS FailoverPriority 2 и region3 как FailoverPriority 3.</span><span class="sxs-lookup"><span data-stu-id="aadf5-112">FailoverPolicies updated with region1 as FailoverPriority 1, region2 as FailoverPriority 2 and region3 as FailoverPriority 3.</span></span>

## <span data-ttu-id="aadf5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aadf5-113">PARAMETERS</span></span>

### <span data-ttu-id="aadf5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aadf5-114">-AsJob</span></span>
<span data-ttu-id="aadf5-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aadf5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aadf5-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aadf5-116">-Confirm</span></span>
<span data-ttu-id="aadf5-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aadf5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aadf5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadf5-118">-DefaultProfile</span></span>
<span data-ttu-id="aadf5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aadf5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aadf5-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="aadf5-120">-FailoverPolicy</span></span>
<span data-ttu-id="aadf5-121">Массив строк с именами областей, упорядоченных по приоритету отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="aadf5-121">Array of strings having region names, ordered by failover priority.</span></span>
<span data-ttu-id="aadf5-122">Например, eastus, westus</span><span class="sxs-lookup"><span data-stu-id="aadf5-122">E.g eastus, westus</span></span>

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

### <span data-ttu-id="aadf5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aadf5-123">-InputObject</span></span>
<span data-ttu-id="aadf5-124">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="aadf5-124">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aadf5-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aadf5-125">-Name</span></span>
<span data-ttu-id="aadf5-126">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="aadf5-126">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="aadf5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aadf5-127">-ResourceGroupName</span></span>
<span data-ttu-id="aadf5-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aadf5-128">Name of resource group.</span></span>

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

### <span data-ttu-id="aadf5-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aadf5-129">-ResourceId</span></span>
<span data-ttu-id="aadf5-130">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="aadf5-130">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="aadf5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aadf5-131">-WhatIf</span></span>
<span data-ttu-id="aadf5-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aadf5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aadf5-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aadf5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aadf5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadf5-134">CommonParameters</span></span>
<span data-ttu-id="aadf5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aadf5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadf5-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aadf5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadf5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aadf5-137">INPUTS</span></span>

### <span data-ttu-id="aadf5-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="aadf5-138">None</span></span>

## <span data-ttu-id="aadf5-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aadf5-139">OUTPUTS</span></span>

### <span data-ttu-id="aadf5-140">System. void</span><span class="sxs-lookup"><span data-stu-id="aadf5-140">System.Void</span></span>

## <span data-ttu-id="aadf5-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="aadf5-141">NOTES</span></span>

## <span data-ttu-id="aadf5-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aadf5-142">RELATED LINKS</span></span>
