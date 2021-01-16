---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412740"
---
# <span data-ttu-id="95698-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95698-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="95698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95698-102">SYNOPSIS</span></span>
<span data-ttu-id="95698-103">Остановка операции захвата пакетов при подсети виртуального сетевого шлюза</span><span class="sxs-lookup"><span data-stu-id="95698-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="95698-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95698-104">SYNTAX</span></span>

### <span data-ttu-id="95698-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95698-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95698-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="95698-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95698-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="95698-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95698-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95698-108">DESCRIPTION</span></span>
<span data-ttu-id="95698-109">Остановка операции захвата пакетов для подключения виртуального сетевого шлюза и отправка результата для заданного контейнера хранилища SasUrl.</span><span class="sxs-lookup"><span data-stu-id="95698-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="95698-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95698-110">EXAMPLES</span></span>

### <span data-ttu-id="95698-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="95698-111">Example 1</span></span>
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
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="95698-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="95698-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="95698-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95698-113">PARAMETERS</span></span>

### <span data-ttu-id="95698-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95698-114">-AsJob</span></span>
<span data-ttu-id="95698-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="95698-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="95698-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95698-116">-Confirm</span></span>
<span data-ttu-id="95698-117">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95698-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95698-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95698-118">-DefaultProfile</span></span>
<span data-ttu-id="95698-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95698-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95698-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95698-120">-InputObject</span></span>
<span data-ttu-id="95698-121">Объект подключения виртуального сетевого шлюза, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="95698-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="95698-122">-Name</span><span class="sxs-lookup"><span data-stu-id="95698-122">-Name</span></span>
<span data-ttu-id="95698-123">Имя подключения виртуального сетевого шлюза, для которого нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="95698-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95698-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95698-124">-ResourceGroupName</span></span>
<span data-ttu-id="95698-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="95698-125">The resource group name.</span></span>

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

### <span data-ttu-id="95698-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="95698-126">-ResourceId</span></span>
<span data-ttu-id="95698-127">Azure resource ID of the VirtualNetworkGatewayConnection, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="95698-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="95698-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="95698-128">-SasUrl</span></span>
<span data-ttu-id="95698-129">URL-адрес SAS для остановки захвата пакетов на виртуальном сетевом шлюзе.</span><span class="sxs-lookup"><span data-stu-id="95698-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="95698-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95698-130">-WhatIf</span></span>
<span data-ttu-id="95698-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95698-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95698-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="95698-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95698-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95698-133">CommonParameters</span></span>
<span data-ttu-id="95698-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95698-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95698-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95698-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95698-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95698-136">INPUTS</span></span>

### <span data-ttu-id="95698-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="95698-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="95698-138">System.String</span><span class="sxs-lookup"><span data-stu-id="95698-138">System.String</span></span>

## <span data-ttu-id="95698-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95698-139">OUTPUTS</span></span>

### <span data-ttu-id="95698-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="95698-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="95698-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95698-141">NOTES</span></span>

## <span data-ttu-id="95698-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95698-142">RELATED LINKS</span></span>
[<span data-ttu-id="95698-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="95698-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)