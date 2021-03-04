---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 0b920adf2f0357db7e9babf7b8e4b4e603255fab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951880"
---
# <span data-ttu-id="644a8-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="644a8-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="644a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="644a8-102">SYNOPSIS</span></span>
<span data-ttu-id="644a8-103">Начинает операцию захвата пакетов для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="644a8-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="644a8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="644a8-104">SYNTAX</span></span>

### <span data-ttu-id="644a8-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="644a8-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="644a8-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="644a8-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="644a8-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="644a8-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="644a8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="644a8-108">DESCRIPTION</span></span>
<span data-ttu-id="644a8-109">Начинает операцию захвата пакетов для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="644a8-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="644a8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="644a8-110">EXAMPLES</span></span>

### <span data-ttu-id="644a8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="644a8-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="644a8-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="644a8-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="644a8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="644a8-113">PARAMETERS</span></span>

### <span data-ttu-id="644a8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="644a8-114">-AsJob</span></span>
<span data-ttu-id="644a8-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="644a8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="644a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644a8-116">-DefaultProfile</span></span>
<span data-ttu-id="644a8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="644a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="644a8-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="644a8-118">-FilterData</span></span>
<span data-ttu-id="644a8-119">Параметры фильтрации для запуска захвата пакетов на VPN-подмесяце.</span><span class="sxs-lookup"><span data-stu-id="644a8-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="644a8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="644a8-120">-InputObject</span></span>
<span data-ttu-id="644a8-121">Объект VPN-подключения, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="644a8-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="644a8-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="644a8-122">-LinkConnectionName</span></span>
<span data-ttu-id="644a8-123">Имена SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="644a8-123">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644a8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="644a8-124">-Name</span></span>
<span data-ttu-id="644a8-125">Имя VPN-подключения, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="644a8-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644a8-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="644a8-126">-ParentResourceName</span></span>
<span data-ttu-id="644a8-127">Имя Parent Vpngateway.</span><span class="sxs-lookup"><span data-stu-id="644a8-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644a8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="644a8-128">-ResourceGroupName</span></span>
<span data-ttu-id="644a8-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="644a8-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="644a8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="644a8-130">-ResourceId</span></span>
<span data-ttu-id="644a8-131">Azure resource ID of the VpnConnection where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="644a8-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644a8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="644a8-132">-Confirm</span></span>
<span data-ttu-id="644a8-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="644a8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="644a8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="644a8-134">-WhatIf</span></span>
<span data-ttu-id="644a8-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="644a8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="644a8-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="644a8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="644a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644a8-137">CommonParameters</span></span>
<span data-ttu-id="644a8-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="644a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644a8-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="644a8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644a8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="644a8-140">INPUTS</span></span>

### <span data-ttu-id="644a8-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="644a8-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="644a8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="644a8-142">System.String</span></span>

## <span data-ttu-id="644a8-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="644a8-143">OUTPUTS</span></span>

### <span data-ttu-id="644a8-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="644a8-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="644a8-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="644a8-145">NOTES</span></span>

## <span data-ttu-id="644a8-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="644a8-146">RELATED LINKS</span></span>

[<span data-ttu-id="644a8-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="644a8-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)