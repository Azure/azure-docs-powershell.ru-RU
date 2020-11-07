---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914430"
---
# <span data-ttu-id="64408-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="64408-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="64408-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64408-102">SYNOPSIS</span></span>
<span data-ttu-id="64408-103">Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN.</span><span class="sxs-lookup"><span data-stu-id="64408-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="64408-104">Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="64408-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64408-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64408-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64408-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64408-106">DESCRIPTION</span></span>
<span data-ttu-id="64408-107">Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN.</span><span class="sxs-lookup"><span data-stu-id="64408-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="64408-108">Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="64408-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="64408-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64408-109">EXAMPLES</span></span>

### <span data-ttu-id="64408-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64408-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="64408-111">В приведенном выше примере Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice используется для получения поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="64408-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="64408-112">Затем использует одну из данных возвращенных моделей для создания сценария конфигурации устройства VPN для VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="64408-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="64408-113">Устройство, используемое в этом примере, имеет DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" и FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="64408-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="64408-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64408-114">PARAMETERS</span></span>

### <span data-ttu-id="64408-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64408-115">-DefaultProfile</span></span>
<span data-ttu-id="64408-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64408-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64408-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="64408-117">-DeviceFamily</span></span>
<span data-ttu-id="64408-118">Имя модели или семейства VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="64408-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="64408-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="64408-119">-DeviceVendor</span></span>
<span data-ttu-id="64408-120">Имя поставщика VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="64408-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="64408-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="64408-121">-FirmwareVersion</span></span>
<span data-ttu-id="64408-122">Версия встроенного по устройства VPN.</span><span class="sxs-lookup"><span data-stu-id="64408-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="64408-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="64408-123">-Name</span></span>
<span data-ttu-id="64408-124">Название ресурса соединения, для которого необходимо создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="64408-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="64408-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64408-125">-ResourceGroupName</span></span>
<span data-ttu-id="64408-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64408-126">The resource group name.</span></span>

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

### <span data-ttu-id="64408-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64408-127">-Confirm</span></span>
<span data-ttu-id="64408-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64408-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64408-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64408-129">-WhatIf</span></span>
<span data-ttu-id="64408-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64408-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64408-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64408-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64408-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64408-132">CommonParameters</span></span>
<span data-ttu-id="64408-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64408-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64408-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64408-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64408-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64408-135">INPUTS</span></span>

### <span data-ttu-id="64408-136">System. String</span><span class="sxs-lookup"><span data-stu-id="64408-136">System.String</span></span>

## <span data-ttu-id="64408-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64408-137">OUTPUTS</span></span>

### <span data-ttu-id="64408-138">System. String</span><span class="sxs-lookup"><span data-stu-id="64408-138">System.String</span></span>

## <span data-ttu-id="64408-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="64408-139">NOTES</span></span>

## <span data-ttu-id="64408-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64408-140">RELATED LINKS</span></span>

