---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978291"
---
# <span data-ttu-id="58008-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="58008-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="58008-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58008-102">SYNOPSIS</span></span>
<span data-ttu-id="58008-103">Этот командлет принимает ресурс подключения, бренд VPN-устройства, модель, версию по прямой настройке и возвращает сценарий конфигурации, который клиенты могут применять непосредственно на своих собственных VPN-устройствах.</span><span class="sxs-lookup"><span data-stu-id="58008-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="58008-104">Сценарий будет выполнять синтаксис выбранного устройства и заполнять необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных адресов сети, VPN-туннель предварительного общего доступа и т. д., чтобы клиенты могли просто скопировать вставку в конфигурации VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="58008-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="58008-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="58008-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58008-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58008-106">DESCRIPTION</span></span>
<span data-ttu-id="58008-107">Этот командлет принимает ресурс подключения, бренд VPN-устройства, модель, версию по прямой настройке и возвращает сценарий конфигурации, который клиенты могут применять непосредственно на своих собственных VPN-устройствах.</span><span class="sxs-lookup"><span data-stu-id="58008-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="58008-108">Сценарий будет выполнять синтаксис выбранного устройства и заполнять необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных адресов сети, VPN-туннель предварительного общего доступа и т. д., чтобы клиенты могли просто скопировать вставку в конфигурации VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="58008-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="58008-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="58008-109">EXAMPLES</span></span>

### <span data-ttu-id="58008-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58008-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="58008-111">В примере выше Get-AzVirtualNetworkGatewaySupportedVpnDevice для получения поддерживаемых марок VPN-устройств, моделей и версий микропрограмм.</span><span class="sxs-lookup"><span data-stu-id="58008-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="58008-112">Затем использует одну из возвращенных моделей для создания сценария конфигурации VPN-устройства для Технологии TestConnection VirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="58008-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="58008-113">На устройстве, используемом в этом примере, есть DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" и FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="58008-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="58008-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58008-114">PARAMETERS</span></span>

### <span data-ttu-id="58008-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58008-115">-DefaultProfile</span></span>
<span data-ttu-id="58008-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58008-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58008-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="58008-117">-DeviceFamily</span></span>
<span data-ttu-id="58008-118">Имя модели устройства VPN или семейства.</span><span class="sxs-lookup"><span data-stu-id="58008-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="58008-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="58008-119">-DeviceVendor</span></span>
<span data-ttu-id="58008-120">Имя поставщика vpn-устройств.</span><span class="sxs-lookup"><span data-stu-id="58008-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="58008-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="58008-121">-FirmwareVersion</span></span>
<span data-ttu-id="58008-122">Версия ПРОГРАММЫ VPN.</span><span class="sxs-lookup"><span data-stu-id="58008-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="58008-123">-Name</span><span class="sxs-lookup"><span data-stu-id="58008-123">-Name</span></span>
<span data-ttu-id="58008-124">Имя ресурса подключения, для которого создается конфигурация.</span><span class="sxs-lookup"><span data-stu-id="58008-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="58008-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58008-125">-ResourceGroupName</span></span>
<span data-ttu-id="58008-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58008-126">The resource group name.</span></span>

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

### <span data-ttu-id="58008-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58008-127">-Confirm</span></span>
<span data-ttu-id="58008-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="58008-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58008-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58008-129">-WhatIf</span></span>
<span data-ttu-id="58008-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58008-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58008-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="58008-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58008-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58008-132">CommonParameters</span></span>
<span data-ttu-id="58008-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58008-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58008-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58008-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58008-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="58008-135">INPUTS</span></span>

### <span data-ttu-id="58008-136">System.String</span><span class="sxs-lookup"><span data-stu-id="58008-136">System.String</span></span>

## <span data-ttu-id="58008-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="58008-137">OUTPUTS</span></span>

### <span data-ttu-id="58008-138">System.String</span><span class="sxs-lookup"><span data-stu-id="58008-138">System.String</span></span>

## <span data-ttu-id="58008-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="58008-139">NOTES</span></span>

## <span data-ttu-id="58008-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58008-140">RELATED LINKS</span></span>
