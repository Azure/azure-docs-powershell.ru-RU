---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: dc6ca5c41e5f819c8f1db3d0c601b48273e3d78e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245978"
---
# <span data-ttu-id="7efd0-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7efd0-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="7efd0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7efd0-102">SYNOPSIS</span></span>
<span data-ttu-id="7efd0-103">Возвращает виртуальную сетевую команду</span><span class="sxs-lookup"><span data-stu-id="7efd0-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="7efd0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7efd0-104">SYNTAX</span></span>

### <span data-ttu-id="7efd0-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7efd0-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7efd0-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7efd0-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7efd0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7efd0-107">DESCRIPTION</span></span>
<span data-ttu-id="7efd0-108">Командлет **Get-AzVirtualNetworkTap** получает виртуальную сеть Azure или список участников виртуальной сети Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7efd0-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="7efd0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7efd0-109">EXAMPLES</span></span>

### <span data-ttu-id="7efd0-110">Пример 1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="7efd0-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="7efd0-111">Эта команда возвращает ссылку VirtualNetwork TAP для заданных "VirtualTap1" в "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="7efd0-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="7efd0-112">Пример 2: получение всех отвода виртуальных сетей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="7efd0-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="7efd0-113">Эта команда получает все ссылки VirtualNetwork TAP, которые начинаются с "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="7efd0-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="7efd0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7efd0-114">PARAMETERS</span></span>

### <span data-ttu-id="7efd0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7efd0-115">-DefaultProfile</span></span>
<span data-ttu-id="7efd0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7efd0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7efd0-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7efd0-117">-Name</span></span>
<span data-ttu-id="7efd0-118">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="7efd0-118">The name of the tap.</span></span>

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

### <span data-ttu-id="7efd0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7efd0-119">-ResourceGroupName</span></span>
<span data-ttu-id="7efd0-120">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="7efd0-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="7efd0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7efd0-121">-ResourceId</span></span>
<span data-ttu-id="7efd0-122">ResourceId для ресурса VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7efd0-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="7efd0-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7efd0-123">-Confirm</span></span>
<span data-ttu-id="7efd0-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7efd0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7efd0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7efd0-125">-WhatIf</span></span>
<span data-ttu-id="7efd0-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7efd0-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7efd0-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7efd0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7efd0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7efd0-128">CommonParameters</span></span>
<span data-ttu-id="7efd0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7efd0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7efd0-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7efd0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7efd0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7efd0-131">INPUTS</span></span>

### <span data-ttu-id="7efd0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7efd0-132">System.String</span></span>

## <span data-ttu-id="7efd0-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7efd0-133">OUTPUTS</span></span>

### <span data-ttu-id="7efd0-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7efd0-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="7efd0-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="7efd0-135">NOTES</span></span>

## <span data-ttu-id="7efd0-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7efd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="7efd0-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7efd0-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="7efd0-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7efd0-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="7efd0-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7efd0-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)