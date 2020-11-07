---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkTap.md
ms.openlocfilehash: df4da43c1a8edf0c3c887e4acdd009593984c048
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902290"
---
# <span data-ttu-id="2369b-101">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2369b-101">Get-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="2369b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2369b-102">SYNOPSIS</span></span>
<span data-ttu-id="2369b-103">Возвращает виртуальную сетевую команду</span><span class="sxs-lookup"><span data-stu-id="2369b-103">Gets a virtual network tap</span></span>

## <span data-ttu-id="2369b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2369b-104">SYNTAX</span></span>

### <span data-ttu-id="2369b-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2369b-105">ListParameterSet (Default)</span></span>
```
Get-AzVirtualNetworkTap [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2369b-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2369b-106">GetByResourceIdParameterSet</span></span>
```
Get-AzVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2369b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2369b-107">DESCRIPTION</span></span>
<span data-ttu-id="2369b-108">Командлет **Get-AzVirtualNetworkTap** получает виртуальную сеть Azure или список участников виртуальной сети Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2369b-108">The **Get-AzVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="2369b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2369b-109">EXAMPLES</span></span>

### <span data-ttu-id="2369b-110">Пример 1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2369b-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="2369b-111">Эта команда возвращает ссылку VirtualNetwork TAP для заданных "VirtualTap1" в "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="2369b-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

### <span data-ttu-id="2369b-112">Пример 2: получение всех отвода виртуальных сетей с помощью фильтрации</span><span class="sxs-lookup"><span data-stu-id="2369b-112">Example 2: Get all virtual network taps using filtering</span></span>
```
PS C:\> Get-AzVirtualNetworkTap -Name "VirtualTap*"
```

<span data-ttu-id="2369b-113">Эта команда получает все ссылки VirtualNetwork TAP, которые начинаются с "VirtualTap".</span><span class="sxs-lookup"><span data-stu-id="2369b-113">This command gets all VirtualNetwork tap references that start with "VirtualTap".</span></span>

## <span data-ttu-id="2369b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2369b-114">PARAMETERS</span></span>

### <span data-ttu-id="2369b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2369b-115">-DefaultProfile</span></span>
<span data-ttu-id="2369b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2369b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2369b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2369b-117">-Name</span></span>
<span data-ttu-id="2369b-118">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="2369b-118">The name of the tap.</span></span>

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

### <span data-ttu-id="2369b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2369b-119">-ResourceGroupName</span></span>
<span data-ttu-id="2369b-120">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="2369b-120">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="2369b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2369b-121">-ResourceId</span></span>
<span data-ttu-id="2369b-122">ResourceId для ресурса VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2369b-122">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="2369b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2369b-123">-Confirm</span></span>
<span data-ttu-id="2369b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2369b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2369b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2369b-125">-WhatIf</span></span>
<span data-ttu-id="2369b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2369b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2369b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2369b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2369b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2369b-128">CommonParameters</span></span>
<span data-ttu-id="2369b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2369b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2369b-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2369b-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2369b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2369b-131">INPUTS</span></span>

### <span data-ttu-id="2369b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2369b-132">System.String</span></span>

## <span data-ttu-id="2369b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2369b-133">OUTPUTS</span></span>

### <span data-ttu-id="2369b-134">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2369b-134">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="2369b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2369b-135">NOTES</span></span>

## <span data-ttu-id="2369b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2369b-136">RELATED LINKS</span></span>

[<span data-ttu-id="2369b-137">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2369b-137">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="2369b-138">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2369b-138">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)

[<span data-ttu-id="2369b-139">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="2369b-139">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
