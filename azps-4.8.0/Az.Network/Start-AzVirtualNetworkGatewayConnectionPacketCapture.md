---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234875"
---
# <span data-ttu-id="e657e-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e657e-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="e657e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e657e-102">SYNOPSIS</span></span>
<span data-ttu-id="e657e-103">Запускает операцию захвата пакетов для подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e657e-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="e657e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e657e-104">SYNTAX</span></span>

### <span data-ttu-id="e657e-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e657e-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e657e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e657e-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e657e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e657e-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e657e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e657e-108">DESCRIPTION</span></span>
<span data-ttu-id="e657e-109">Запускает операцию захвата пакетов для подключения к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e657e-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="e657e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e657e-110">EXAMPLES</span></span>

### <span data-ttu-id="e657e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e657e-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="e657e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e657e-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="e657e-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e657e-113">Example 3</span></span>
<span data-ttu-id="e657e-114">Пример захвата пакетов для захвата всех внутренних и внешних пакетов</span><span class="sxs-lookup"><span data-stu-id="e657e-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="e657e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e657e-115">PARAMETERS</span></span>

### <span data-ttu-id="e657e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e657e-116">-AsJob</span></span>
<span data-ttu-id="e657e-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e657e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e657e-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e657e-118">-Confirm</span></span>
<span data-ttu-id="e657e-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e657e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e657e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e657e-120">-DefaultProfile</span></span>
<span data-ttu-id="e657e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e657e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e657e-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="e657e-122">-FilterData</span></span>
<span data-ttu-id="e657e-123">Параметры фильтра для запуска захвата пакетов на подключении к шлюзу виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e657e-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e657e-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e657e-124">-InputObject</span></span>
<span data-ttu-id="e657e-125">Объект подключения к шлюзу виртуальной сети, для которого необходимо запустить сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="e657e-125">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e657e-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e657e-126">-Name</span></span>
<span data-ttu-id="e657e-127">Имя подключения к шлюзу виртуальной сети, в котором нужно запустить сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="e657e-127">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e657e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e657e-128">-ResourceGroupName</span></span>
<span data-ttu-id="e657e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e657e-129">The resource group name.</span></span>

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

### <span data-ttu-id="e657e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e657e-130">-ResourceId</span></span>
<span data-ttu-id="e657e-131">Идентификатор ресурса Azure VirtualNetworkGatewayConnection, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="e657e-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="e657e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e657e-132">-WhatIf</span></span>
<span data-ttu-id="e657e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e657e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e657e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e657e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e657e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e657e-135">CommonParameters</span></span>
<span data-ttu-id="e657e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e657e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e657e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e657e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e657e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e657e-138">INPUTS</span></span>

### <span data-ttu-id="e657e-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e657e-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="e657e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e657e-140">System.String</span></span>

## <span data-ttu-id="e657e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e657e-141">OUTPUTS</span></span>

### <span data-ttu-id="e657e-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e657e-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="e657e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="e657e-143">NOTES</span></span>

## <span data-ttu-id="e657e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e657e-144">RELATED LINKS</span></span>
[<span data-ttu-id="e657e-145">Остановить-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e657e-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)