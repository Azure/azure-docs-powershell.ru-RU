---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: ff2e1a820a2a1cc664969c1872aebe6b88fc415b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518793"
---
# <span data-ttu-id="4bae0-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bae0-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="4bae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bae0-102">SYNOPSIS</span></span>
<span data-ttu-id="4bae0-103">Получает виртуальную сеть в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4bae0-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="4bae0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4bae0-104">SYNTAX</span></span>

### <span data-ttu-id="4bae0-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="4bae0-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bae0-106">Развернуть</span><span class="sxs-lookup"><span data-stu-id="4bae0-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bae0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bae0-107">DESCRIPTION</span></span>
<span data-ttu-id="4bae0-108">Командлет **Get-AzVirtualNetwork** получает одну или несколько виртуальных сетей в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4bae0-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="4bae0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4bae0-109">EXAMPLES</span></span>

### <span data-ttu-id="4bae0-110">1. Извлечение виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="4bae0-110">1: Retrieve a virtual network</span></span>
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

<span data-ttu-id="4bae0-111">Эта команда получает виртуальную сеть MyVirtualNetwork в группе ресурсов TestResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4bae0-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

### <span data-ttu-id="4bae0-112">2. Список виртуальных сетей с помощью фильтра</span><span class="sxs-lookup"><span data-stu-id="4bae0-112">2: List virtual networks using filter</span></span>
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

<span data-ttu-id="4bae0-113">Эта команда возвращает все виртуальные сети, которые начинаются с MyVirtualNetwork.</span><span class="sxs-lookup"><span data-stu-id="4bae0-113">This command gets all virtual networks that start with "MyVirtualNetwork".</span></span>

## <span data-ttu-id="4bae0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bae0-114">PARAMETERS</span></span>

### <span data-ttu-id="4bae0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bae0-115">-DefaultProfile</span></span>
<span data-ttu-id="4bae0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bae0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bae0-117">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="4bae0-117">-ExpandResource</span></span>
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

### <span data-ttu-id="4bae0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4bae0-118">-Name</span></span>
<span data-ttu-id="4bae0-119">Определяет имя виртуальной сети, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4bae0-119">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4bae0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bae0-120">-ResourceGroupName</span></span>
<span data-ttu-id="4bae0-121">Имя группы ресурсов, к которой относится виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="4bae0-121">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="4bae0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bae0-122">CommonParameters</span></span>
<span data-ttu-id="4bae0-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bae0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bae0-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bae0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bae0-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bae0-125">INPUTS</span></span>

### <span data-ttu-id="4bae0-126">System.String</span><span class="sxs-lookup"><span data-stu-id="4bae0-126">System.String</span></span>

## <span data-ttu-id="4bae0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4bae0-127">OUTPUTS</span></span>

### <span data-ttu-id="4bae0-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bae0-128">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="4bae0-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4bae0-129">NOTES</span></span>

## <span data-ttu-id="4bae0-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bae0-130">RELATED LINKS</span></span>

[<span data-ttu-id="4bae0-131">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bae0-131">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="4bae0-132">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bae0-132">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="4bae0-133">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4bae0-133">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


