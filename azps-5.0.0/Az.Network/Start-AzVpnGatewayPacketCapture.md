---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319037"
---
# <span data-ttu-id="ee97d-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ee97d-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="ee97d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee97d-102">SYNOPSIS</span></span>
<span data-ttu-id="ee97d-103">Запускает операцию захвата пакетов на шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="ee97d-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="ee97d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee97d-104">SYNTAX</span></span>

### <span data-ttu-id="ee97d-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee97d-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee97d-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ee97d-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee97d-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ee97d-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee97d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee97d-108">DESCRIPTION</span></span>
<span data-ttu-id="ee97d-109">Запускает операцию захвата пакетов на шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="ee97d-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="ee97d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee97d-110">EXAMPLES</span></span>

### <span data-ttu-id="ee97d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee97d-111">Example 1</span></span>
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

### <span data-ttu-id="ee97d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ee97d-112">Example 2</span></span>
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

## <span data-ttu-id="ee97d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee97d-113">PARAMETERS</span></span>

### <span data-ttu-id="ee97d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee97d-114">-AsJob</span></span>
<span data-ttu-id="ee97d-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ee97d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee97d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee97d-116">-DefaultProfile</span></span>
<span data-ttu-id="ee97d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee97d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee97d-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="ee97d-118">-FilterData</span></span>
<span data-ttu-id="ee97d-119">Параметры фильтра для запуска захвата пакетов на шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="ee97d-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="ee97d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee97d-120">-InputObject</span></span>
<span data-ttu-id="ee97d-121">Объект шлюза VPN, на котором запускается сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="ee97d-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="ee97d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee97d-122">-Name</span></span>
<span data-ttu-id="ee97d-123">Имя шлюза VPN, на котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="ee97d-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="ee97d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee97d-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee97d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee97d-125">The resource group name.</span></span>

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

### <span data-ttu-id="ee97d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee97d-126">-ResourceId</span></span>
<span data-ttu-id="ee97d-127">Идентификатор ресурса Azure VpnGateway, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="ee97d-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="ee97d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee97d-128">-Confirm</span></span>
<span data-ttu-id="ee97d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ee97d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee97d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee97d-130">-WhatIf</span></span>
<span data-ttu-id="ee97d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ee97d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee97d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ee97d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee97d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee97d-133">CommonParameters</span></span>
<span data-ttu-id="ee97d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee97d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee97d-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee97d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee97d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee97d-136">INPUTS</span></span>

### <span data-ttu-id="ee97d-137">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ee97d-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ee97d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ee97d-138">System.String</span></span>

## <span data-ttu-id="ee97d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee97d-139">OUTPUTS</span></span>

### <span data-ttu-id="ee97d-140">Microsoft. Azure. Commands. Network. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="ee97d-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="ee97d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee97d-141">NOTES</span></span>

## <span data-ttu-id="ee97d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee97d-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee97d-143">Остановить-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ee97d-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)