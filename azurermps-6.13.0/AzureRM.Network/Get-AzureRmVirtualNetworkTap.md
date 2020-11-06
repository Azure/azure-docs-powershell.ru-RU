---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: ff9ed8220cf2b30f2e652e207cb4d63db969a8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562940"
---
# <span data-ttu-id="b31aa-101">Get-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b31aa-101">Get-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="b31aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b31aa-102">SYNOPSIS</span></span>
<span data-ttu-id="b31aa-103">Возвращает виртуальную сетевую команду</span><span class="sxs-lookup"><span data-stu-id="b31aa-103">Gets a virtual network tap</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b31aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b31aa-104">SYNTAX</span></span>

### <span data-ttu-id="b31aa-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b31aa-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b31aa-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b31aa-106">GetByResourceIdParameterSet</span></span>
```
Get-AzureRmVirtualNetworkTap -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b31aa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b31aa-107">DESCRIPTION</span></span>
<span data-ttu-id="b31aa-108">Командлет **Get-AzureRmVirtualNetworkTap** получает виртуальную сеть Azure или список участников виртуальной сети Azure в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b31aa-108">The **Get-AzureRmVirtualNetworkTap** cmdlet gets an Azure virtual network tap or a list of Azure virtual network taps in a resource group.</span></span>

## <span data-ttu-id="b31aa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b31aa-109">EXAMPLES</span></span>

### <span data-ttu-id="b31aa-110">Пример 1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="b31aa-110">Example 1: Get a virtual network tap</span></span>
```
PS C:\>Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
```

<span data-ttu-id="b31aa-111">Эта команда возвращает ссылку VirtualNetwork TAP для заданных "VirtualTap1" в "ResourceGroup1".</span><span class="sxs-lookup"><span data-stu-id="b31aa-111">This command gets a VirtualNetwork tap reference for given "VirtualTap1" in "ResourceGroup1".</span></span>

## <span data-ttu-id="b31aa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b31aa-112">PARAMETERS</span></span>

### <span data-ttu-id="b31aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b31aa-113">-DefaultProfile</span></span>
<span data-ttu-id="b31aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b31aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b31aa-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b31aa-115">-Name</span></span>
<span data-ttu-id="b31aa-116">Имя TAP.</span><span class="sxs-lookup"><span data-stu-id="b31aa-116">The name of the tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b31aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="b31aa-118">Имя группы ресурсов, в которой будет нажата виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="b31aa-118">The resource group name of the virtual network tap.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b31aa-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b31aa-119">-ResourceId</span></span>
<span data-ttu-id="b31aa-120">ResourceId для ресурса VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b31aa-120">ResourceId of the VirtualNetworkTap resource</span></span>

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

### <span data-ttu-id="b31aa-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b31aa-121">-Confirm</span></span>
<span data-ttu-id="b31aa-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b31aa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b31aa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b31aa-123">-WhatIf</span></span>
<span data-ttu-id="b31aa-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b31aa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b31aa-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b31aa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b31aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b31aa-126">CommonParameters</span></span>
<span data-ttu-id="b31aa-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b31aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b31aa-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b31aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b31aa-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b31aa-129">INPUTS</span></span>

### <span data-ttu-id="b31aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="b31aa-130">System.String</span></span>

## <span data-ttu-id="b31aa-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b31aa-131">OUTPUTS</span></span>

### <span data-ttu-id="b31aa-132">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="b31aa-132">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="b31aa-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b31aa-133">NOTES</span></span>

## <span data-ttu-id="b31aa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b31aa-134">RELATED LINKS</span></span>
