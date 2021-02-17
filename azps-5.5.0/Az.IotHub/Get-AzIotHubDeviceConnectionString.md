---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219817"
---
# <span data-ttu-id="75a5e-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="75a5e-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="75a5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75a5e-102">SYNOPSIS</span></span>
<span data-ttu-id="75a5e-103">Получите строку подключения конечного устройства IoT в концентраторе IOT.</span><span class="sxs-lookup"><span data-stu-id="75a5e-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="75a5e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="75a5e-104">SYNTAX</span></span>

### <span data-ttu-id="75a5e-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75a5e-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a5e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="75a5e-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="75a5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="75a5e-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75a5e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75a5e-108">DESCRIPTION</span></span>
<span data-ttu-id="75a5e-109">Строка подключения списка всех устройств или целевое устройство IoT, содержающееся в Центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="75a5e-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="75a5e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="75a5e-110">EXAMPLES</span></span>

### <span data-ttu-id="75a5e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="75a5e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="75a5e-112">Откажите строку подключения для всех устройств в IOT-концентраторе.</span><span class="sxs-lookup"><span data-stu-id="75a5e-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="75a5e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="75a5e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="75a5e-114">Получить вторичную строку подключения устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="75a5e-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="75a5e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75a5e-115">PARAMETERS</span></span>

### <span data-ttu-id="75a5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75a5e-116">-DefaultProfile</span></span>
<span data-ttu-id="75a5e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75a5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75a5e-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="75a5e-118">-DeviceId</span></span>
<span data-ttu-id="75a5e-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="75a5e-119">Target Device Id.</span></span>

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

### <span data-ttu-id="75a5e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75a5e-120">-InputObject</span></span>
<span data-ttu-id="75a5e-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="75a5e-121">IotHub object</span></span>

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

### <span data-ttu-id="75a5e-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="75a5e-122">-IotHubName</span></span>
<span data-ttu-id="75a5e-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="75a5e-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="75a5e-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="75a5e-124">-KeyType</span></span>
<span data-ttu-id="75a5e-125">Тип ключа политики общего доступа для auth.</span><span class="sxs-lookup"><span data-stu-id="75a5e-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75a5e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75a5e-126">-ResourceGroupName</span></span>
<span data-ttu-id="75a5e-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="75a5e-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="75a5e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75a5e-128">-ResourceId</span></span>
<span data-ttu-id="75a5e-129">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="75a5e-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="75a5e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75a5e-130">CommonParameters</span></span>
<span data-ttu-id="75a5e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75a5e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75a5e-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75a5e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75a5e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="75a5e-133">INPUTS</span></span>

### <span data-ttu-id="75a5e-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="75a5e-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="75a5e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="75a5e-135">System.String</span></span>

## <span data-ttu-id="75a5e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="75a5e-136">OUTPUTS</span></span>

### <span data-ttu-id="75a5e-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="75a5e-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="75a5e-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="75a5e-138">NOTES</span></span>

## <span data-ttu-id="75a5e-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75a5e-139">RELATED LINKS</span></span>
