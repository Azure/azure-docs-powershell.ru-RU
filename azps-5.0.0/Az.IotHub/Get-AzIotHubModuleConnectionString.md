---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94258010"
---
# <span data-ttu-id="28b6a-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="28b6a-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="28b6a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="28b6a-103">Получение строки подключения целевого модуля устройства IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="28b6a-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="28b6a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28b6a-104">SYNTAX</span></span>

### <span data-ttu-id="28b6a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28b6a-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28b6a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="28b6a-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28b6a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="28b6a-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28b6a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28b6a-108">DESCRIPTION</span></span>
<span data-ttu-id="28b6a-109">Вывод строки подключения для всех модулей или определенного модуля целевого устройства IoT, содержащегося в центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="28b6a-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="28b6a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28b6a-110">EXAMPLES</span></span>

### <span data-ttu-id="28b6a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="28b6a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="28b6a-112">Показать строку подключения ко всем модулям для целевого устройства IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="28b6a-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="28b6a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="28b6a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="28b6a-114">Получение строки подключения к дополнительным модулям для целевого устройства IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="28b6a-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="28b6a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28b6a-115">PARAMETERS</span></span>

### <span data-ttu-id="28b6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b6a-116">-DefaultProfile</span></span>
<span data-ttu-id="28b6a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28b6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28b6a-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="28b6a-118">-DeviceId</span></span>
<span data-ttu-id="28b6a-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="28b6a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="28b6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="28b6a-120">-InputObject</span></span>
<span data-ttu-id="28b6a-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="28b6a-121">IotHub object</span></span>

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

### <span data-ttu-id="28b6a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="28b6a-122">-IotHubName</span></span>
<span data-ttu-id="28b6a-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="28b6a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="28b6a-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="28b6a-124">-KeyType</span></span>
<span data-ttu-id="28b6a-125">Тип ключа политики общего доступа для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="28b6a-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="28b6a-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="28b6a-126">-ModuleId</span></span>
<span data-ttu-id="28b6a-127">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="28b6a-127">Target Module Id.</span></span>

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

### <span data-ttu-id="28b6a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b6a-128">-ResourceGroupName</span></span>
<span data-ttu-id="28b6a-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="28b6a-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="28b6a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="28b6a-130">-ResourceId</span></span>
<span data-ttu-id="28b6a-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="28b6a-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="28b6a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b6a-132">CommonParameters</span></span>
<span data-ttu-id="28b6a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28b6a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b6a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b6a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b6a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28b6a-135">INPUTS</span></span>

### <span data-ttu-id="28b6a-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="28b6a-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="28b6a-137">System. String</span><span class="sxs-lookup"><span data-stu-id="28b6a-137">System.String</span></span>

## <span data-ttu-id="28b6a-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28b6a-138">OUTPUTS</span></span>

### <span data-ttu-id="28b6a-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="28b6a-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="28b6a-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="28b6a-140">NOTES</span></span>

## <span data-ttu-id="28b6a-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28b6a-141">RELATED LINKS</span></span>
