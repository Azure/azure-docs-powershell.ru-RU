---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218628"
---
# <span data-ttu-id="b9d42-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b9d42-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="b9d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9d42-102">SYNOPSIS</span></span>
<span data-ttu-id="b9d42-103">Получает ресурс Azure VpnSite по имени ИЛИ перечисляет все VPNSites в resourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="b9d42-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="b9d42-104">Это представление RM для ветвей клиентов, которые загружаются в Azure для подключения к S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="b9d42-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="b9d42-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9d42-105">SYNTAX</span></span>

### <span data-ttu-id="b9d42-106">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9d42-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9d42-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9d42-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b9d42-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9d42-108">DESCRIPTION</span></span>
<span data-ttu-id="b9d42-109">Получает ресурс Azure VpnSite по имени ИЛИ перечисляет все VPNSites в resourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="b9d42-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="b9d42-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9d42-110">EXAMPLES</span></span>

### <span data-ttu-id="b9d42-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9d42-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="b9d42-112">Выше будет создаваться группа ресурсов Virtual WAN в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="b9d42-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="b9d42-113">Затем создается VPNSite, представляют ветвь клиента и связывает его с виртуальной сетью WAN.</span><span class="sxs-lookup"><span data-stu-id="b9d42-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="b9d42-114">Созданный сайт будет создан с помощью команды "Get-AzVpnSite".</span><span class="sxs-lookup"><span data-stu-id="b9d42-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="b9d42-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b9d42-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="b9d42-116">Этот cmdlet возвращает все сайты, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="b9d42-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="b9d42-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9d42-117">PARAMETERS</span></span>

### <span data-ttu-id="b9d42-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9d42-118">-DefaultProfile</span></span>
<span data-ttu-id="b9d42-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9d42-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9d42-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b9d42-120">-Name</span></span>
<span data-ttu-id="b9d42-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="b9d42-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d42-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9d42-122">-ResourceGroupName</span></span>
<span data-ttu-id="b9d42-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9d42-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9d42-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9d42-124">CommonParameters</span></span>
<span data-ttu-id="b9d42-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9d42-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9d42-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9d42-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9d42-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9d42-127">INPUTS</span></span>

### <span data-ttu-id="b9d42-128">Нет</span><span class="sxs-lookup"><span data-stu-id="b9d42-128">None</span></span>

## <span data-ttu-id="b9d42-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9d42-129">OUTPUTS</span></span>

### <span data-ttu-id="b9d42-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="b9d42-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="b9d42-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9d42-131">NOTES</span></span>

## <span data-ttu-id="b9d42-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9d42-132">RELATED LINKS</span></span>

[<span data-ttu-id="b9d42-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b9d42-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="b9d42-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b9d42-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="b9d42-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b9d42-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
