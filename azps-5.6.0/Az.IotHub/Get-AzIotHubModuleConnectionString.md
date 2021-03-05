---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 739153aebdaf8b089c0d180643056725a85f450a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987944"
---
# <span data-ttu-id="77156-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="77156-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="77156-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77156-102">SYNOPSIS</span></span>
<span data-ttu-id="77156-103">Получите строку подключения конечного модуля устройства IoT в центре IOT.</span><span class="sxs-lookup"><span data-stu-id="77156-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="77156-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="77156-104">SYNTAX</span></span>

### <span data-ttu-id="77156-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77156-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77156-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77156-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77156-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="77156-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77156-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77156-108">DESCRIPTION</span></span>
<span data-ttu-id="77156-109">Строка подключения списка для всех модулей или определенный модуль конечного устройства IoT, которое содержится в Центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="77156-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="77156-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="77156-110">EXAMPLES</span></span>

### <span data-ttu-id="77156-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77156-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="77156-112">Откажите строку подключения всех модулей конечного устройства ioT в центре Iot.</span><span class="sxs-lookup"><span data-stu-id="77156-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="77156-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="77156-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="77156-114">Получить строку подключения дополнительного модуля конечного устройства IoT в центре Iot.</span><span class="sxs-lookup"><span data-stu-id="77156-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="77156-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77156-115">PARAMETERS</span></span>

### <span data-ttu-id="77156-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77156-116">-DefaultProfile</span></span>
<span data-ttu-id="77156-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77156-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77156-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="77156-118">-DeviceId</span></span>
<span data-ttu-id="77156-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="77156-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77156-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77156-120">-InputObject</span></span>
<span data-ttu-id="77156-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="77156-121">IotHub object</span></span>

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

### <span data-ttu-id="77156-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="77156-122">-IotHubName</span></span>
<span data-ttu-id="77156-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="77156-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="77156-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="77156-124">-KeyType</span></span>
<span data-ttu-id="77156-125">Тип ключа политики общего доступа для auth.</span><span class="sxs-lookup"><span data-stu-id="77156-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="77156-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="77156-126">-ModuleId</span></span>
<span data-ttu-id="77156-127">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="77156-127">Target Module Id.</span></span>

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

### <span data-ttu-id="77156-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77156-128">-ResourceGroupName</span></span>
<span data-ttu-id="77156-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="77156-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="77156-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77156-130">-ResourceId</span></span>
<span data-ttu-id="77156-131">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="77156-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="77156-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77156-132">CommonParameters</span></span>
<span data-ttu-id="77156-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77156-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77156-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77156-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77156-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77156-135">INPUTS</span></span>

### <span data-ttu-id="77156-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="77156-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="77156-137">System.String</span><span class="sxs-lookup"><span data-stu-id="77156-137">System.String</span></span>

## <span data-ttu-id="77156-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="77156-138">OUTPUTS</span></span>

### <span data-ttu-id="77156-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="77156-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="77156-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="77156-140">NOTES</span></span>

## <span data-ttu-id="77156-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77156-141">RELATED LINKS</span></span>
