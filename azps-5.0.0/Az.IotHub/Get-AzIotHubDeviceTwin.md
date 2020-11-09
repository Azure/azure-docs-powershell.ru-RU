---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceTwin.md
ms.openlocfilehash: 6d8397ff8b22895614c67592460eadf76aa3fb92
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247749"
---
# <span data-ttu-id="36905-101">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="36905-101">Get-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="36905-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36905-102">SYNOPSIS</span></span>
<span data-ttu-id="36905-103">Возвращает двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="36905-103">Gets a device twin.</span></span>

## <span data-ttu-id="36905-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36905-104">SYNTAX</span></span>

### <span data-ttu-id="36905-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36905-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36905-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36905-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36905-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="36905-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36905-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36905-108">DESCRIPTION</span></span>
<span data-ttu-id="36905-109">Возвращает двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="36905-109">Gets a device twin.</span></span> <span data-ttu-id="36905-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="36905-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="36905-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36905-111">EXAMPLES</span></span>

### <span data-ttu-id="36905-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36905-112">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"
```

<span data-ttu-id="36905-113">Возвращает объект двойной устройства.</span><span class="sxs-lookup"><span data-stu-id="36905-113">Returns the device twin object.</span></span>

## <span data-ttu-id="36905-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36905-114">PARAMETERS</span></span>

### <span data-ttu-id="36905-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36905-115">-DefaultProfile</span></span>
<span data-ttu-id="36905-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36905-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36905-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="36905-117">-DeviceId</span></span>
<span data-ttu-id="36905-118">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="36905-118">Target Device Id.</span></span>

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

### <span data-ttu-id="36905-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36905-119">-InputObject</span></span>
<span data-ttu-id="36905-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="36905-120">IotHub object</span></span>

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

### <span data-ttu-id="36905-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="36905-121">-IotHubName</span></span>
<span data-ttu-id="36905-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="36905-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="36905-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36905-123">-ResourceGroupName</span></span>
<span data-ttu-id="36905-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="36905-124">Name of the Resource Group</span></span>

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

### <span data-ttu-id="36905-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36905-125">-ResourceId</span></span>
<span data-ttu-id="36905-126">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="36905-126">IotHub Resource Id</span></span>

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

### <span data-ttu-id="36905-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36905-127">CommonParameters</span></span>
<span data-ttu-id="36905-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36905-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36905-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36905-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36905-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36905-130">INPUTS</span></span>

### <span data-ttu-id="36905-131">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="36905-131">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="36905-132">System. String</span><span class="sxs-lookup"><span data-stu-id="36905-132">System.String</span></span>

## <span data-ttu-id="36905-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36905-133">OUTPUTS</span></span>

### <span data-ttu-id="36905-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="36905-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceTwin</span></span>

## <span data-ttu-id="36905-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="36905-135">NOTES</span></span>

## <span data-ttu-id="36905-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36905-136">RELATED LINKS</span></span>