---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987804"
---
# <span data-ttu-id="143ba-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="143ba-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="143ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="143ba-102">SYNOPSIS</span></span>
<span data-ttu-id="143ba-103">Этот командлет возвращает список поддерживаемых марок VPN-устройств, моделей и версий микропрограмм.</span><span class="sxs-lookup"><span data-stu-id="143ba-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="143ba-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="143ba-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="143ba-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="143ba-105">DESCRIPTION</span></span>
<span data-ttu-id="143ba-106">Этот командлет возвращает список поддерживаемых марок VPN-устройств, моделей и версий микропрограмм.</span><span class="sxs-lookup"><span data-stu-id="143ba-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="143ba-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="143ba-107">EXAMPLES</span></span>

### <span data-ttu-id="143ba-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="143ba-108">Example 1</span></span>
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

<span data-ttu-id="143ba-109">Возвращает список поддерживаемых марок VPN-устройств, моделей и версий ПО:</span><span class="sxs-lookup"><span data-stu-id="143ba-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="143ba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="143ba-110">PARAMETERS</span></span>

### <span data-ttu-id="143ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="143ba-111">-DefaultProfile</span></span>
<span data-ttu-id="143ba-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="143ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="143ba-113">-Name</span><span class="sxs-lookup"><span data-stu-id="143ba-113">-Name</span></span>
<span data-ttu-id="143ba-114">Имя виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="143ba-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="143ba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="143ba-115">-ResourceGroupName</span></span>
<span data-ttu-id="143ba-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="143ba-116">The resource group name.</span></span>

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

### <span data-ttu-id="143ba-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="143ba-117">CommonParameters</span></span>
<span data-ttu-id="143ba-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="143ba-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="143ba-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="143ba-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="143ba-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="143ba-120">INPUTS</span></span>

### <span data-ttu-id="143ba-121">System.String</span><span class="sxs-lookup"><span data-stu-id="143ba-121">System.String</span></span>

## <span data-ttu-id="143ba-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="143ba-122">OUTPUTS</span></span>

### <span data-ttu-id="143ba-123">System.String</span><span class="sxs-lookup"><span data-stu-id="143ba-123">System.String</span></span>

## <span data-ttu-id="143ba-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="143ba-124">NOTES</span></span>

## <span data-ttu-id="143ba-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="143ba-125">RELATED LINKS</span></span>
