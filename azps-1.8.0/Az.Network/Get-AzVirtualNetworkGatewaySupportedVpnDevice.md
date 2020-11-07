---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 0ff95b3e212e61b3d8c9d01b0ad745963d7b24e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730468"
---
# <span data-ttu-id="aae63-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="aae63-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="aae63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aae63-102">SYNOPSIS</span></span>
<span data-ttu-id="aae63-103">Этот unifiedgroup возвращает список поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="aae63-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="aae63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aae63-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aae63-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aae63-105">DESCRIPTION</span></span>
<span data-ttu-id="aae63-106">Этот unifiedgroup возвращает список поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="aae63-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="aae63-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aae63-107">EXAMPLES</span></span>

### <span data-ttu-id="aae63-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aae63-108">Example 1</span></span>
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

<span data-ttu-id="aae63-109">Возвращает список поддерживаемых торговых марок устройств VPN, моделей и версий микропрограмм:</span><span class="sxs-lookup"><span data-stu-id="aae63-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="aae63-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aae63-110">PARAMETERS</span></span>

### <span data-ttu-id="aae63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aae63-111">-DefaultProfile</span></span>
<span data-ttu-id="aae63-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aae63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aae63-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aae63-113">-Name</span></span>
<span data-ttu-id="aae63-114">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aae63-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="aae63-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aae63-115">-ResourceGroupName</span></span>
<span data-ttu-id="aae63-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aae63-116">The resource group name.</span></span>

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

### <span data-ttu-id="aae63-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aae63-117">CommonParameters</span></span>
<span data-ttu-id="aae63-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aae63-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aae63-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aae63-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aae63-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aae63-120">INPUTS</span></span>

### <span data-ttu-id="aae63-121">System. String</span><span class="sxs-lookup"><span data-stu-id="aae63-121">System.String</span></span>

## <span data-ttu-id="aae63-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aae63-122">OUTPUTS</span></span>

### <span data-ttu-id="aae63-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aae63-123">System.String</span></span>

## <span data-ttu-id="aae63-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="aae63-124">NOTES</span></span>

## <span data-ttu-id="aae63-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aae63-125">RELATED LINKS</span></span>
