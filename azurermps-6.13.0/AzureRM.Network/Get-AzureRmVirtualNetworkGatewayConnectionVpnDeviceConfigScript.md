---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: abaaaf7d9f430bd1b7850f3141b651ac02821257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560079"
---
# <span data-ttu-id="cb540-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="cb540-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="cb540-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cb540-102">SYNOPSIS</span></span>
<span data-ttu-id="cb540-103">Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN.</span><span class="sxs-lookup"><span data-stu-id="cb540-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="cb540-104">Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="cb540-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb540-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cb540-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb540-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb540-106">DESCRIPTION</span></span>
<span data-ttu-id="cb540-107">Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN.</span><span class="sxs-lookup"><span data-stu-id="cb540-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="cb540-108">Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="cb540-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="cb540-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cb540-109">EXAMPLES</span></span>

### <span data-ttu-id="cb540-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb540-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="cb540-111">В приведенном выше примере Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice используется для получения поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="cb540-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="cb540-112">Затем использует одну из данных возвращенных моделей для создания сценария конфигурации устройства VPN для VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="cb540-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="cb540-113">Устройство, используемое в этом примере, имеет DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" и FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="cb540-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="cb540-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cb540-114">PARAMETERS</span></span>

### <span data-ttu-id="cb540-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb540-115">-DefaultProfile</span></span>
<span data-ttu-id="cb540-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb540-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb540-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="cb540-117">-DeviceFamily</span></span>
<span data-ttu-id="cb540-118">Имя модели или семейства VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="cb540-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="cb540-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="cb540-119">-DeviceVendor</span></span>
<span data-ttu-id="cb540-120">Имя поставщика VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="cb540-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="cb540-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="cb540-121">-FirmwareVersion</span></span>
<span data-ttu-id="cb540-122">Версия встроенного по устройства VPN.</span><span class="sxs-lookup"><span data-stu-id="cb540-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="cb540-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cb540-123">-Name</span></span>
<span data-ttu-id="cb540-124">Название ресурса соединения, для которого необходимо создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="cb540-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="cb540-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb540-125">-ResourceGroupName</span></span>
<span data-ttu-id="cb540-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb540-126">The resource group name.</span></span>

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

### <span data-ttu-id="cb540-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb540-127">-Confirm</span></span>
<span data-ttu-id="cb540-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cb540-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb540-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb540-129">-WhatIf</span></span>
<span data-ttu-id="cb540-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cb540-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb540-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cb540-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb540-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb540-132">CommonParameters</span></span>
<span data-ttu-id="cb540-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cb540-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb540-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb540-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb540-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cb540-135">INPUTS</span></span>

### <span data-ttu-id="cb540-136">System. String</span><span class="sxs-lookup"><span data-stu-id="cb540-136">System.String</span></span>

## <span data-ttu-id="cb540-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb540-137">OUTPUTS</span></span>

### <span data-ttu-id="cb540-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cb540-138">System.String</span></span>

## <span data-ttu-id="cb540-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="cb540-139">NOTES</span></span>

## <span data-ttu-id="cb540-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb540-140">RELATED LINKS</span></span>
