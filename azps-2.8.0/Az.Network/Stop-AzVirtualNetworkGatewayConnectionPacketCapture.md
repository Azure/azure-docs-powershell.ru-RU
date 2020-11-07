---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 791b6d74049aeec24e67ca29f5fae990f511908d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904313"
---
# <span data-ttu-id="6967b-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6967b-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="6967b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6967b-102">SYNOPSIS</span></span>
<span data-ttu-id="6967b-103">Остановить операцию захвата пакетов на подключении к шлюзу виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="6967b-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="6967b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6967b-104">SYNTAX</span></span>

### <span data-ttu-id="6967b-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6967b-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6967b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6967b-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6967b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6967b-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6967b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6967b-108">DESCRIPTION</span></span>
<span data-ttu-id="6967b-109">Останавливает операцию захвата пакетов на подключении к шлюзу виртуальной сети и отправляет результат по данному SasUrl контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="6967b-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="6967b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6967b-110">EXAMPLES</span></span>

### <span data-ttu-id="6967b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6967b-111">Example 1</span></span>
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

### <span data-ttu-id="6967b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6967b-112">Example 2</span></span>
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

## <span data-ttu-id="6967b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6967b-113">PARAMETERS</span></span>

### <span data-ttu-id="6967b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6967b-114">-AsJob</span></span>
<span data-ttu-id="6967b-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6967b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6967b-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6967b-116">-Confirm</span></span>
<span data-ttu-id="6967b-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6967b-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6967b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6967b-118">-DefaultProfile</span></span>
<span data-ttu-id="6967b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6967b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6967b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6967b-120">-InputObject</span></span>
<span data-ttu-id="6967b-121">Объект подключения к шлюзу виртуальной сети, для которого необходимо запустить сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="6967b-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="6967b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6967b-122">-Name</span></span>
<span data-ttu-id="6967b-123">Имя подключения к шлюзу виртуальной сети, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="6967b-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="6967b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6967b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6967b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6967b-125">The resource group name.</span></span>

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

### <span data-ttu-id="6967b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6967b-126">-ResourceId</span></span>
<span data-ttu-id="6967b-127">Идентификатор ресурса Azure VirtualNetworkGatewayConnection, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="6967b-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="6967b-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="6967b-128">-SasUrl</span></span>
<span data-ttu-id="6967b-129">URL-адрес SAS для захвата остановленных пакетов на шлюзе виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6967b-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="6967b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6967b-130">-WhatIf</span></span>
<span data-ttu-id="6967b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6967b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6967b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6967b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6967b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6967b-133">CommonParameters</span></span>
<span data-ttu-id="6967b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6967b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6967b-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6967b-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6967b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6967b-136">INPUTS</span></span>

### <span data-ttu-id="6967b-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6967b-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="6967b-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6967b-138">System.String</span></span>

## <span data-ttu-id="6967b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6967b-139">OUTPUTS</span></span>

### <span data-ttu-id="6967b-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="6967b-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="6967b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="6967b-141">NOTES</span></span>

## <span data-ttu-id="6967b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6967b-142">RELATED LINKS</span></span>
[<span data-ttu-id="6967b-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6967b-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)