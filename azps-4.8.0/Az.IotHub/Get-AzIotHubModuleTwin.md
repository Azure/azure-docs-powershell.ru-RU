---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModuleTwin.md
ms.openlocfilehash: 5a033bd0d43f614dd7fa1dd45cb3581d6808309d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242741"
---
# <span data-ttu-id="fe1d1-101">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="fe1d1-101">Get-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="fe1d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe1d1-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1d1-103">Получает двойной модуля устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-103">Gets an IoT device module twin.</span></span>

## <span data-ttu-id="fe1d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe1d1-104">SYNTAX</span></span>

### <span data-ttu-id="fe1d1-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe1d1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe1d1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fe1d1-106">InputObjectSet</span></span>
```
Get-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fe1d1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fe1d1-107">ResourceIdSet</span></span>
```
Get-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe1d1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1d1-108">DESCRIPTION</span></span>
<span data-ttu-id="fe1d1-109">Получает двойной модуля устройства IoT.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-109">Gets an IoT device module twin.</span></span> <span data-ttu-id="fe1d1-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="fe1d1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe1d1-111">EXAMPLES</span></span>

### <span data-ttu-id="fe1d1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe1d1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"
```

<span data-ttu-id="fe1d1-113">Возвращает объект двойной модуля устройства.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-113">Returns the device module twin object.</span></span>

## <span data-ttu-id="fe1d1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1d1-114">PARAMETERS</span></span>

### <span data-ttu-id="fe1d1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1d1-115">-DefaultProfile</span></span>
<span data-ttu-id="fe1d1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe1d1-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fe1d1-117">-DeviceId</span></span>
<span data-ttu-id="fe1d1-118">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-118">Target Device Id.</span></span>

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

### <span data-ttu-id="fe1d1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe1d1-119">-InputObject</span></span>
<span data-ttu-id="fe1d1-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="fe1d1-120">IotHub object</span></span>

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

### <span data-ttu-id="fe1d1-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fe1d1-121">-IotHubName</span></span>
<span data-ttu-id="fe1d1-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="fe1d1-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fe1d1-123">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="fe1d1-123">-ModuleId</span></span>
<span data-ttu-id="fe1d1-124">Идентификатор целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-124">Target Module Id.</span></span>

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

### <span data-ttu-id="fe1d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe1d1-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="fe1d1-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fe1d1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe1d1-127">-ResourceId</span></span>
<span data-ttu-id="fe1d1-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="fe1d1-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fe1d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1d1-129">CommonParameters</span></span>
<span data-ttu-id="fe1d1-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe1d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1d1-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1d1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1d1-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe1d1-132">INPUTS</span></span>

### <span data-ttu-id="fe1d1-133">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fe1d1-133">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fe1d1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fe1d1-134">System.String</span></span>

## <span data-ttu-id="fe1d1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1d1-135">OUTPUTS</span></span>

### <span data-ttu-id="fe1d1-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="fe1d1-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="fe1d1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe1d1-137">NOTES</span></span>

## <span data-ttu-id="fe1d1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1d1-138">RELATED LINKS</span></span>
