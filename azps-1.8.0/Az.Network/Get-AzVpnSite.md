---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: aad8b9c253dadfa199a16e3cf0a996c430b3b7d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730444"
---
# <span data-ttu-id="ab22b-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab22b-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="ab22b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ab22b-102">SYNOPSIS</span></span>
<span data-ttu-id="ab22b-103">Получает ресурс Azure VpnSite по имени или перечисление всех VpnSites в ResourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="ab22b-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="ab22b-104">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="ab22b-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="ab22b-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ab22b-105">SYNTAX</span></span>

### <span data-ttu-id="ab22b-106">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ab22b-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab22b-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab22b-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab22b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab22b-108">DESCRIPTION</span></span>
<span data-ttu-id="ab22b-109">Получает ресурс Azure VpnSite по имени или перечисление всех VpnSites в ResourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="ab22b-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="ab22b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ab22b-110">EXAMPLES</span></span>

### <span data-ttu-id="ab22b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ab22b-111">Example 1</span></span>

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

<span data-ttu-id="ab22b-112">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="ab22b-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="ab22b-113">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="ab22b-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="ab22b-114">После создания сайта он получает сайт с помощью команды Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="ab22b-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="ab22b-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ab22b-115">Example 2</span></span>

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

<span data-ttu-id="ab22b-116">Этот командлет получает все сайты, которые начинаются с "Test".</span><span class="sxs-lookup"><span data-stu-id="ab22b-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="ab22b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ab22b-117">PARAMETERS</span></span>

### <span data-ttu-id="ab22b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab22b-118">-DefaultProfile</span></span>
<span data-ttu-id="ab22b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ab22b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab22b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ab22b-120">-Name</span></span>
<span data-ttu-id="ab22b-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab22b-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ab22b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab22b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ab22b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab22b-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ab22b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab22b-124">CommonParameters</span></span>
<span data-ttu-id="ab22b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ab22b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab22b-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab22b-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab22b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ab22b-127">INPUTS</span></span>

### <span data-ttu-id="ab22b-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="ab22b-128">None</span></span>

## <span data-ttu-id="ab22b-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ab22b-129">OUTPUTS</span></span>

### <span data-ttu-id="ab22b-130">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab22b-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="ab22b-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ab22b-131">NOTES</span></span>

## <span data-ttu-id="ab22b-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ab22b-132">RELATED LINKS</span></span>

[<span data-ttu-id="ab22b-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab22b-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="ab22b-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab22b-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="ab22b-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="ab22b-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
