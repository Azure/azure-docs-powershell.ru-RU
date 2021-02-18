---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218713"
---
# <span data-ttu-id="4af90-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="4af90-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="4af90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4af90-102">SYNOPSIS</span></span>
<span data-ttu-id="4af90-103">Этот командлет принимает ресурс подключения, бренд VPN-устройства, модель, версию программы firmWARE и возвращает сценарий конфигурации, который клиенты могут применять непосредственно на своих собственных VPN-устройствах.</span><span class="sxs-lookup"><span data-stu-id="4af90-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="4af90-104">Сценарий выполнит синтаксис выбранного устройства и заполнит необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных адресов сети, VPN-туннель предварительного общего доступа и т. д., чтобы клиенты могли просто скопировать вставку в конфигурации VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="4af90-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="4af90-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4af90-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4af90-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4af90-106">DESCRIPTION</span></span>
<span data-ttu-id="4af90-107">Этот командлет принимает ресурс подключения, бренд VPN-устройства, модель, версию программы firmWARE и возвращает сценарий конфигурации, который клиенты могут применять непосредственно на своих собственных VPN-устройствах.</span><span class="sxs-lookup"><span data-stu-id="4af90-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="4af90-108">Сценарий выполнит синтаксис выбранного устройства и заполнит необходимые параметры, такие как общедоступные IP-адреса шлюза Azure, префиксы виртуальных адресов сети, VPN-туннель предварительного общего доступа и т. д., чтобы клиенты могли просто скопировать вставку в конфигурации VPN-устройства.</span><span class="sxs-lookup"><span data-stu-id="4af90-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="4af90-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4af90-109">EXAMPLES</span></span>

### <span data-ttu-id="4af90-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4af90-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="4af90-111">В примере выше Get-AzVirtualNetworkGatewaySupportedVpnDevice для получения поддерживаемых марок VPN-устройств, моделей и версий микропрограмм.</span><span class="sxs-lookup"><span data-stu-id="4af90-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="4af90-112">Затем использует одну из возвращенных моделей для создания сценария конфигурации VPN-устройства для Технологии TestConnection VirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="4af90-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="4af90-113">На устройстве, используемом в этом примере, есть DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" и FirmwareVersion 20.</span><span class="sxs-lookup"><span data-stu-id="4af90-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="4af90-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4af90-114">PARAMETERS</span></span>

### <span data-ttu-id="4af90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4af90-115">-DefaultProfile</span></span>
<span data-ttu-id="4af90-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4af90-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4af90-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="4af90-117">-DeviceFamily</span></span>
<span data-ttu-id="4af90-118">Имя модели устройства VPN или семейства.</span><span class="sxs-lookup"><span data-stu-id="4af90-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="4af90-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="4af90-119">-DeviceVendor</span></span>
<span data-ttu-id="4af90-120">Имя поставщика vpn-устройств.</span><span class="sxs-lookup"><span data-stu-id="4af90-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="4af90-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="4af90-121">-FirmwareVersion</span></span>
<span data-ttu-id="4af90-122">Версия ПРОГРАММЫ VPN.</span><span class="sxs-lookup"><span data-stu-id="4af90-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="4af90-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4af90-123">-Name</span></span>
<span data-ttu-id="4af90-124">Имя ресурса подключения, для которого создается конфигурация.</span><span class="sxs-lookup"><span data-stu-id="4af90-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="4af90-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4af90-125">-ResourceGroupName</span></span>
<span data-ttu-id="4af90-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4af90-126">The resource group name.</span></span>

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

### <span data-ttu-id="4af90-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4af90-127">-Confirm</span></span>
<span data-ttu-id="4af90-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4af90-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4af90-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4af90-129">-WhatIf</span></span>
<span data-ttu-id="4af90-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4af90-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4af90-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4af90-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4af90-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4af90-132">CommonParameters</span></span>
<span data-ttu-id="4af90-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4af90-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4af90-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4af90-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4af90-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4af90-135">INPUTS</span></span>

### <span data-ttu-id="4af90-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4af90-136">System.String</span></span>

## <span data-ttu-id="4af90-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4af90-137">OUTPUTS</span></span>

### <span data-ttu-id="4af90-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4af90-138">System.String</span></span>

## <span data-ttu-id="4af90-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4af90-139">NOTES</span></span>

## <span data-ttu-id="4af90-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4af90-140">RELATED LINKS</span></span>
