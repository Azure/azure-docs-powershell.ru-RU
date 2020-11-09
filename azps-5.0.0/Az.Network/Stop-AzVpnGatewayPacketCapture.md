---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318539"
---
# <span data-ttu-id="7142a-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7142a-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="7142a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7142a-102">SYNOPSIS</span></span>
<span data-ttu-id="7142a-103">Останавливает операцию захвата пакетов на шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="7142a-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="7142a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7142a-104">SYNTAX</span></span>

### <span data-ttu-id="7142a-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7142a-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7142a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="7142a-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7142a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="7142a-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7142a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7142a-108">DESCRIPTION</span></span>
<span data-ttu-id="7142a-109">Останавливает операцию захвата пакетов на шлюзе VPN и отправляет результат по данному SasUrl контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="7142a-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="7142a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7142a-110">EXAMPLES</span></span>

### <span data-ttu-id="7142a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7142a-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="7142a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7142a-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="7142a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7142a-113">PARAMETERS</span></span>

### <span data-ttu-id="7142a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7142a-114">-AsJob</span></span>
<span data-ttu-id="7142a-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7142a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7142a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7142a-116">-DefaultProfile</span></span>
<span data-ttu-id="7142a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7142a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7142a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7142a-118">-InputObject</span></span>
<span data-ttu-id="7142a-119">Объект шлюза VPN, на котором запускается сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="7142a-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="7142a-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7142a-120">-Name</span></span>
<span data-ttu-id="7142a-121">Имя шлюза VPN, на котором запускается сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="7142a-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="7142a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7142a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7142a-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7142a-123">The resource group name.</span></span>

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

### <span data-ttu-id="7142a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7142a-124">-ResourceId</span></span>
<span data-ttu-id="7142a-125">Идентификатор ресурса Azure VpnGateway, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="7142a-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="7142a-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="7142a-126">-SasUrl</span></span>
<span data-ttu-id="7142a-127">URL-пакеты SAS на шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="7142a-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="7142a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7142a-128">-Confirm</span></span>
<span data-ttu-id="7142a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7142a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7142a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7142a-130">-WhatIf</span></span>
<span data-ttu-id="7142a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7142a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7142a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7142a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7142a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7142a-133">CommonParameters</span></span>
<span data-ttu-id="7142a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7142a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7142a-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7142a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7142a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7142a-136">INPUTS</span></span>

### <span data-ttu-id="7142a-137">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="7142a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="7142a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="7142a-138">System.String</span></span>

## <span data-ttu-id="7142a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7142a-139">OUTPUTS</span></span>

### <span data-ttu-id="7142a-140">Microsoft. Azure. Commands. Network. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="7142a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="7142a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="7142a-141">NOTES</span></span>

## <span data-ttu-id="7142a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7142a-142">RELATED LINKS</span></span>

[<span data-ttu-id="7142a-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7142a-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)