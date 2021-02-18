---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218689"
---
# <span data-ttu-id="25492-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="25492-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="25492-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25492-102">SYNOPSIS</span></span>
<span data-ttu-id="25492-103">Получает виртуальное сетевое касание</span><span class="sxs-lookup"><span data-stu-id="25492-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="25492-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25492-104">SYNTAX</span></span>

### <span data-ttu-id="25492-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="25492-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25492-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25492-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25492-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25492-107">DESCRIPTION</span></span>
<span data-ttu-id="25492-108">Командлет **Get-AzVirtualNetworkTap** получает виртуальный сетевой касание Azure или список виртуальных сетей Azure, которые коснитесь группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="25492-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="25492-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25492-109">EXAMPLES</span></span>

### <span data-ttu-id="25492-110">Пример 1. Виртуальный сетевой касание</span><span class="sxs-lookup"><span data-stu-id="25492-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="25492-111">Эта команда получает ссылку на tap VirtualNetwork для данного "VirtualTap1" в "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="25492-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="25492-112">Пример 2. Все виртуальные сетевые касания с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="25492-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="25492-113">Эта команда получает все ссылки на virtualNetwork, которые начинаются с VirtualTap.</span><span class="sxs-lookup"><span data-stu-id="25492-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="25492-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25492-114">PARAMETERS</span></span>

### <span data-ttu-id="25492-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25492-115">-DefaultProfile</span></span>
<span data-ttu-id="25492-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25492-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25492-117">-Name</span><span class="sxs-lookup"><span data-stu-id="25492-117">-Name</span></span>
<span data-ttu-id="25492-118">Имя касания.</span><span class="sxs-lookup"><span data-stu-id="25492-118">The name of the tap.</span></span>

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

### <span data-ttu-id="25492-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25492-119">-ResourceGroupName</span></span>
<span data-ttu-id="25492-120">Имя группы ресурсов виртуального сетевого касания.</span><span class="sxs-lookup"><span data-stu-id="25492-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="25492-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25492-121">-ResourceId</span></span>
<span data-ttu-id="25492-122">ResourceId ресурса VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="25492-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="25492-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25492-123">-Confirm</span></span>
<span data-ttu-id="25492-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="25492-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25492-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25492-125">-WhatIf</span></span>
<span data-ttu-id="25492-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25492-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25492-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="25492-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25492-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25492-128">CommonParameters</span></span>
<span data-ttu-id="25492-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25492-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25492-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25492-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25492-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25492-131">INPUTS</span></span>

### <span data-ttu-id="25492-132">System.String</span><span class="sxs-lookup"><span data-stu-id="25492-132">System.String</span></span>

## <span data-ttu-id="25492-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25492-133">OUTPUTS</span></span>

### <span data-ttu-id="25492-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="25492-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="25492-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25492-135">NOTES</span></span>

## <span data-ttu-id="25492-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25492-136">RELATED LINKS</span></span>

[<span data-ttu-id="25492-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="25492-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="25492-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="25492-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="25492-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="25492-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
