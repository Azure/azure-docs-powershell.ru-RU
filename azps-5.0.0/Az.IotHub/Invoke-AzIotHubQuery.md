---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250255"
---
# <span data-ttu-id="136c9-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="136c9-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="136c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="136c9-102">SYNOPSIS</span></span>
<span data-ttu-id="136c9-103">Запросите центр Интернета вещей с помощью мощного языка, похожего на SQL.</span><span class="sxs-lookup"><span data-stu-id="136c9-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="136c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="136c9-104">SYNTAX</span></span>

### <span data-ttu-id="136c9-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="136c9-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="136c9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="136c9-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="136c9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="136c9-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="136c9-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="136c9-108">DESCRIPTION</span></span>
<span data-ttu-id="136c9-109">Запросите центр Интернета вещей с помощью мощного языкового языка SQL для получения информации о устройствах и Twins, заданиях и маршрутизации сообщений.</span><span class="sxs-lookup"><span data-stu-id="136c9-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="136c9-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-languageДля получения дополнительных сведений ознакомьтесь с дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="136c9-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="136c9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="136c9-111">EXAMPLES</span></span>

### <span data-ttu-id="136c9-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="136c9-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="136c9-113">Запросите данные двойной устройств в центре Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="136c9-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="136c9-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="136c9-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="136c9-115">Запросите первые 2 модуля двойной данные на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="136c9-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="136c9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="136c9-116">PARAMETERS</span></span>

### <span data-ttu-id="136c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136c9-117">-DefaultProfile</span></span>
<span data-ttu-id="136c9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="136c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="136c9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="136c9-119">-InputObject</span></span>
<span data-ttu-id="136c9-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="136c9-120">IotHub object</span></span>

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

### <span data-ttu-id="136c9-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="136c9-121">-IotHubName</span></span>
<span data-ttu-id="136c9-122">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="136c9-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="136c9-123">-Query</span><span class="sxs-lookup"><span data-stu-id="136c9-123">-Query</span></span>
<span data-ttu-id="136c9-124">Пользовательский запрос для выполнения.</span><span class="sxs-lookup"><span data-stu-id="136c9-124">User query to be executed.</span></span>

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

### <span data-ttu-id="136c9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="136c9-125">-ResourceGroupName</span></span>
<span data-ttu-id="136c9-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="136c9-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="136c9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="136c9-127">-ResourceId</span></span>
<span data-ttu-id="136c9-128">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="136c9-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="136c9-129">-Top</span><span class="sxs-lookup"><span data-stu-id="136c9-129">-Top</span></span>
<span data-ttu-id="136c9-130">Максимальное количество возвращаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="136c9-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="136c9-131">По умолчанию запрос не имеет политики.</span><span class="sxs-lookup"><span data-stu-id="136c9-131">By default query has no cap.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136c9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="136c9-132">-Confirm</span></span>
<span data-ttu-id="136c9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="136c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="136c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="136c9-134">-WhatIf</span></span>
<span data-ttu-id="136c9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="136c9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="136c9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="136c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="136c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136c9-137">CommonParameters</span></span>
<span data-ttu-id="136c9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="136c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136c9-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136c9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136c9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="136c9-140">INPUTS</span></span>

### <span data-ttu-id="136c9-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="136c9-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="136c9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="136c9-142">System.String</span></span>

## <span data-ttu-id="136c9-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="136c9-143">OUTPUTS</span></span>

### <span data-ttu-id="136c9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="136c9-144">System.String</span></span>

## <span data-ttu-id="136c9-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="136c9-145">NOTES</span></span>

## <span data-ttu-id="136c9-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="136c9-146">RELATED LINKS</span></span>
