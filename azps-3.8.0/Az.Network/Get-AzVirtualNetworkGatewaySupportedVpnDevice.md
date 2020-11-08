---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066135"
---
# <span data-ttu-id="014f5-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="014f5-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="014f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="014f5-102">SYNOPSIS</span></span>
<span data-ttu-id="014f5-103">Этот unifiedgroup возвращает список поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="014f5-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="014f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="014f5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="014f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="014f5-105">DESCRIPTION</span></span>
<span data-ttu-id="014f5-106">Этот unifiedgroup возвращает список поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="014f5-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="014f5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="014f5-107">EXAMPLES</span></span>

### <span data-ttu-id="014f5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="014f5-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="014f5-109">Возвращает список поддерживаемых торговых марок устройств VPN, моделей и версий микропрограмм:</span><span class="sxs-lookup"><span data-stu-id="014f5-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="014f5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="014f5-110">PARAMETERS</span></span>

### <span data-ttu-id="014f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014f5-111">-DefaultProfile</span></span>
<span data-ttu-id="014f5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="014f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="014f5-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="014f5-113">-Name</span></span>
<span data-ttu-id="014f5-114">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="014f5-114">The virtual network gateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014f5-115">-ResourceGroupName</span></span>
<span data-ttu-id="014f5-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="014f5-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="014f5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014f5-117">CommonParameters</span></span>
<span data-ttu-id="014f5-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="014f5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014f5-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="014f5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014f5-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="014f5-120">INPUTS</span></span>

### <span data-ttu-id="014f5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="014f5-121">System.String</span></span>

## <span data-ttu-id="014f5-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="014f5-122">OUTPUTS</span></span>

### <span data-ttu-id="014f5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="014f5-123">System.String</span></span>

## <span data-ttu-id="014f5-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="014f5-124">NOTES</span></span>

## <span data-ttu-id="014f5-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="014f5-125">RELATED LINKS</span></span>
