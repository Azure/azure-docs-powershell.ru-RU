---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 9bfaea690ab23df6e7ba5480aaeb28ca00dfa20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236673"
---
# <span data-ttu-id="4dddd-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4dddd-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="4dddd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dddd-102">SYNOPSIS</span></span>
<span data-ttu-id="4dddd-103">Создает Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="4dddd-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="4dddd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4dddd-104">SYNTAX</span></span>

```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedSubnet <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4dddd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dddd-105">DESCRIPTION</span></span>
<span data-ttu-id="4dddd-106">Для создания azure VirtualRouter с его использованием создается новый cmdlet Azure **AzVirtualRouter.**</span><span class="sxs-lookup"><span data-stu-id="4dddd-106">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>

## <span data-ttu-id="4dddd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4dddd-107">EXAMPLES</span></span>

### <span data-ttu-id="4dddd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4dddd-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name $subnetName -AddressPrefix 10.0.0.0/24
$vnet = New-AzVirtualNetwork -Name $vnetName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -AddressPrefix 10.0.0.0/16 -Subnet $subnet
$subnetId = (Get-AzVirtualNetworkSubnetConfig -Name $subnetName -VirtualNetwork $vnet).Id
New-AzVirtualRouter -Name $virtualRouterName -ResourceGroupName $resourceGroupName -Location $resourceGroupLocation -HostedSubnet $subnetId
```

## <span data-ttu-id="4dddd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dddd-109">PARAMETERS</span></span>

### <span data-ttu-id="4dddd-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dddd-110">-AsJob</span></span>
<span data-ttu-id="4dddd-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4dddd-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4dddd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dddd-112">-DefaultProfile</span></span>
<span data-ttu-id="4dddd-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dddd-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dddd-114">-Force</span><span class="sxs-lookup"><span data-stu-id="4dddd-114">-Force</span></span>
<span data-ttu-id="4dddd-115">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="4dddd-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4dddd-116">-HostedSubnet</span><span class="sxs-lookup"><span data-stu-id="4dddd-116">-HostedSubnet</span></span>
<span data-ttu-id="4dddd-117">Подсеть, в которой находится виртуальный маршрутизатор.</span><span class="sxs-lookup"><span data-stu-id="4dddd-117">The subnet where the virtual router is hosted.</span></span>

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

### <span data-ttu-id="4dddd-118">-Location</span><span class="sxs-lookup"><span data-stu-id="4dddd-118">-Location</span></span>
<span data-ttu-id="4dddd-119">Расположение.</span><span class="sxs-lookup"><span data-stu-id="4dddd-119">The location.</span></span>

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

### <span data-ttu-id="4dddd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4dddd-120">-Name</span></span>
<span data-ttu-id="4dddd-121">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="4dddd-121">The name of the virtual router.</span></span>

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

### <span data-ttu-id="4dddd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dddd-122">-ResourceGroupName</span></span>
<span data-ttu-id="4dddd-123">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="4dddd-123">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="4dddd-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="4dddd-124">-Tag</span></span>
<span data-ttu-id="4dddd-125">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="4dddd-125">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="4dddd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dddd-126">-Confirm</span></span>
<span data-ttu-id="4dddd-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4dddd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dddd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dddd-128">-WhatIf</span></span>
<span data-ttu-id="4dddd-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dddd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dddd-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4dddd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dddd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dddd-131">CommonParameters</span></span>
<span data-ttu-id="4dddd-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dddd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dddd-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dddd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dddd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4dddd-134">INPUTS</span></span>

### <span data-ttu-id="4dddd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4dddd-135">System.String</span></span>

### <span data-ttu-id="4dddd-136">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4dddd-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4dddd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4dddd-137">OUTPUTS</span></span>

### <span data-ttu-id="4dddd-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="4dddd-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="4dddd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4dddd-139">NOTES</span></span>

## <span data-ttu-id="4dddd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dddd-140">RELATED LINKS</span></span>
