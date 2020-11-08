---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243366"
---
# <span data-ttu-id="a4a5b-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="a4a5b-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="a4a5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4a5b-102">SYNOPSIS</span></span>
<span data-ttu-id="a4a5b-103">В этой статье перечислены все устройства или определенное устройство, содержащееся в центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="a4a5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4a5b-104">SYNTAX</span></span>

### <span data-ttu-id="a4a5b-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4a5b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4a5b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4a5b-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4a5b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4a5b-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4a5b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4a5b-108">DESCRIPTION</span></span>
<span data-ttu-id="a4a5b-109">Получение подробных сведений об устройстве Интернет-концентратора вещей или список всех устройств в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="a4a5b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4a5b-110">EXAMPLES</span></span>

### <span data-ttu-id="a4a5b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4a5b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="a4a5b-112">Показать все устройства в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="a4a5b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a4a5b-113">Example 2</span></span>
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

<span data-ttu-id="a4a5b-114">Получение подробных сведений об устройстве IoT центр Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="a4a5b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4a5b-115">PARAMETERS</span></span>

### <span data-ttu-id="a4a5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4a5b-116">-DefaultProfile</span></span>
<span data-ttu-id="a4a5b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4a5b-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a4a5b-118">-DeviceId</span></span>
<span data-ttu-id="a4a5b-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-119">Target Device Id.</span></span>

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

### <span data-ttu-id="a4a5b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4a5b-120">-InputObject</span></span>
<span data-ttu-id="a4a5b-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="a4a5b-121">IotHub object</span></span>

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

### <span data-ttu-id="a4a5b-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a4a5b-122">-IotHubName</span></span>
<span data-ttu-id="a4a5b-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="a4a5b-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a4a5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4a5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a4a5b-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a4a5b-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a4a5b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4a5b-126">-ResourceId</span></span>
<span data-ttu-id="a4a5b-127">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="a4a5b-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a4a5b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4a5b-128">CommonParameters</span></span>
<span data-ttu-id="a4a5b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4a5b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4a5b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4a5b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4a5b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4a5b-131">INPUTS</span></span>

### <span data-ttu-id="a4a5b-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a4a5b-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a4a5b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a4a5b-133">System.String</span></span>

## <span data-ttu-id="a4a5b-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4a5b-134">OUTPUTS</span></span>

### <span data-ttu-id="a4a5b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="a4a5b-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="a4a5b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEvices []</span><span class="sxs-lookup"><span data-stu-id="a4a5b-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="a4a5b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4a5b-137">NOTES</span></span>

## <span data-ttu-id="a4a5b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4a5b-138">RELATED LINKS</span></span>