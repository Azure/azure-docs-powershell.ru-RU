---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236690"
---
# <span data-ttu-id="c5341-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="c5341-101">New-AzHpcCache</span></span>

## <span data-ttu-id="c5341-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5341-102">SYNOPSIS</span></span>
<span data-ttu-id="c5341-103">Создание кэша HPC.</span><span class="sxs-lookup"><span data-stu-id="c5341-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="c5341-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5341-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5341-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5341-105">DESCRIPTION</span></span>
<span data-ttu-id="c5341-106">Командлет **New-AzHpcCache** создает кэш Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="c5341-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="c5341-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5341-107">EXAMPLES</span></span>

### <span data-ttu-id="c5341-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5341-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="c5341-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5341-109">PARAMETERS</span></span>

### <span data-ttu-id="c5341-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5341-110">-AsJob</span></span>
<span data-ttu-id="c5341-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c5341-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="c5341-112">-CacheSize</span></span>
<span data-ttu-id="c5341-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="c5341-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5341-114">-DefaultProfile</span></span>
<span data-ttu-id="c5341-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5341-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-116">-Location</span><span class="sxs-lookup"><span data-stu-id="c5341-116">-Location</span></span>
<span data-ttu-id="c5341-117">Поиска.</span><span class="sxs-lookup"><span data-stu-id="c5341-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5341-118">-Name</span></span>
<span data-ttu-id="c5341-119">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="c5341-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5341-120">-ResourceGroupName</span></span>
<span data-ttu-id="c5341-121">Имя группы ресурсов, в которой вы хотите создать кэш.</span><span class="sxs-lookup"><span data-stu-id="c5341-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="c5341-122">-Sku</span></span>
<span data-ttu-id="c5341-123">Кратки.</span><span class="sxs-lookup"><span data-stu-id="c5341-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="c5341-124">-SubnetUri</span></span>
<span data-ttu-id="c5341-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="c5341-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="c5341-126">-Tag</span></span>
<span data-ttu-id="c5341-127">Теги, которые нужно связать с кэшем HPC.</span><span class="sxs-lookup"><span data-stu-id="c5341-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5341-128">-Confirm</span></span>
<span data-ttu-id="c5341-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5341-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5341-130">-WhatIf</span></span>
<span data-ttu-id="c5341-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5341-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5341-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5341-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5341-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5341-133">CommonParameters</span></span>
<span data-ttu-id="c5341-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5341-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5341-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5341-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5341-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5341-136">INPUTS</span></span>

### <span data-ttu-id="c5341-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c5341-137">System.String</span></span>

### <span data-ttu-id="c5341-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c5341-138">System.Int32</span></span>

## <span data-ttu-id="c5341-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5341-139">OUTPUTS</span></span>

### <span data-ttu-id="c5341-140">Microsoft. Azure. PowerShell. командлеты. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="c5341-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="c5341-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5341-141">NOTES</span></span>

## <span data-ttu-id="c5341-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5341-142">RELATED LINKS</span></span>
