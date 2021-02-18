---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240520"
---
# <span data-ttu-id="35380-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35380-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="35380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35380-102">SYNOPSIS</span></span>
<span data-ttu-id="35380-103">Остановка операции захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="35380-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="35380-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35380-104">SYNTAX</span></span>

### <span data-ttu-id="35380-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35380-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35380-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35380-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35380-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35380-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35380-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35380-108">DESCRIPTION</span></span>
<span data-ttu-id="35380-109">Остановка операции захвата пакетов на виртуальном сетевом шлюзе и отправка результата для заданного контейнера хранилища SasUrl.</span><span class="sxs-lookup"><span data-stu-id="35380-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="35380-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35380-110">EXAMPLES</span></span>

### <span data-ttu-id="35380-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35380-111">Example 1</span></span>
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

### <span data-ttu-id="35380-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="35380-112">Example 2</span></span>
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

## <span data-ttu-id="35380-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35380-113">PARAMETERS</span></span>

### <span data-ttu-id="35380-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35380-114">-AsJob</span></span>
<span data-ttu-id="35380-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35380-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35380-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35380-116">-Confirm</span></span>
<span data-ttu-id="35380-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35380-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35380-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35380-118">-DefaultProfile</span></span>
<span data-ttu-id="35380-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35380-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35380-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35380-120">-InputObject</span></span>
<span data-ttu-id="35380-121">Объект виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="35380-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="35380-122">-Name</span><span class="sxs-lookup"><span data-stu-id="35380-122">-Name</span></span>
<span data-ttu-id="35380-123">Имя виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="35380-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="35380-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35380-124">-ResourceGroupName</span></span>
<span data-ttu-id="35380-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35380-125">The resource group name.</span></span>

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

### <span data-ttu-id="35380-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35380-126">-ResourceId</span></span>
<span data-ttu-id="35380-127">Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="35380-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="35380-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="35380-128">-SasUrl</span></span>
<span data-ttu-id="35380-129">URL-адрес SAS для захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="35380-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="35380-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35380-130">-WhatIf</span></span>
<span data-ttu-id="35380-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35380-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35380-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35380-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35380-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35380-133">CommonParameters</span></span>
<span data-ttu-id="35380-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35380-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35380-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35380-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35380-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35380-136">INPUTS</span></span>

### <span data-ttu-id="35380-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="35380-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="35380-138">System.String</span><span class="sxs-lookup"><span data-stu-id="35380-138">System.String</span></span>

## <span data-ttu-id="35380-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35380-139">OUTPUTS</span></span>

### <span data-ttu-id="35380-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="35380-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="35380-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35380-141">NOTES</span></span>

## <span data-ttu-id="35380-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35380-142">RELATED LINKS</span></span>
[<span data-ttu-id="35380-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="35380-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
