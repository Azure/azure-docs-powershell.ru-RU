---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562903"
---
# <span data-ttu-id="55e20-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="55e20-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="55e20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55e20-102">SYNOPSIS</span></span>
<span data-ttu-id="55e20-103">Получает ресурс Azure VpnSite по имени или перечисление всех VpnSites в ResourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="55e20-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="55e20-104">Это представление RM для ветвей клиентов, которые отправляются в подключение к Azure для S2S с помощью виртуального концентратора Cortex.</span><span class="sxs-lookup"><span data-stu-id="55e20-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e20-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55e20-105">SYNTAX</span></span>

### <span data-ttu-id="55e20-106">ListBySubscriptionId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55e20-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e20-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e20-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="55e20-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e20-108">DESCRIPTION</span></span>
<span data-ttu-id="55e20-109">Получает ресурс Azure VpnSite по имени или перечисление всех VpnSites в ResourceGroup или SubscriptionId.</span><span class="sxs-lookup"><span data-stu-id="55e20-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="55e20-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55e20-110">EXAMPLES</span></span>

### <span data-ttu-id="55e20-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55e20-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="55e20-112">В приведенном выше примере будет создана группа ресурсов, Виртуальная глобальная сеть в Запад США в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="55e20-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="55e20-113">Затем он создает VpnSite для представления ветви клиента и связывает ее с виртуальной глобальной сетью.</span><span class="sxs-lookup"><span data-stu-id="55e20-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="55e20-114">После создания сайта он получает сайт с помощью команды Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="55e20-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="55e20-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55e20-115">PARAMETERS</span></span>

### <span data-ttu-id="55e20-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e20-116">-DefaultProfile</span></span>
<span data-ttu-id="55e20-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55e20-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55e20-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55e20-118">-Name</span></span>
<span data-ttu-id="55e20-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="55e20-119">The resource name.</span></span>

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

### <span data-ttu-id="55e20-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e20-120">-ResourceGroupName</span></span>
<span data-ttu-id="55e20-121">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="55e20-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e20-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e20-122">CommonParameters</span></span>
<span data-ttu-id="55e20-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55e20-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e20-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e20-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e20-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55e20-125">INPUTS</span></span>

### <span data-ttu-id="55e20-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="55e20-126">None</span></span>

## <span data-ttu-id="55e20-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e20-127">OUTPUTS</span></span>

### <span data-ttu-id="55e20-128">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="55e20-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="55e20-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="55e20-129">NOTES</span></span>

## <span data-ttu-id="55e20-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55e20-130">RELATED LINKS</span></span>
