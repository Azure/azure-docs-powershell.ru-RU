---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: f80543b245c59cee7261d062c741788489fb5cb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98412724"
---
# <span data-ttu-id="fa92e-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa92e-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="fa92e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa92e-102">SYNOPSIS</span></span>
<span data-ttu-id="fa92e-103">Остановка операции захвата пакетов для VPN-подключения</span><span class="sxs-lookup"><span data-stu-id="fa92e-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="fa92e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa92e-104">SYNTAX</span></span>

### <span data-ttu-id="fa92e-105">ByVpnConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa92e-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -LinkConnectionName <String> -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa92e-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="fa92e-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> -LinkConnectionName <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa92e-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="fa92e-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> -LinkConnectionName <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa92e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa92e-108">DESCRIPTION</span></span>
<span data-ttu-id="fa92e-109">Остановка операции захвата пакетов через VPN-подключение и отправка результата по заданным sasUrl контейнера хранения.</span><span class="sxs-lookup"><span data-stu-id="fa92e-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="fa92e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa92e-110">EXAMPLES</span></span>

### <span data-ttu-id="fa92e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa92e-111">Example 1</span></span>
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

### <span data-ttu-id="fa92e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa92e-112">Example 2</span></span>
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

## <span data-ttu-id="fa92e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa92e-113">PARAMETERS</span></span>

### <span data-ttu-id="fa92e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa92e-114">-AsJob</span></span>
<span data-ttu-id="fa92e-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fa92e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa92e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa92e-116">-DefaultProfile</span></span>
<span data-ttu-id="fa92e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa92e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa92e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa92e-118">-InputObject</span></span>
<span data-ttu-id="fa92e-119">Объект VPN-подключения, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="fa92e-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="fa92e-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="fa92e-120">-LinkConnectionName</span></span>
<span data-ttu-id="fa92e-121">Имена SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="fa92e-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="fa92e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fa92e-122">-Name</span></span>
<span data-ttu-id="fa92e-123">Имя VPN-подключения, в котором нужно начать захват пакетов.</span><span class="sxs-lookup"><span data-stu-id="fa92e-123">The Vpn connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="fa92e-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fa92e-124">-ParentResourceName</span></span>
<span data-ttu-id="fa92e-125">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa92e-125">The parent resource name.</span></span>

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

### <span data-ttu-id="fa92e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa92e-126">-ResourceGroupName</span></span>
<span data-ttu-id="fa92e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa92e-127">The resource group name.</span></span>

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

### <span data-ttu-id="fa92e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa92e-128">-ResourceId</span></span>
<span data-ttu-id="fa92e-129">Azure resource ID of the VpnConnection where packet capture to be started.</span><span class="sxs-lookup"><span data-stu-id="fa92e-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="fa92e-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="fa92e-130">-SasUrl</span></span>
<span data-ttu-id="fa92e-131">URL-адрес SAS для остановки захвата пакетов в Vpn.</span><span class="sxs-lookup"><span data-stu-id="fa92e-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="fa92e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa92e-132">-Confirm</span></span>
<span data-ttu-id="fa92e-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa92e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa92e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa92e-134">-WhatIf</span></span>
<span data-ttu-id="fa92e-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa92e-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa92e-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fa92e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa92e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa92e-137">CommonParameters</span></span>
<span data-ttu-id="fa92e-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa92e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa92e-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa92e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa92e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa92e-140">INPUTS</span></span>

### <span data-ttu-id="fa92e-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="fa92e-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="fa92e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fa92e-142">System.String</span></span>

## <span data-ttu-id="fa92e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa92e-143">OUTPUTS</span></span>

### <span data-ttu-id="fa92e-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="fa92e-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="fa92e-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa92e-145">NOTES</span></span>

## <span data-ttu-id="fa92e-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa92e-146">RELATED LINKS</span></span>

[<span data-ttu-id="fa92e-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fa92e-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)