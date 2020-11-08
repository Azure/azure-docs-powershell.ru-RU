---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065837"
---
# <span data-ttu-id="c8674-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8674-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="c8674-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8674-102">SYNOPSIS</span></span>
<span data-ttu-id="c8674-103">Возвращает виртуальную сетевую команду</span><span class="sxs-lookup"><span data-stu-id="c8674-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="c8674-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8674-104">SYNTAX</span></span>

### <span data-ttu-id="c8674-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8674-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8674-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8674-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c8674-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8674-107">DESCRIPTION</span></span>
<span data-ttu-id="c8674-108">Командлет **Get-AzVirtualNetworkTap** получает виртуальную сеть Azure или список участников виртуальной сети Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c8674-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="c8674-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8674-109">EXAMPLES</span></span>

### <span data-ttu-id="c8674-110">Пример 1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="c8674-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="c8674-111">Эта команда возвращает ссылку VirtualNetwork TAP для заданных "VirtualTap1" в "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="c8674-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="c8674-112">Пример 2: получение всех отвода виртуальных сетей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="c8674-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="c8674-113">Эта команда получает все ссылки VirtualNetwork TAP, которые начинаются с "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="c8674-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="c8674-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8674-114">PARAMETERS</span></span>

### <span data-ttu-id="c8674-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8674-115">-DefaultProfile</span></span>
<span data-ttu-id="c8674-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8674-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8674-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c8674-117">-Name</span></span>
<span data-ttu-id="c8674-118">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="c8674-118">The name of the tap.</span></span>

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

### <span data-ttu-id="c8674-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8674-119">-ResourceGroupName</span></span>
<span data-ttu-id="c8674-120">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="c8674-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="c8674-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8674-121">-ResourceId</span></span>
<span data-ttu-id="c8674-122">ResourceId для ресурса VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8674-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="c8674-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8674-123">-Confirm</span></span>
<span data-ttu-id="c8674-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c8674-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8674-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8674-125">-WhatIf</span></span>
<span data-ttu-id="c8674-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c8674-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8674-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c8674-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8674-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8674-128">CommonParameters</span></span>
<span data-ttu-id="c8674-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8674-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8674-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8674-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8674-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8674-131">INPUTS</span></span>

### <span data-ttu-id="c8674-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c8674-132">System.String</span></span>

## <span data-ttu-id="c8674-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8674-133">OUTPUTS</span></span>

### <span data-ttu-id="c8674-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8674-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="c8674-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8674-135">NOTES</span></span>

## <span data-ttu-id="c8674-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8674-136">RELATED LINKS</span></span>

[<span data-ttu-id="c8674-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8674-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="c8674-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8674-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="c8674-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="c8674-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
