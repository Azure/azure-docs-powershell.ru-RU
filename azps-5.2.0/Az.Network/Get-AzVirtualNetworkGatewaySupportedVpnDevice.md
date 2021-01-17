---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418047"
---
# <span data-ttu-id="ae737-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="ae737-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="ae737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae737-102">SYNOPSIS</span></span>
<span data-ttu-id="ae737-103">Этот командлет возвращает список поддерживаемых марок VPN-устройств, моделей и версий микропрограмм.</span><span class="sxs-lookup"><span data-stu-id="ae737-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="ae737-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae737-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae737-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae737-105">DESCRIPTION</span></span>
<span data-ttu-id="ae737-106">Этот командлет возвращает список поддерживаемых марок VPN-устройств, моделей и версий микропрограмм.</span><span class="sxs-lookup"><span data-stu-id="ae737-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="ae737-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae737-107">EXAMPLES</span></span>

### <span data-ttu-id="ae737-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae737-108">Example 1</span></span>
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

<span data-ttu-id="ae737-109">Возвращает список поддерживаемых марок VPN-устройств, моделей и версий программы:</span><span class="sxs-lookup"><span data-stu-id="ae737-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="ae737-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae737-110">PARAMETERS</span></span>

### <span data-ttu-id="ae737-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae737-111">-DefaultProfile</span></span>
<span data-ttu-id="ae737-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae737-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae737-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ae737-113">-Name</span></span>
<span data-ttu-id="ae737-114">Имя виртуального сетевого шлюза.</span><span class="sxs-lookup"><span data-stu-id="ae737-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="ae737-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae737-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae737-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ae737-116">The resource group name.</span></span>

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

### <span data-ttu-id="ae737-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae737-117">CommonParameters</span></span>
<span data-ttu-id="ae737-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae737-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae737-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae737-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae737-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae737-120">INPUTS</span></span>

### <span data-ttu-id="ae737-121">System.String</span><span class="sxs-lookup"><span data-stu-id="ae737-121">System.String</span></span>

## <span data-ttu-id="ae737-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae737-122">OUTPUTS</span></span>

### <span data-ttu-id="ae737-123">System.String</span><span class="sxs-lookup"><span data-stu-id="ae737-123">System.String</span></span>

## <span data-ttu-id="ae737-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae737-124">NOTES</span></span>

## <span data-ttu-id="ae737-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae737-125">RELATED LINKS</span></span>
