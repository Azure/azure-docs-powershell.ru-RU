---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911925"
---
# <span data-ttu-id="aaef9-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aaef9-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="aaef9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaef9-102">SYNOPSIS</span></span>
<span data-ttu-id="aaef9-103">Запускает операцию захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aaef9-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="aaef9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaef9-104">SYNTAX</span></span>

### <span data-ttu-id="aaef9-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="aaef9-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaef9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aaef9-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaef9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aaef9-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaef9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaef9-108">DESCRIPTION</span></span>
<span data-ttu-id="aaef9-109">Запускает операцию захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aaef9-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="aaef9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaef9-110">EXAMPLES</span></span>

### <span data-ttu-id="aaef9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aaef9-111">Example 1</span></span>
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
### <span data-ttu-id="aaef9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="aaef9-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="aaef9-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="aaef9-113">Example 3</span></span>
<span data-ttu-id="aaef9-114">Пример захвата пакетов для захвата всех внутренних и внешних пакетов</span><span class="sxs-lookup"><span data-stu-id="aaef9-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="aaef9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaef9-115">PARAMETERS</span></span>

### <span data-ttu-id="aaef9-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaef9-116">-AsJob</span></span>
<span data-ttu-id="aaef9-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="aaef9-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aaef9-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaef9-118">-Confirm</span></span>
<span data-ttu-id="aaef9-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aaef9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaef9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaef9-120">-DefaultProfile</span></span>
<span data-ttu-id="aaef9-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaef9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaef9-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="aaef9-122">-FilterData</span></span>
<span data-ttu-id="aaef9-123">Параметры фильтра для запуска захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="aaef9-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="aaef9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaef9-124">-InputObject</span></span>
<span data-ttu-id="aaef9-125">Объект шлюза виртуальной сети, в котором запускается сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="aaef9-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="aaef9-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aaef9-126">-Name</span></span>
<span data-ttu-id="aaef9-127">Имя шлюза виртуальной сети, на котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="aaef9-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="aaef9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaef9-128">-ResourceGroupName</span></span>
<span data-ttu-id="aaef9-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaef9-129">The resource group name.</span></span>

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

### <span data-ttu-id="aaef9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aaef9-130">-ResourceId</span></span>
<span data-ttu-id="aaef9-131">Идентификатор ресурса Azure VirtualNetworkGateway, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="aaef9-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="aaef9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaef9-132">-WhatIf</span></span>
<span data-ttu-id="aaef9-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aaef9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaef9-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aaef9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaef9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaef9-135">CommonParameters</span></span>
<span data-ttu-id="aaef9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaef9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaef9-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aaef9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaef9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaef9-138">INPUTS</span></span>

### <span data-ttu-id="aaef9-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="aaef9-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="aaef9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="aaef9-140">System.String</span></span>

## <span data-ttu-id="aaef9-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaef9-141">OUTPUTS</span></span>

### <span data-ttu-id="aaef9-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="aaef9-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="aaef9-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaef9-143">NOTES</span></span>

## <span data-ttu-id="aaef9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaef9-144">RELATED LINKS</span></span>
[<span data-ttu-id="aaef9-145">Остановить-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aaef9-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)