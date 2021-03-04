---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 2838d3d18aaa1cdf450eed184c5ebfe9a803c20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951832"
---
# <span data-ttu-id="5a2d5-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5a2d5-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="5a2d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a2d5-102">SYNOPSIS</span></span>
<span data-ttu-id="5a2d5-103">Остановка операции захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="5a2d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5a2d5-104">SYNTAX</span></span>

### <span data-ttu-id="5a2d5-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a2d5-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a2d5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a2d5-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a2d5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5a2d5-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a2d5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a2d5-108">DESCRIPTION</span></span>
<span data-ttu-id="5a2d5-109">Остановка операции захвата пакетов на виртуальном сетевом шлюзе и отправка результата для заданного контейнера хранилища SasUrl.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="5a2d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5a2d5-110">EXAMPLES</span></span>

### <span data-ttu-id="5a2d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a2d5-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

### <span data-ttu-id="5a2d5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5a2d5-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

## <span data-ttu-id="5a2d5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a2d5-113">PARAMETERS</span></span>

### <span data-ttu-id="5a2d5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a2d5-114">-AsJob</span></span>
<span data-ttu-id="5a2d5-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5a2d5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a2d5-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a2d5-116">-Confirm</span></span>
<span data-ttu-id="5a2d5-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a2d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a2d5-118">-DefaultProfile</span></span>
<span data-ttu-id="5a2d5-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a2d5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a2d5-120">-InputObject</span></span>
<span data-ttu-id="5a2d5-121">Объект виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="5a2d5-122">-Name</span><span class="sxs-lookup"><span data-stu-id="5a2d5-122">-Name</span></span>
<span data-ttu-id="5a2d5-123">Имя виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="5a2d5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a2d5-124">-ResourceGroupName</span></span>
<span data-ttu-id="5a2d5-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-125">The resource group name.</span></span>

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

### <span data-ttu-id="5a2d5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a2d5-126">-ResourceId</span></span>
<span data-ttu-id="5a2d5-127">Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="5a2d5-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="5a2d5-128">-SasUrl</span></span>
<span data-ttu-id="5a2d5-129">URL-адрес SAS для захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="5a2d5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a2d5-130">-WhatIf</span></span>
<span data-ttu-id="5a2d5-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a2d5-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a2d5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a2d5-133">CommonParameters</span></span>
<span data-ttu-id="5a2d5-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a2d5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a2d5-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a2d5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a2d5-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a2d5-136">INPUTS</span></span>

### <span data-ttu-id="5a2d5-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5a2d5-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="5a2d5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5a2d5-138">System.String</span></span>

## <span data-ttu-id="5a2d5-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5a2d5-139">OUTPUTS</span></span>

### <span data-ttu-id="5a2d5-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5a2d5-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="5a2d5-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5a2d5-141">NOTES</span></span>

## <span data-ttu-id="5a2d5-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a2d5-142">RELATED LINKS</span></span>
[<span data-ttu-id="5a2d5-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5a2d5-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
