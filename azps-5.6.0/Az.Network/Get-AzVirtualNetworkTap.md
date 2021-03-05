---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: 154cededf20ceb88fdbc851b96189282e1b6123a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003592"
---
# <span data-ttu-id="67a1a-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="67a1a-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="67a1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="67a1a-103">Получает виртуальное сетевое касание</span><span class="sxs-lookup"><span data-stu-id="67a1a-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="67a1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67a1a-104">SYNTAX</span></span>

### <span data-ttu-id="67a1a-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="67a1a-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67a1a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="67a1a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67a1a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67a1a-107">DESCRIPTION</span></span>
<span data-ttu-id="67a1a-108">Командлет **Get-AzVirtualNetworkTap** получает виртуальный сетевой касание Azure или список виртуальных сетей Azure, которые коснитесь группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="67a1a-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="67a1a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67a1a-109">EXAMPLES</span></span>

### <span data-ttu-id="67a1a-110">Пример 1. Виртуальный сетевой касание</span><span class="sxs-lookup"><span data-stu-id="67a1a-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="67a1a-111">Эта команда получает ссылку на tap VirtualNetwork для данного "VirtualTap1" в "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="67a1a-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="67a1a-112">Пример 2. Все виртуальные сетевые касания с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="67a1a-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="67a1a-113">Эта команда получает все ссылки на темы VirtualNetwork, которые начинаются с VirtualTap.</span><span class="sxs-lookup"><span data-stu-id="67a1a-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="67a1a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67a1a-114">PARAMETERS</span></span>

### <span data-ttu-id="67a1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a1a-115">-DefaultProfile</span></span>
<span data-ttu-id="67a1a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67a1a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67a1a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="67a1a-117">-Name</span></span>
<span data-ttu-id="67a1a-118">Имя касания.</span><span class="sxs-lookup"><span data-stu-id="67a1a-118">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="67a1a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a1a-119">-ResourceGroupName</span></span>
<span data-ttu-id="67a1a-120">Имя группы ресурсов виртуального сетевого касания.</span><span class="sxs-lookup"><span data-stu-id="67a1a-120">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="67a1a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67a1a-121">-ResourceId</span></span>
<span data-ttu-id="67a1a-122">ResourceId ресурса VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="67a1a-122">ResourceId of the VirtualNetworkTap resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a1a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67a1a-123">-Confirm</span></span>
<span data-ttu-id="67a1a-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="67a1a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a1a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a1a-125">-WhatIf</span></span>
<span data-ttu-id="67a1a-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67a1a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67a1a-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="67a1a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a1a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a1a-128">CommonParameters</span></span>
<span data-ttu-id="67a1a-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a1a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a1a-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67a1a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a1a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67a1a-131">INPUTS</span></span>

### <span data-ttu-id="67a1a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="67a1a-132">System.String</span></span>

## <span data-ttu-id="67a1a-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67a1a-133">OUTPUTS</span></span>

### <span data-ttu-id="67a1a-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="67a1a-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="67a1a-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67a1a-135">NOTES</span></span>

## <span data-ttu-id="67a1a-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67a1a-136">RELATED LINKS</span></span>

[<span data-ttu-id="67a1a-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="67a1a-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="67a1a-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="67a1a-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="67a1a-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="67a1a-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
