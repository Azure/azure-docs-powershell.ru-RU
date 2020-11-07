---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: da0dde546d5875c1a29bd02805f40c7f12a68188
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902845"
---
# <span data-ttu-id="cba0c-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cba0c-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="cba0c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cba0c-102">SYNOPSIS</span></span>
<span data-ttu-id="cba0c-103">Возвращает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cba0c-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="cba0c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cba0c-104">SYNTAX</span></span>

### <span data-ttu-id="cba0c-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="cba0c-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cba0c-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="cba0c-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cba0c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba0c-107">DESCRIPTION</span></span>
<span data-ttu-id="cba0c-108">Командлет **Get-AzVirtualNetwork** получает одну или несколько виртуальных сетей n группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cba0c-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="cba0c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cba0c-109">EXAMPLES</span></span>

### <span data-ttu-id="cba0c-110">1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="cba0c-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="cba0c-111">Эта команда возвращает виртуальную сеть с именем MyVirtualNetwork в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cba0c-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="cba0c-112">2: список виртуальных сетей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="cba0c-112">2: List virtual networks using filter</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork*

Name                   : MyVirtualNetwork1
ResourceGroupName      : TestResourceGroup
Location               : eastus
Id                     : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup
                         /providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork1
Etag                   : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid           : 00000000-0000-0000-0000-000000000000
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "xx.x.x.x/x"
                           ]
                         }
DhcpOptions            : {}
Subnets                : []
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
```

<span data-ttu-id="cba0c-113">Эта команда получает все виртуальные сети, которые начинаются с "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="cba0c-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="cba0c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cba0c-114">PARAMETERS</span></span>

### <span data-ttu-id="cba0c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba0c-115">-DefaultProfile</span></span>
<span data-ttu-id="cba0c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cba0c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba0c-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cba0c-117">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cba0c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cba0c-118">-Name</span></span>
<span data-ttu-id="cba0c-119">Указывает имя виртуальной сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cba0c-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cba0c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba0c-120">-ResourceGroupName</span></span>
<span data-ttu-id="cba0c-121">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="cba0c-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="cba0c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba0c-122">CommonParameters</span></span>
<span data-ttu-id="cba0c-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cba0c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba0c-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cba0c-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba0c-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cba0c-125">INPUTS</span></span>

### <span data-ttu-id="cba0c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="cba0c-126">System.String</span></span>

## <span data-ttu-id="cba0c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba0c-127">OUTPUTS</span></span>

### <span data-ttu-id="cba0c-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cba0c-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cba0c-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="cba0c-129">NOTES</span></span>

## <span data-ttu-id="cba0c-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cba0c-130">RELATED LINKS</span></span>

[<span data-ttu-id="cba0c-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cba0c-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="cba0c-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cba0c-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="cba0c-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cba0c-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


