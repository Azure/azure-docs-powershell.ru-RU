---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236229"
---
# <span data-ttu-id="df54a-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="df54a-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="df54a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df54a-102">SYNOPSIS</span></span>
<span data-ttu-id="df54a-103">Удаление устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="df54a-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="df54a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df54a-104">SYNTAX</span></span>

### <span data-ttu-id="df54a-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df54a-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df54a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df54a-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df54a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df54a-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df54a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df54a-108">DESCRIPTION</span></span>
<span data-ttu-id="df54a-109">Удаление всех устройств или определенного устройства из центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="df54a-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="df54a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df54a-110">EXAMPLES</span></span>

### <span data-ttu-id="df54a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df54a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="df54a-112">Удалите все устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="df54a-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="df54a-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="df54a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="df54a-114">Удаление устройства центра Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="df54a-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="df54a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df54a-115">PARAMETERS</span></span>

### <span data-ttu-id="df54a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df54a-116">-DefaultProfile</span></span>
<span data-ttu-id="df54a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df54a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df54a-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="df54a-118">-DeviceId</span></span>
<span data-ttu-id="df54a-119">Идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="df54a-119">Target Device Id.</span></span>

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

### <span data-ttu-id="df54a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df54a-120">-InputObject</span></span>
<span data-ttu-id="df54a-121">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="df54a-121">IotHub object</span></span>

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

### <span data-ttu-id="df54a-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="df54a-122">-IotHubName</span></span>
<span data-ttu-id="df54a-123">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="df54a-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="df54a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df54a-124">-PassThru</span></span>
<span data-ttu-id="df54a-125">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="df54a-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="df54a-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="df54a-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="df54a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df54a-127">-ResourceGroupName</span></span>
<span data-ttu-id="df54a-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="df54a-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="df54a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df54a-129">-ResourceId</span></span>
<span data-ttu-id="df54a-130">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="df54a-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="df54a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df54a-131">-Confirm</span></span>
<span data-ttu-id="df54a-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df54a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df54a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df54a-133">-WhatIf</span></span>
<span data-ttu-id="df54a-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df54a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df54a-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df54a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df54a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df54a-136">CommonParameters</span></span>
<span data-ttu-id="df54a-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df54a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df54a-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df54a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df54a-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df54a-139">INPUTS</span></span>

### <span data-ttu-id="df54a-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="df54a-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="df54a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="df54a-141">System.String</span></span>

## <span data-ttu-id="df54a-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df54a-142">OUTPUTS</span></span>

### <span data-ttu-id="df54a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df54a-143">System.Boolean</span></span>

## <span data-ttu-id="df54a-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="df54a-144">NOTES</span></span>

## <span data-ttu-id="df54a-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df54a-145">RELATED LINKS</span></span>
