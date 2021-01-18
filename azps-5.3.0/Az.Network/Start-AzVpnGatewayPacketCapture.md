---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517893"
---
# <span data-ttu-id="50879-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50879-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="50879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50879-102">SYNOPSIS</span></span>
<span data-ttu-id="50879-103">Начало операции захвата пакетов на VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="50879-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="50879-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="50879-104">SYNTAX</span></span>

### <span data-ttu-id="50879-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50879-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50879-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="50879-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50879-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="50879-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50879-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50879-108">DESCRIPTION</span></span>
<span data-ttu-id="50879-109">Начало операции захвата пакетов на VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="50879-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="50879-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="50879-110">EXAMPLES</span></span>

### <span data-ttu-id="50879-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="50879-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

### <span data-ttu-id="50879-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="50879-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="50879-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50879-113">PARAMETERS</span></span>

### <span data-ttu-id="50879-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50879-114">-AsJob</span></span>
<span data-ttu-id="50879-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="50879-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50879-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50879-116">-DefaultProfile</span></span>
<span data-ttu-id="50879-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50879-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50879-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="50879-118">-FilterData</span></span>
<span data-ttu-id="50879-119">Параметры фильтрации для запуска захвата пакетов на шлюзе Vpn.</span><span class="sxs-lookup"><span data-stu-id="50879-119">Filter options for start packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50879-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50879-120">-InputObject</span></span>
<span data-ttu-id="50879-121">Объект Vpn Gateway, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="50879-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50879-122">-Name</span><span class="sxs-lookup"><span data-stu-id="50879-122">-Name</span></span>
<span data-ttu-id="50879-123">Имя шлюза Vpn, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="50879-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50879-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50879-124">-ResourceGroupName</span></span>
<span data-ttu-id="50879-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50879-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50879-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50879-126">-ResourceId</span></span>
<span data-ttu-id="50879-127">Azure resource ID of the VpnGateway where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="50879-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50879-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50879-128">-Confirm</span></span>
<span data-ttu-id="50879-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50879-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50879-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50879-130">-WhatIf</span></span>
<span data-ttu-id="50879-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50879-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50879-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="50879-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50879-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50879-133">CommonParameters</span></span>
<span data-ttu-id="50879-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50879-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50879-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50879-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50879-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="50879-136">INPUTS</span></span>

### <span data-ttu-id="50879-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="50879-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="50879-138">System.String</span><span class="sxs-lookup"><span data-stu-id="50879-138">System.String</span></span>

## <span data-ttu-id="50879-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="50879-139">OUTPUTS</span></span>

### <span data-ttu-id="50879-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="50879-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="50879-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="50879-141">NOTES</span></span>

## <span data-ttu-id="50879-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50879-142">RELATED LINKS</span></span>

[<span data-ttu-id="50879-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50879-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)