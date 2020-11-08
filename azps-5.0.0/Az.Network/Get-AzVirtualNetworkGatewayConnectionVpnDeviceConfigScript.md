---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247276"
---
# <span data-ttu-id="072a3-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="072a3-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="072a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="072a3-102">SYNOPSIS</span></span>
<span data-ttu-id="072a3-103">Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN.</span><span class="sxs-lookup"><span data-stu-id="072a3-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="072a3-104">Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="072a3-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="072a3-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="072a3-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="072a3-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="072a3-106">DESCRIPTION</span></span>
<span data-ttu-id="072a3-107">Этот unifiedgroup берет на себя ресурс подключения, марку VPN-устройства, модель, версию микропрограммы и возвращает соответствующий сценарий конфигурации, который пользователи могут применять непосредственно на локальных виртуальных устройствах VPN.</span><span class="sxs-lookup"><span data-stu-id="072a3-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="072a3-108">Сценарий будет следовать синтаксису выбранного устройства и заполнить необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных сетевых адресов, предварительный ключ VPN-туннеля и т. д., чтобы пользователи могли просто копировать и вставлять их в конфигурации VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="072a3-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="072a3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="072a3-109">EXAMPLES</span></span>

### <span data-ttu-id="072a3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="072a3-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="072a3-111">В приведенном выше примере Get-AzVirtualNetworkGatewaySupportedVpnDevice используется для получения поддерживаемых торговых марок, моделей и версий микропрограмм для устройств VPN.</span><span class="sxs-lookup"><span data-stu-id="072a3-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="072a3-112">Затем использует одну из данных возвращенных моделей для создания сценария конфигурации устройства VPN для VirtualNetworkGatewayConnection "TestConnection".</span><span class="sxs-lookup"><span data-stu-id="072a3-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="072a3-113">Устройство, используемое в этом примере, имеет DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" и FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="072a3-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="072a3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="072a3-114">PARAMETERS</span></span>

### <span data-ttu-id="072a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="072a3-115">-DefaultProfile</span></span>
<span data-ttu-id="072a3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="072a3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="072a3-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="072a3-117">-DeviceFamily</span></span>
<span data-ttu-id="072a3-118">Имя модели или семейства VPN-устройств.</span><span class="sxs-lookup"><span data-stu-id="072a3-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="072a3-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="072a3-119">-DeviceVendor</span></span>
<span data-ttu-id="072a3-120">Имя поставщика VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="072a3-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="072a3-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="072a3-121">-FirmwareVersion</span></span>
<span data-ttu-id="072a3-122">Версия встроенного по устройства VPN.</span><span class="sxs-lookup"><span data-stu-id="072a3-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="072a3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="072a3-123">-Name</span></span>
<span data-ttu-id="072a3-124">Название ресурса соединения, для которого необходимо создать конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="072a3-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="072a3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="072a3-125">-ResourceGroupName</span></span>
<span data-ttu-id="072a3-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="072a3-126">The resource group name.</span></span>

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

### <span data-ttu-id="072a3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="072a3-127">-Confirm</span></span>
<span data-ttu-id="072a3-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="072a3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="072a3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="072a3-129">-WhatIf</span></span>
<span data-ttu-id="072a3-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="072a3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="072a3-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="072a3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="072a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072a3-132">CommonParameters</span></span>
<span data-ttu-id="072a3-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="072a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072a3-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="072a3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072a3-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="072a3-135">INPUTS</span></span>

### <span data-ttu-id="072a3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="072a3-136">System.String</span></span>

## <span data-ttu-id="072a3-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="072a3-137">OUTPUTS</span></span>

### <span data-ttu-id="072a3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="072a3-138">System.String</span></span>

## <span data-ttu-id="072a3-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="072a3-139">NOTES</span></span>

## <span data-ttu-id="072a3-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="072a3-140">RELATED LINKS</span></span>
