---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219833"
---
# <span data-ttu-id="6efa5-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="6efa5-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="6efa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6efa5-102">SYNOPSIS</span></span>
<span data-ttu-id="6efa5-103">Список всех или отдельных устройств, содержащихся в Центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="6efa5-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="6efa5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6efa5-104">SYNTAX</span></span>

### <span data-ttu-id="6efa5-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6efa5-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6efa5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6efa5-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6efa5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6efa5-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6efa5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6efa5-108">DESCRIPTION</span></span>
<span data-ttu-id="6efa5-109">Получите сведения об устройстве iot-концентратора или укаймь все устройства в концентраторе IOT.</span><span class="sxs-lookup"><span data-stu-id="6efa5-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="6efa5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6efa5-110">EXAMPLES</span></span>

### <span data-ttu-id="6efa5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6efa5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="6efa5-112">Показать все устройства в IOT-концентраторе.</span><span class="sxs-lookup"><span data-stu-id="6efa5-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="6efa5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6efa5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="6efa5-114">Получите сведения об устройстве с концентратором IoT.</span><span class="sxs-lookup"><span data-stu-id="6efa5-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="6efa5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6efa5-115">PARAMETERS</span></span>

### <span data-ttu-id="6efa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6efa5-116">-DefaultProfile</span></span>
<span data-ttu-id="6efa5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6efa5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6efa5-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6efa5-118">-DeviceId</span></span>
<span data-ttu-id="6efa5-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="6efa5-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6efa5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6efa5-120">-InputObject</span></span>
<span data-ttu-id="6efa5-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="6efa5-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6efa5-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6efa5-122">-IotHubName</span></span>
<span data-ttu-id="6efa5-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="6efa5-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efa5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6efa5-124">-ResourceGroupName</span></span>
<span data-ttu-id="6efa5-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6efa5-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6efa5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6efa5-126">-ResourceId</span></span>
<span data-ttu-id="6efa5-127">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="6efa5-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6efa5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6efa5-128">CommonParameters</span></span>
<span data-ttu-id="6efa5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6efa5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6efa5-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6efa5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6efa5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6efa5-131">INPUTS</span></span>

### <span data-ttu-id="6efa5-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6efa5-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6efa5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6efa5-133">System.String</span></span>

## <span data-ttu-id="6efa5-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6efa5-134">OUTPUTS</span></span>

### <span data-ttu-id="6efa5-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="6efa5-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="6efa5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span><span class="sxs-lookup"><span data-stu-id="6efa5-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="6efa5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6efa5-137">NOTES</span></span>

## <span data-ttu-id="6efa5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6efa5-138">RELATED LINKS</span></span>
