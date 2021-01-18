---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubQuery.md
ms.openlocfilehash: 6445e6281ff69f4eef54a5694f953beaa08ad098
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518589"
---
# <span data-ttu-id="5c1ce-101">Invoke-AzIotHubQuery</span><span class="sxs-lookup"><span data-stu-id="5c1ce-101">Invoke-AzIotHubQuery</span></span>

## <span data-ttu-id="5c1ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1ce-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1ce-103">Выполнив запрос к концентратору IoT, можно использовать SQL-язык.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-103">Query an IoT Hub using a powerful SQL-like language.</span></span>

## <span data-ttu-id="5c1ce-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5c1ce-104">SYNTAX</span></span>

### <span data-ttu-id="5c1ce-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c1ce-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubQuery [-ResourceGroupName] <String> [-IotHubName] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1ce-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5c1ce-106">InputObjectSet</span></span>
```
Invoke-AzIotHubQuery [-InputObject] <PSIotHub> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c1ce-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5c1ce-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubQuery [-ResourceId] <String> [-Query] <String> [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c1ce-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c1ce-108">DESCRIPTION</span></span>
<span data-ttu-id="5c1ce-109">Вы можете запрашивать данные об устройствах и модулях, заданиях и маршрутах сообщений SQL на одном языке с помощью мощного SQL.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-109">Query an IoT Hub using a powerful SQL-like language to retrieve information regarding device and module twins, jobs and message routing.</span></span>
<span data-ttu-id="5c1ce-110">Дополнительные https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language сведения см. в этой области.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-query-language for more information.</span></span>

## <span data-ttu-id="5c1ce-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5c1ce-111">EXAMPLES</span></span>

### <span data-ttu-id="5c1ce-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c1ce-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices"
```

<span data-ttu-id="5c1ce-113">Запрос на все устройства в концентраторе Azure IoT.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-113">Query all device twin data in an Azure IoT Hub.</span></span>

### <span data-ttu-id="5c1ce-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5c1ce-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Query "select * from devices.modules where devices.deviceId = 'myDevice1'" -Top 2
```

<span data-ttu-id="5c1ce-115">Запрос 2 модуля позволяет получить данные на целевом устройстве.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-115">Query top 2 module twin data on a target device.</span></span>

## <span data-ttu-id="5c1ce-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c1ce-116">PARAMETERS</span></span>

### <span data-ttu-id="5c1ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1ce-117">-DefaultProfile</span></span>
<span data-ttu-id="5c1ce-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c1ce-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c1ce-119">-InputObject</span></span>
<span data-ttu-id="5c1ce-120">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="5c1ce-120">IotHub object</span></span>

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

### <span data-ttu-id="5c1ce-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5c1ce-121">-IotHubName</span></span>
<span data-ttu-id="5c1ce-122">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="5c1ce-122">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="5c1ce-123">-Query</span><span class="sxs-lookup"><span data-stu-id="5c1ce-123">-Query</span></span>
<span data-ttu-id="5c1ce-124">Запрос пользователя для выполнения.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-124">User query to be executed.</span></span>

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

### <span data-ttu-id="5c1ce-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1ce-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c1ce-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5c1ce-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5c1ce-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c1ce-127">-ResourceId</span></span>
<span data-ttu-id="5c1ce-128">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="5c1ce-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="5c1ce-129">-Top</span><span class="sxs-lookup"><span data-stu-id="5c1ce-129">-Top</span></span>
<span data-ttu-id="5c1ce-130">Максимальное количество возвращаемых элементов.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-130">Maximum number of elements to return.</span></span>
<span data-ttu-id="5c1ce-131">По умолчанию у запроса нет cap.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-131">By default query has no cap.</span></span>

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

### <span data-ttu-id="5c1ce-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c1ce-132">-Confirm</span></span>
<span data-ttu-id="5c1ce-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c1ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c1ce-134">-WhatIf</span></span>
<span data-ttu-id="5c1ce-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c1ce-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c1ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1ce-137">CommonParameters</span></span>
<span data-ttu-id="5c1ce-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c1ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1ce-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1ce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1ce-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5c1ce-140">INPUTS</span></span>

### <span data-ttu-id="5c1ce-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5c1ce-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5c1ce-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1ce-142">System.String</span></span>

## <span data-ttu-id="5c1ce-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5c1ce-143">OUTPUTS</span></span>

### <span data-ttu-id="5c1ce-144">System.String</span><span class="sxs-lookup"><span data-stu-id="5c1ce-144">System.String</span></span>

## <span data-ttu-id="5c1ce-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5c1ce-145">NOTES</span></span>

## <span data-ttu-id="5c1ce-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c1ce-146">RELATED LINKS</span></span>
