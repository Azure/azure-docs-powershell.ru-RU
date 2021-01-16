---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322395"
---
# <span data-ttu-id="6acb6-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="6acb6-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="6acb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6acb6-102">SYNOPSIS</span></span>
<span data-ttu-id="6acb6-103">Удалите модули на целевом устройстве ioT в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="6acb6-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6acb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6acb6-104">SYNTAX</span></span>

### <span data-ttu-id="6acb6-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6acb6-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6acb6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6acb6-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6acb6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="6acb6-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6acb6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6acb6-108">DESCRIPTION</span></span>
<span data-ttu-id="6acb6-109">Удалите модули на целевом устройстве ioT в центре IoT.</span><span class="sxs-lookup"><span data-stu-id="6acb6-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="6acb6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6acb6-110">EXAMPLES</span></span>

### <span data-ttu-id="6acb6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6acb6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="6acb6-112">Удалите модуль устройства IOT.</span><span class="sxs-lookup"><span data-stu-id="6acb6-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="6acb6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6acb6-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="6acb6-114">Удалите все модули IOT-устройств.</span><span class="sxs-lookup"><span data-stu-id="6acb6-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="6acb6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6acb6-115">PARAMETERS</span></span>

### <span data-ttu-id="6acb6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6acb6-116">-DefaultProfile</span></span>
<span data-ttu-id="6acb6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6acb6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6acb6-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="6acb6-118">-DeviceId</span></span>
<span data-ttu-id="6acb6-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="6acb6-119">Target Device Id.</span></span>

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

### <span data-ttu-id="6acb6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6acb6-120">-InputObject</span></span>
<span data-ttu-id="6acb6-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="6acb6-121">IotHub object</span></span>

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

### <span data-ttu-id="6acb6-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6acb6-122">-IotHubName</span></span>
<span data-ttu-id="6acb6-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="6acb6-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6acb6-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="6acb6-124">-ModuleId</span></span>
<span data-ttu-id="6acb6-125">ИД целевого модуля.</span><span class="sxs-lookup"><span data-stu-id="6acb6-125">Target Module Id.</span></span>

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

### <span data-ttu-id="6acb6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6acb6-126">-PassThru</span></span>
<span data-ttu-id="6acb6-127">Возвращает объект boolean.</span><span class="sxs-lookup"><span data-stu-id="6acb6-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="6acb6-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6acb6-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6acb6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6acb6-129">-ResourceGroupName</span></span>
<span data-ttu-id="6acb6-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6acb6-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6acb6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6acb6-131">-ResourceId</span></span>
<span data-ttu-id="6acb6-132">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="6acb6-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6acb6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6acb6-133">-Confirm</span></span>
<span data-ttu-id="6acb6-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acb6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6acb6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acb6-135">-WhatIf</span></span>
<span data-ttu-id="6acb6-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6acb6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6acb6-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6acb6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6acb6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acb6-138">CommonParameters</span></span>
<span data-ttu-id="6acb6-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6acb6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acb6-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6acb6-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acb6-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6acb6-141">INPUTS</span></span>

### <span data-ttu-id="6acb6-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6acb6-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6acb6-143">System.String</span><span class="sxs-lookup"><span data-stu-id="6acb6-143">System.String</span></span>

## <span data-ttu-id="6acb6-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6acb6-144">OUTPUTS</span></span>

### <span data-ttu-id="6acb6-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6acb6-145">System.Boolean</span></span>

## <span data-ttu-id="6acb6-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6acb6-146">NOTES</span></span>

## <span data-ttu-id="6acb6-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6acb6-147">RELATED LINKS</span></span>
