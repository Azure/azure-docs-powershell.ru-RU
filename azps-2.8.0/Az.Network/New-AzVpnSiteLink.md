---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnsitelink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnSiteLink.md
ms.openlocfilehash: 7e53c6828fa5c7bae40037f2fd64bb06ddf0be45
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902030"
---
# <span data-ttu-id="f770d-101">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f770d-101">New-AzVpnSiteLink</span></span>

## <span data-ttu-id="f770d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f770d-102">SYNOPSIS</span></span>
<span data-ttu-id="f770d-103">Создает объект Azure VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="f770d-103">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="f770d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f770d-104">SYNTAX</span></span>

```
New-AzVpnSiteLink -Name <String> -IPAddress <String> [-LinkProviderName <String>] [-LinkSpeedInMbps <UInt32>]
 [-BGPAsn <UInt32>] [-BGPPeeringAddress <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f770d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f770d-105">DESCRIPTION</span></span>
<span data-ttu-id="f770d-106">Создает объект Azure VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="f770d-106">Creates an Azure VpnSiteLink object.</span></span>

## <span data-ttu-id="f770d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f770d-107">EXAMPLES</span></span>

### <span data-ttu-id="f770d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f770d-108">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSiteLink = New-AzVpnSiteLink -Name "testVpnSiteLink1" -IpAddress "15.25.35.45" -LinkProviderName "SomeTelecomProvider" -LinkSpeedInMbps "10"
PS C:\> $vpnSite = New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -VpnSiteLink @($vpnSiteLink)
```

<span data-ttu-id="f770d-109">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть и VpnSite с 1 VpnSiteLinks "Западная часть США" в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="f770d-109">The above will create a resource group, Virtual WAN and a VpnSite with 1 VpnSiteLinks in West US in "testRG" resource group in Azure.</span></span>

## <span data-ttu-id="f770d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f770d-110">PARAMETERS</span></span>

### <span data-ttu-id="f770d-111">-BGPAsn</span><span class="sxs-lookup"><span data-stu-id="f770d-111">-BGPAsn</span></span>
<span data-ttu-id="f770d-112">BGP ASN для этого VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="f770d-112">The BGP ASN for this VpnSiteLink.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f770d-113">-BGPPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="f770d-113">-BGPPeeringAddress</span></span>
<span data-ttu-id="f770d-114">Адрес пиринга BGP для этого VpnSiteLink.</span><span class="sxs-lookup"><span data-stu-id="f770d-114">The BGP Peering Address for this VpnSiteLink.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f770d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f770d-115">-DefaultProfile</span></span>
<span data-ttu-id="f770d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f770d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f770d-117">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="f770d-117">-IPAddress</span></span>
<span data-ttu-id="f770d-118">IP-адрес следующего прыжка.</span><span class="sxs-lookup"><span data-stu-id="f770d-118">The Next Hop IpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f770d-119">-LinkProviderName</span><span class="sxs-lookup"><span data-stu-id="f770d-119">-LinkProviderName</span></span>
<span data-ttu-id="f770d-120">Имя поставщика ссылок.</span><span class="sxs-lookup"><span data-stu-id="f770d-120">Link Provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f770d-121">-LinkSpeedInMbps</span><span class="sxs-lookup"><span data-stu-id="f770d-121">-LinkSpeedInMbps</span></span>
<span data-ttu-id="f770d-122">Скорость соединения (Мбит/с).</span><span class="sxs-lookup"><span data-stu-id="f770d-122">Link Speed In Mbps.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f770d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f770d-123">-Name</span></span>
<span data-ttu-id="f770d-124">Псевдоним</span><span class="sxs-lookup"><span data-stu-id="f770d-124">Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f770d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f770d-125">CommonParameters</span></span>
<span data-ttu-id="f770d-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f770d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f770d-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f770d-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f770d-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f770d-128">INPUTS</span></span>

### <span data-ttu-id="f770d-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="f770d-129">None</span></span>

## <span data-ttu-id="f770d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f770d-130">OUTPUTS</span></span>

### <span data-ttu-id="f770d-131">Microsoft. Azure. Commands. Network. Models. PSVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="f770d-131">Microsoft.Azure.Commands.Network.Models.PSVpnSiteLink</span></span>

## <span data-ttu-id="f770d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f770d-132">NOTES</span></span>

## <span data-ttu-id="f770d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f770d-133">RELATED LINKS</span></span>

[<span data-ttu-id="f770d-134">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="f770d-134">New-AzVpnSite</span></span>](./New-AzVpnSite.md)