---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: d61b12a5a46abbba95919bb747966caf14d61538
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951752"
---
# <span data-ttu-id="9918a-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9918a-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="9918a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9918a-102">SYNOPSIS</span></span>
<span data-ttu-id="9918a-103">Остановка операции захвата пакетов на VPN-шлюзе.</span><span class="sxs-lookup"><span data-stu-id="9918a-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="9918a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9918a-104">SYNTAX</span></span>

### <span data-ttu-id="9918a-105">ByVpnGatewayName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9918a-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9918a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="9918a-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9918a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="9918a-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9918a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9918a-108">DESCRIPTION</span></span>
<span data-ttu-id="9918a-109">Остановка операции захвата пакетов на VPN-шлюзе и отправка результата для заданного контейнера хранилища SasUrl.</span><span class="sxs-lookup"><span data-stu-id="9918a-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="9918a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9918a-110">EXAMPLES</span></span>

### <span data-ttu-id="9918a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9918a-111">Example 1</span></span>
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

### <span data-ttu-id="9918a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9918a-112">Example 2</span></span>
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

## <span data-ttu-id="9918a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9918a-113">PARAMETERS</span></span>

### <span data-ttu-id="9918a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9918a-114">-AsJob</span></span>
<span data-ttu-id="9918a-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9918a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9918a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9918a-116">-DefaultProfile</span></span>
<span data-ttu-id="9918a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9918a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9918a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9918a-118">-InputObject</span></span>
<span data-ttu-id="9918a-119">Объект Vpn Gateway, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="9918a-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="9918a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9918a-120">-Name</span></span>
<span data-ttu-id="9918a-121">Имя шлюза Vpn, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="9918a-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="9918a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9918a-122">-ResourceGroupName</span></span>
<span data-ttu-id="9918a-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9918a-123">The resource group name.</span></span>

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

### <span data-ttu-id="9918a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9918a-124">-ResourceId</span></span>
<span data-ttu-id="9918a-125">Azure resource ID of the VpnGateway where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="9918a-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="9918a-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="9918a-126">-SasUrl</span></span>
<span data-ttu-id="9918a-127">URL-адрес SAS для захвата пакетов на шлюзе Vpn.</span><span class="sxs-lookup"><span data-stu-id="9918a-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="9918a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9918a-128">-Confirm</span></span>
<span data-ttu-id="9918a-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9918a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9918a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9918a-130">-WhatIf</span></span>
<span data-ttu-id="9918a-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9918a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9918a-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9918a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9918a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9918a-133">CommonParameters</span></span>
<span data-ttu-id="9918a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9918a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9918a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9918a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9918a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9918a-136">INPUTS</span></span>

### <span data-ttu-id="9918a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="9918a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="9918a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9918a-138">System.String</span></span>

## <span data-ttu-id="9918a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9918a-139">OUTPUTS</span></span>

### <span data-ttu-id="9918a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="9918a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="9918a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9918a-141">NOTES</span></span>

## <span data-ttu-id="9918a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9918a-142">RELATED LINKS</span></span>

[<span data-ttu-id="9918a-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9918a-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)