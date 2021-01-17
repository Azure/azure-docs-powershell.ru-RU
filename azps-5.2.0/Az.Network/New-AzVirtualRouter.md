---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412311"
---
# <span data-ttu-id="bd9e2-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bd9e2-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="bd9e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="bd9e2-103">Создает Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="bd9e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd9e2-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bd9e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd9e2-105">DESCRIPTION</span></span>
<span data-ttu-id="bd9e2-106">С **его использованием** создается виртуальныйrouter Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="bd9e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd9e2-107">EXAMPLES</span></span>

### <span data-ttu-id="bd9e2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd9e2-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="bd9e2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd9e2-109">PARAMETERS</span></span>

### <span data-ttu-id="bd9e2-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bd9e2-110">-AsJob</span></span>
<span data-ttu-id="bd9e2-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bd9e2-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bd9e2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd9e2-112">-DefaultProfile</span></span>
<span data-ttu-id="bd9e2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd9e2-114">-Force</span><span class="sxs-lookup"><span data-stu-id="bd9e2-114">-Force</span></span>
<span data-ttu-id="bd9e2-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="bd9e2-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="bd9e2-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="bd9e2-116">-HostedSubnet</span></span>
<span data-ttu-id="bd9e2-117">Подсеть, в которой находится виртуальный маршрутизатор.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-117">The subnet where the virtual router is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd9e2-118">-Location</span><span class="sxs-lookup"><span data-stu-id="bd9e2-118">-Location</span></span>
<span data-ttu-id="bd9e2-119">Расположение.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-119">The location.</span></span>

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

### <span data-ttu-id="bd9e2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="bd9e2-120">-Name</span></span>
<span data-ttu-id="bd9e2-121">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-121">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9e2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd9e2-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd9e2-123">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="bd9e2-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd9e2-124">-Tag</span></span>
<span data-ttu-id="bd9e2-125">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd9e2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd9e2-126">-Confirm</span></span>
<span data-ttu-id="bd9e2-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd9e2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd9e2-128">-WhatIf</span></span>
<span data-ttu-id="bd9e2-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd9e2-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd9e2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd9e2-131">CommonParameters</span></span>
<span data-ttu-id="bd9e2-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd9e2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd9e2-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd9e2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd9e2-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd9e2-134">INPUTS</span></span>

### <span data-ttu-id="bd9e2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bd9e2-135">System.String</span></span>

### <span data-ttu-id="bd9e2-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bd9e2-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bd9e2-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd9e2-137">OUTPUTS</span></span>

### <span data-ttu-id="bd9e2-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bd9e2-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="bd9e2-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd9e2-139">NOTES</span></span>

## <span data-ttu-id="bd9e2-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd9e2-140">RELATED LINKS</span></span>
