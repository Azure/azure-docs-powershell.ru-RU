---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394892"
---
# <span data-ttu-id="af9fb-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="af9fb-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="af9fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="af9fb-103">Удалите устройство из концентратора IoT.</span><span class="sxs-lookup"><span data-stu-id="af9fb-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="af9fb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="af9fb-104">SYNTAX</span></span>

### <span data-ttu-id="af9fb-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="af9fb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9fb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af9fb-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9fb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af9fb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9fb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af9fb-108">DESCRIPTION</span></span>
<span data-ttu-id="af9fb-109">Удалите все устройства или отдельные устройства из IOT-концентратора.</span><span class="sxs-lookup"><span data-stu-id="af9fb-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="af9fb-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="af9fb-110">EXAMPLES</span></span>

### <span data-ttu-id="af9fb-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="af9fb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="af9fb-112">Удалите все устройства IOT-концентратора.</span><span class="sxs-lookup"><span data-stu-id="af9fb-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="af9fb-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="af9fb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="af9fb-114">Удалите устройство IOT-концентратора.</span><span class="sxs-lookup"><span data-stu-id="af9fb-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="af9fb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af9fb-115">PARAMETERS</span></span>

### <span data-ttu-id="af9fb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9fb-116">-DefaultProfile</span></span>
<span data-ttu-id="af9fb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af9fb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9fb-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="af9fb-118">-DeviceId</span></span>
<span data-ttu-id="af9fb-119">ИД целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="af9fb-119">Target Device Id.</span></span>

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

### <span data-ttu-id="af9fb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9fb-120">-InputObject</span></span>
<span data-ttu-id="af9fb-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="af9fb-121">IotHub object</span></span>

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

### <span data-ttu-id="af9fb-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="af9fb-122">-IotHubName</span></span>
<span data-ttu-id="af9fb-123">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="af9fb-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="af9fb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af9fb-124">-PassThru</span></span>
<span data-ttu-id="af9fb-125">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="af9fb-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="af9fb-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="af9fb-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="af9fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="af9fb-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="af9fb-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="af9fb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9fb-129">-ResourceId</span></span>
<span data-ttu-id="af9fb-130">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="af9fb-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="af9fb-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="af9fb-131">-Confirm</span></span>
<span data-ttu-id="af9fb-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="af9fb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9fb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9fb-133">-WhatIf</span></span>
<span data-ttu-id="af9fb-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af9fb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9fb-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="af9fb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9fb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9fb-136">CommonParameters</span></span>
<span data-ttu-id="af9fb-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9fb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9fb-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af9fb-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9fb-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="af9fb-139">INPUTS</span></span>

### <span data-ttu-id="af9fb-140">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="af9fb-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="af9fb-141">System.String</span><span class="sxs-lookup"><span data-stu-id="af9fb-141">System.String</span></span>

## <span data-ttu-id="af9fb-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="af9fb-142">OUTPUTS</span></span>

### <span data-ttu-id="af9fb-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="af9fb-143">System.Boolean</span></span>

## <span data-ttu-id="af9fb-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="af9fb-144">NOTES</span></span>

## <span data-ttu-id="af9fb-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af9fb-145">RELATED LINKS</span></span>
