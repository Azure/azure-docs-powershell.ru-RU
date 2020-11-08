---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduleconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleConnectionString.md
ms.openlocfilehash: 30926eaad6447f109b1755d419be0b3931a76054
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073383"
---
# <span data-ttu-id="4f15f-101">Get-AzIotHubModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="4f15f-101">Get-AzIotHubModuleConnectionString</span></span>

## <span data-ttu-id="4f15f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4f15f-102">SYNOPSIS</span></span>
<span data-ttu-id="4f15f-103">Получение строки подключения целевого модуля устройства IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="4f15f-103">Get the connection string of a target IoT device module in an Iot Hub.</span></span>

## <span data-ttu-id="4f15f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4f15f-104">SYNTAX</span></span>

### <span data-ttu-id="4f15f-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4f15f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f15f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4f15f-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleConnectionString [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f15f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4f15f-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleConnectionString [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f15f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f15f-108">DESCRIPTION</span></span>
<span data-ttu-id="4f15f-109">Вывод строки подключения для всех модулей или определенного модуля целевого устройства IoT, содержащегося в центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="4f15f-109">List connection string of all modules or a specified module of a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="4f15f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4f15f-110">EXAMPLES</span></span>

### <span data-ttu-id="4f15f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4f15f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Deviceid "myDevice1"

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******     
module2   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module2;x509=true
```

<span data-ttu-id="4f15f-112">Показать строку подключения ко всем модулям для целевого устройства IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="4f15f-112">Show all modules connection string of a target IoT device in an Iot Hub.</span></span>

### <span data-ttu-id="4f15f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4f15f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubMCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "module1" -KeyType secondary

Module Id Connection String
--------- -----------------
module1   HostName=myiothub.azure-devices.net;DeviceId=myDevice1;ModuleId=module1;SharedAccessKey=/X4yj******
```

<span data-ttu-id="4f15f-114">Получение строки подключения к дополнительным модулям для целевого устройства IoT в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="4f15f-114">Get the secondary module connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="4f15f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4f15f-115">PARAMETERS</span></span>

### <span data-ttu-id="4f15f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f15f-116">-DefaultProfile</span></span>
<span data-ttu-id="4f15f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4f15f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f15f-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4f15f-118">-DeviceId</span></span>
<span data-ttu-id="4f15f-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="4f15f-119">Target Device Id.</span></span>

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

### <span data-ttu-id="4f15f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f15f-120">-InputObject</span></span>
<span data-ttu-id="4f15f-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="4f15f-121">IotHub object</span></span>

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

### <span data-ttu-id="4f15f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4f15f-122">-IotHubName</span></span>
<span data-ttu-id="4f15f-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="4f15f-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4f15f-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="4f15f-124">-KeyType</span></span>
<span data-ttu-id="4f15f-125">Тип ключа политики общего доступа для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4f15f-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="4f15f-126">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="4f15f-126">-ModuleId</span></span>
<span data-ttu-id="4f15f-127">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="4f15f-127">Target Module Id.</span></span>

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

### <span data-ttu-id="4f15f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f15f-128">-ResourceGroupName</span></span>
<span data-ttu-id="4f15f-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4f15f-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4f15f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f15f-130">-ResourceId</span></span>
<span data-ttu-id="4f15f-131">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="4f15f-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4f15f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f15f-132">CommonParameters</span></span>
<span data-ttu-id="4f15f-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4f15f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f15f-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f15f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f15f-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4f15f-135">INPUTS</span></span>

### <span data-ttu-id="4f15f-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4f15f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4f15f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4f15f-137">System.String</span></span>

## <span data-ttu-id="4f15f-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4f15f-138">OUTPUTS</span></span>

### <span data-ttu-id="4f15f-139">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleConnectionString</span><span class="sxs-lookup"><span data-stu-id="4f15f-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleConnectionString</span></span>

## <span data-ttu-id="4f15f-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4f15f-140">NOTES</span></span>

## <span data-ttu-id="4f15f-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4f15f-141">RELATED LINKS</span></span>
