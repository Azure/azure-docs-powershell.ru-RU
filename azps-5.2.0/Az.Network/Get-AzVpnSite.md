---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414188"
---
# <span data-ttu-id="95401-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95401-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="95401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95401-102">SYNOPSIS</span></span>
<span data-ttu-id="95401-103">Получает ресурс VpnSite Azure по имени ИЛИ перечисляет все VPNSites в resourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="95401-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="95401-104">Это представление RM для ветвей клиентов, которые загружаются в Azure для подключения к S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="95401-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="95401-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95401-105">SYNTAX</span></span>

### <span data-ttu-id="95401-106">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95401-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95401-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95401-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95401-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95401-108">DESCRIPTION</span></span>
<span data-ttu-id="95401-109">Получает ресурс VpnSite Azure по имени ИЛИ перечисляет все VPNSites в resourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="95401-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="95401-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95401-110">EXAMPLES</span></span>

### <span data-ttu-id="95401-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95401-111">Example 1</span></span>

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

<span data-ttu-id="95401-112">Выше будет создаться группа ресурсов Virtual WAN в западной части США в группе ресурсов testRG в Azure.</span><span class="sxs-lookup"><span data-stu-id="95401-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="95401-113">Затем создается VPNSite, представляют ветвь клиента и связывает его с виртуальной сетью WAN.</span><span class="sxs-lookup"><span data-stu-id="95401-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="95401-114">Созданный сайт будет создан с помощью команды "Get-AzVpnSite".</span><span class="sxs-lookup"><span data-stu-id="95401-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="95401-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="95401-115">Example 2</span></span>

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

<span data-ttu-id="95401-116">Этот cmdlet возвращает все сайты, которые начинаются с "test".</span><span class="sxs-lookup"><span data-stu-id="95401-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="95401-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95401-117">PARAMETERS</span></span>

### <span data-ttu-id="95401-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95401-118">-DefaultProfile</span></span>
<span data-ttu-id="95401-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95401-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95401-120">-Name</span><span class="sxs-lookup"><span data-stu-id="95401-120">-Name</span></span>
<span data-ttu-id="95401-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="95401-121">The resource name.</span></span>

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

### <span data-ttu-id="95401-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95401-122">-ResourceGroupName</span></span>
<span data-ttu-id="95401-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95401-123">The resource group name.</span></span>

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

### <span data-ttu-id="95401-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95401-124">CommonParameters</span></span>
<span data-ttu-id="95401-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95401-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95401-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95401-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95401-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95401-127">INPUTS</span></span>

### <span data-ttu-id="95401-128">Нет</span><span class="sxs-lookup"><span data-stu-id="95401-128">None</span></span>

## <span data-ttu-id="95401-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95401-129">OUTPUTS</span></span>

### <span data-ttu-id="95401-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="95401-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="95401-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95401-131">NOTES</span></span>

## <span data-ttu-id="95401-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95401-132">RELATED LINKS</span></span>

[<span data-ttu-id="95401-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95401-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="95401-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95401-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="95401-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="95401-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
