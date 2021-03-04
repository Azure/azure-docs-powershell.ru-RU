---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 4f17777d366884f2b71c16c289e50dbf8425d729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951891"
---
# <span data-ttu-id="e6e7d-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6e7d-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="e6e7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e7d-103">Запускает операцию захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="e6e7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6e7d-104">SYNTAX</span></span>

### <span data-ttu-id="e6e7d-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6e7d-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6e7d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6e7d-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6e7d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6e7d-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6e7d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6e7d-108">DESCRIPTION</span></span>
<span data-ttu-id="e6e7d-109">Запускает операцию захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="e6e7d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6e7d-110">EXAMPLES</span></span>

### <span data-ttu-id="e6e7d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6e7d-111">Example 1</span></span>
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
### <span data-ttu-id="e6e7d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e6e7d-112">Example 2</span></span>
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
### <span data-ttu-id="e6e7d-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e6e7d-113">Example 3</span></span>
<span data-ttu-id="e6e7d-114">Пример захвата пакетов для захвата внутренних и внешних пакетов</span><span class="sxs-lookup"><span data-stu-id="e6e7d-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="e6e7d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6e7d-115">PARAMETERS</span></span>

### <span data-ttu-id="e6e7d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6e7d-116">-AsJob</span></span>
<span data-ttu-id="e6e7d-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e6e7d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6e7d-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6e7d-118">-Confirm</span></span>
<span data-ttu-id="e6e7d-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6e7d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e7d-120">-DefaultProfile</span></span>
<span data-ttu-id="e6e7d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6e7d-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="e6e7d-122">-FilterData</span></span>
<span data-ttu-id="e6e7d-123">Параметры фильтрации для запуска захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="e6e7d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6e7d-124">-InputObject</span></span>
<span data-ttu-id="e6e7d-125">Объект виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="e6e7d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e6e7d-126">-Name</span></span>
<span data-ttu-id="e6e7d-127">Имя виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="e6e7d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e7d-128">-ResourceGroupName</span></span>
<span data-ttu-id="e6e7d-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-129">The resource group name.</span></span>

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

### <span data-ttu-id="e6e7d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6e7d-130">-ResourceId</span></span>
<span data-ttu-id="e6e7d-131">Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="e6e7d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6e7d-132">-WhatIf</span></span>
<span data-ttu-id="e6e7d-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6e7d-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6e7d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e7d-135">CommonParameters</span></span>
<span data-ttu-id="e6e7d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e7d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e7d-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6e7d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e7d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6e7d-138">INPUTS</span></span>

### <span data-ttu-id="e6e7d-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="e6e7d-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="e6e7d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e6e7d-140">System.String</span></span>

## <span data-ttu-id="e6e7d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6e7d-141">OUTPUTS</span></span>

### <span data-ttu-id="e6e7d-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e6e7d-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="e6e7d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6e7d-143">NOTES</span></span>

## <span data-ttu-id="e6e7d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6e7d-144">RELATED LINKS</span></span>
[<span data-ttu-id="e6e7d-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e6e7d-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)