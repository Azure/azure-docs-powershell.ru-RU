---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 39bb650333c59bd7d7185449025de7bdd6254fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904309"
---
# <span data-ttu-id="5183d-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5183d-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="5183d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5183d-102">SYNOPSIS</span></span>
<span data-ttu-id="5183d-103">Останавливает операцию захвата пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5183d-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="5183d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5183d-104">SYNTAX</span></span>

### <span data-ttu-id="5183d-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5183d-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5183d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5183d-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5183d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5183d-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5183d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5183d-108">DESCRIPTION</span></span>
<span data-ttu-id="5183d-109">Останавливает операцию захвата пакетов на шлюзе виртуальной сети и отправляет результат по данному SasUrl контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="5183d-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="5183d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5183d-110">EXAMPLES</span></span>

### <span data-ttu-id="5183d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5183d-111">Example 1</span></span>
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
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

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

### <span data-ttu-id="5183d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5183d-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

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

## <span data-ttu-id="5183d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5183d-113">PARAMETERS</span></span>

### <span data-ttu-id="5183d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5183d-114">-AsJob</span></span>
<span data-ttu-id="5183d-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5183d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5183d-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5183d-116">-Confirm</span></span>
<span data-ttu-id="5183d-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5183d-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5183d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5183d-118">-DefaultProfile</span></span>
<span data-ttu-id="5183d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5183d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5183d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5183d-120">-InputObject</span></span>
<span data-ttu-id="5183d-121">Объект шлюза виртуальной сети, в котором запускается сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="5183d-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="5183d-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5183d-122">-Name</span></span>
<span data-ttu-id="5183d-123">Имя шлюза виртуальной сети, в котором нужно запустить сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="5183d-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="5183d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5183d-124">-ResourceGroupName</span></span>
<span data-ttu-id="5183d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5183d-125">The resource group name.</span></span>

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

### <span data-ttu-id="5183d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5183d-126">-ResourceId</span></span>
<span data-ttu-id="5183d-127">Идентификатор ресурса Azure VirtualNetworkGateway, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="5183d-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="5183d-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="5183d-128">-SasUrl</span></span>
<span data-ttu-id="5183d-129">Захват пакетов URL-адресов SAS на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5183d-129">SAS URL packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5183d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5183d-130">-WhatIf</span></span>
<span data-ttu-id="5183d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5183d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5183d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5183d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5183d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5183d-133">CommonParameters</span></span>
<span data-ttu-id="5183d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5183d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5183d-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5183d-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5183d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5183d-136">INPUTS</span></span>

### <span data-ttu-id="5183d-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5183d-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="5183d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5183d-138">System.String</span></span>

## <span data-ttu-id="5183d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5183d-139">OUTPUTS</span></span>

### <span data-ttu-id="5183d-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5183d-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="5183d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="5183d-141">NOTES</span></span>

## <span data-ttu-id="5183d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5183d-142">RELATED LINKS</span></span>
[<span data-ttu-id="5183d-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5183d-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)