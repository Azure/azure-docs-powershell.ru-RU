---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 1f0b539e2f5a6e2c387738558fb6db8cbe647457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904322"
---
# <span data-ttu-id="00984-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00984-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="00984-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00984-102">SYNOPSIS</span></span>
<span data-ttu-id="00984-103">Запускает операцию захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00984-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="00984-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00984-104">SYNTAX</span></span>

### <span data-ttu-id="00984-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00984-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00984-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="00984-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00984-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00984-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00984-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00984-108">DESCRIPTION</span></span>
<span data-ttu-id="00984-109">Запускает операцию захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00984-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="00984-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00984-110">EXAMPLES</span></span>

### <span data-ttu-id="00984-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00984-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

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
### <span data-ttu-id="00984-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="00984-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

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

## <span data-ttu-id="00984-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00984-113">PARAMETERS</span></span>

### <span data-ttu-id="00984-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="00984-114">-AsJob</span></span>
<span data-ttu-id="00984-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="00984-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00984-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00984-116">-Confirm</span></span>
<span data-ttu-id="00984-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00984-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00984-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00984-118">-DefaultProfile</span></span>
<span data-ttu-id="00984-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00984-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00984-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="00984-120">-FilterData</span></span>
<span data-ttu-id="00984-121">Параметры фильтра для запуска захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="00984-121">Filter options for start packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00984-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00984-122">-InputObject</span></span>
<span data-ttu-id="00984-123">Объект шлюза виртуальной сети, в котором запускается сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="00984-123">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00984-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00984-124">-Name</span></span>
<span data-ttu-id="00984-125">Имя шлюза виртуальной сети, на котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="00984-125">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00984-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00984-126">-ResourceGroupName</span></span>
<span data-ttu-id="00984-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="00984-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00984-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00984-128">-ResourceId</span></span>
<span data-ttu-id="00984-129">Идентификатор ресурса Azure VirtualNetworkGateway, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="00984-129">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00984-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00984-130">-WhatIf</span></span>
<span data-ttu-id="00984-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00984-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00984-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00984-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00984-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00984-133">CommonParameters</span></span>
<span data-ttu-id="00984-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00984-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00984-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00984-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00984-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00984-136">INPUTS</span></span>

### <span data-ttu-id="00984-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="00984-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="00984-138">System. String</span><span class="sxs-lookup"><span data-stu-id="00984-138">System.String</span></span>

## <span data-ttu-id="00984-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00984-139">OUTPUTS</span></span>

### <span data-ttu-id="00984-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="00984-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="00984-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="00984-141">NOTES</span></span>

## <span data-ttu-id="00984-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00984-142">RELATED LINKS</span></span>
[<span data-ttu-id="00984-143">Остановить-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="00984-143">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)