---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235512"
---
# <span data-ttu-id="fcbf0-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fcbf0-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="fcbf0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fcbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="fcbf0-103">Возвращает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fcbf0-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="fcbf0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fcbf0-104">SYNTAX</span></span>

### <span data-ttu-id="fcbf0-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="fcbf0-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fcbf0-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="fcbf0-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fcbf0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcbf0-107">DESCRIPTION</span></span>
<span data-ttu-id="fcbf0-108">Командлет **Get-AzVirtualNetwork** получает одну или несколько виртуальных сетей n группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fcbf0-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="fcbf0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fcbf0-109">EXAMPLES</span></span>

### <span data-ttu-id="fcbf0-110">1: получение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="fcbf0-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="fcbf0-111">Эта команда возвращает виртуальную сеть с именем MyVirtualNetwork в группе ресурсов TestResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fcbf0-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="fcbf0-112">2: список виртуальных сетей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="fcbf0-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="fcbf0-113">Эта команда получает все виртуальные сети, которые начинаются с "MyVirtualNetwork".</span><span class="sxs-lookup"><span data-stu-id="fcbf0-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="fcbf0-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fcbf0-114">PARAMETERS</span></span>

### <span data-ttu-id="fcbf0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcbf0-115">-DefaultProfile</span></span>
<span data-ttu-id="fcbf0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcbf0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcbf0-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="fcbf0-117">-ExpandResource</span></span>
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

### <span data-ttu-id="fcbf0-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fcbf0-118">-Name</span></span>
<span data-ttu-id="fcbf0-119">Указывает имя виртуальной сети, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fcbf0-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="fcbf0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcbf0-120">-ResourceGroupName</span></span>
<span data-ttu-id="fcbf0-121">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="fcbf0-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="fcbf0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcbf0-122">CommonParameters</span></span>
<span data-ttu-id="fcbf0-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fcbf0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcbf0-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcbf0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcbf0-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fcbf0-125">INPUTS</span></span>

### <span data-ttu-id="fcbf0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fcbf0-126">System.String</span></span>

## <span data-ttu-id="fcbf0-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcbf0-127">OUTPUTS</span></span>

### <span data-ttu-id="fcbf0-128">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fcbf0-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="fcbf0-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fcbf0-129">NOTES</span></span>

## <span data-ttu-id="fcbf0-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcbf0-130">RELATED LINKS</span></span>

[<span data-ttu-id="fcbf0-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fcbf0-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fcbf0-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fcbf0-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="fcbf0-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fcbf0-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


