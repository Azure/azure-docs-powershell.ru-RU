---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 88cbb5417e8a82ede25cc77274294a5dc4f64b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234859"
---
# <span data-ttu-id="9f56e-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f56e-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="9f56e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f56e-102">SYNOPSIS</span></span>
<span data-ttu-id="9f56e-103">Прекращение операции захвата пакетов для подключения VPN</span><span class="sxs-lookup"><span data-stu-id="9f56e-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="9f56e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f56e-104">SYNTAX</span></span>

### <span data-ttu-id="9f56e-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f56e-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-LinkConnectionName <String>] -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f56e-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="9f56e-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-LinkConnectionName <String>]
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f56e-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="9f56e-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> [-LinkConnectionName <String>] -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f56e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f56e-108">DESCRIPTION</span></span>
<span data-ttu-id="9f56e-109">Останавливает операцию захвата пакетов для подключения VPN и отправляет результат по данному SasUrl контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="9f56e-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="9f56e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f56e-110">EXAMPLES</span></span>

### <span data-ttu-id="9f56e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f56e-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="9f56e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9f56e-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="9f56e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f56e-113">PARAMETERS</span></span>

### <span data-ttu-id="9f56e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f56e-114">-AsJob</span></span>
<span data-ttu-id="9f56e-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9f56e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f56e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f56e-116">-DefaultProfile</span></span>
<span data-ttu-id="9f56e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f56e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f56e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f56e-118">-InputObject</span></span>
<span data-ttu-id="9f56e-119">Объект VPN-подключения, для которого нужно запустить сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="9f56e-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="9f56e-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="9f56e-120">-LinkConnectionName</span></span>
<span data-ttu-id="9f56e-121">Имена SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="9f56e-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="9f56e-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9f56e-122">-Name</span></span>
<span data-ttu-id="9f56e-123">Имя VPN-подключения, для которого нужно запустить сбор пакетов.</span><span class="sxs-lookup"><span data-stu-id="9f56e-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f56e-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="9f56e-124">-ParentResourceName</span></span>
<span data-ttu-id="9f56e-125">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f56e-125">The parent resource name.</span></span>

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

### <span data-ttu-id="9f56e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f56e-126">-ResourceGroupName</span></span>
<span data-ttu-id="9f56e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f56e-127">The resource group name.</span></span>

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

### <span data-ttu-id="9f56e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f56e-128">-ResourceId</span></span>
<span data-ttu-id="9f56e-129">Идентификатор ресурса Azure VpnConnection, в котором запускается захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="9f56e-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="9f56e-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="9f56e-130">-SasUrl</span></span>
<span data-ttu-id="9f56e-131">URL-адрес SAS для записи остановленных пакетов в VPN.</span><span class="sxs-lookup"><span data-stu-id="9f56e-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="9f56e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f56e-132">-Confirm</span></span>
<span data-ttu-id="9f56e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f56e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f56e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f56e-134">-WhatIf</span></span>
<span data-ttu-id="9f56e-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f56e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f56e-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f56e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f56e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f56e-137">CommonParameters</span></span>
<span data-ttu-id="9f56e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f56e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f56e-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f56e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f56e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f56e-140">INPUTS</span></span>

### <span data-ttu-id="9f56e-141">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="9f56e-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="9f56e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9f56e-142">System.String</span></span>

## <span data-ttu-id="9f56e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f56e-143">OUTPUTS</span></span>

### <span data-ttu-id="9f56e-144">Microsoft. Azure. Commands. Network. Models. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="9f56e-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="9f56e-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f56e-145">NOTES</span></span>

## <span data-ttu-id="9f56e-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f56e-146">RELATED LINKS</span></span>

[<span data-ttu-id="9f56e-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9f56e-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)