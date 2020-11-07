---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 30937c856d1961a1f342c73588aa00c74790ec81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732633"
---
# <span data-ttu-id="d2e89-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="d2e89-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="d2e89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2e89-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e89-103">Этот unifiedgroup возвращает список поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="d2e89-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2e89-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2e89-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e89-106">Этот unifiedgroup возвращает список поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="d2e89-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="d2e89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2e89-107">EXAMPLES</span></span>

### <span data-ttu-id="d2e89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d2e89-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="d2e89-109">Возвращает список поддерживаемых торговых марок устройств VPN, моделей и версий микропрограмм:</span><span class="sxs-lookup"><span data-stu-id="d2e89-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="d2e89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2e89-110">PARAMETERS</span></span>

### <span data-ttu-id="d2e89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e89-111">-DefaultProfile</span></span>
<span data-ttu-id="d2e89-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2e89-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2e89-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2e89-113">-Name</span></span>
<span data-ttu-id="d2e89-114">Имя шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d2e89-114">The virtual network gateway name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e89-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e89-115">-ResourceGroupName</span></span>
<span data-ttu-id="d2e89-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2e89-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e89-117">CommonParameters</span></span>
<span data-ttu-id="d2e89-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2e89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e89-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e89-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e89-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2e89-120">INPUTS</span></span>

### <span data-ttu-id="d2e89-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e89-121">System.String</span></span>

## <span data-ttu-id="d2e89-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2e89-122">OUTPUTS</span></span>

### <span data-ttu-id="d2e89-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e89-123">System.String</span></span>

## <span data-ttu-id="d2e89-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2e89-124">NOTES</span></span>

## <span data-ttu-id="d2e89-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2e89-125">RELATED LINKS</span></span>

