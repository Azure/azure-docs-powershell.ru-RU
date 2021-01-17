---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328219"
---
# <span data-ttu-id="6a40f-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="6a40f-101">New-AzHpcCache</span></span>

## <span data-ttu-id="6a40f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a40f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a40f-103">Создает кэш HPC.</span><span class="sxs-lookup"><span data-stu-id="6a40f-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="6a40f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6a40f-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a40f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6a40f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a40f-106">Для **создания кэша HPC Azure создается** новый кэш AzHpcCache.</span><span class="sxs-lookup"><span data-stu-id="6a40f-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="6a40f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6a40f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a40f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6a40f-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="6a40f-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a40f-109">PARAMETERS</span></span>

### <span data-ttu-id="6a40f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a40f-110">-AsJob</span></span>
<span data-ttu-id="6a40f-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6a40f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a40f-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="6a40f-112">-CacheSize</span></span>
<span data-ttu-id="6a40f-113">"КэшSize".</span><span class="sxs-lookup"><span data-stu-id="6a40f-113">CacheSize.</span></span>

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

### <span data-ttu-id="6a40f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a40f-114">-DefaultProfile</span></span>
<span data-ttu-id="6a40f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6a40f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a40f-116">-Location</span><span class="sxs-lookup"><span data-stu-id="6a40f-116">-Location</span></span>
<span data-ttu-id="6a40f-117">"Расположение".</span><span class="sxs-lookup"><span data-stu-id="6a40f-117">Location.</span></span>

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

### <span data-ttu-id="6a40f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6a40f-118">-Name</span></span>
<span data-ttu-id="6a40f-119">Имя кэша.</span><span class="sxs-lookup"><span data-stu-id="6a40f-119">Name of cache.</span></span>

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

### <span data-ttu-id="6a40f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a40f-120">-ResourceGroupName</span></span>
<span data-ttu-id="6a40f-121">Имя группы ресурсов, под которой вы хотите создать кэш.</span><span class="sxs-lookup"><span data-stu-id="6a40f-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="6a40f-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="6a40f-122">-Sku</span></span>
<span data-ttu-id="6a40f-123">SKU.</span><span class="sxs-lookup"><span data-stu-id="6a40f-123">Sku.</span></span>

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

### <span data-ttu-id="6a40f-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="6a40f-124">-SubnetUri</span></span>
<span data-ttu-id="6a40f-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="6a40f-125">SubnetURI.</span></span>

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

### <span data-ttu-id="6a40f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a40f-126">-Tag</span></span>
<span data-ttu-id="6a40f-127">Теги, которые нужно связать с кэшом HPC.</span><span class="sxs-lookup"><span data-stu-id="6a40f-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="6a40f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6a40f-128">-Confirm</span></span>
<span data-ttu-id="6a40f-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a40f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a40f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a40f-130">-WhatIf</span></span>
<span data-ttu-id="6a40f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a40f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a40f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6a40f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a40f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a40f-133">CommonParameters</span></span>
<span data-ttu-id="6a40f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a40f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a40f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a40f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a40f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6a40f-136">INPUTS</span></span>

### <span data-ttu-id="6a40f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6a40f-137">System.String</span></span>

### <span data-ttu-id="6a40f-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6a40f-138">System.Int32</span></span>

## <span data-ttu-id="6a40f-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a40f-139">OUTPUTS</span></span>

### <span data-ttu-id="6a40f-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="6a40f-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="6a40f-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6a40f-141">NOTES</span></span>

## <span data-ttu-id="6a40f-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6a40f-142">RELATED LINKS</span></span>
