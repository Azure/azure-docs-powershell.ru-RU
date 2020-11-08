---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078235"
---
# <span data-ttu-id="495d3-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="495d3-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="495d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="495d3-102">SYNOPSIS</span></span>
<span data-ttu-id="495d3-103">Удаляйте неграничные устройства как дочерние элементы с указанного пограничного устройства.</span><span class="sxs-lookup"><span data-stu-id="495d3-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="495d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="495d3-104">SYNTAX</span></span>

### <span data-ttu-id="495d3-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="495d3-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="495d3-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="495d3-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="495d3-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="495d3-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="495d3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="495d3-108">DESCRIPTION</span></span>
<span data-ttu-id="495d3-109">Удалите все или упомянутые неграничные устройства как дочерние, указанные на пограничном устройстве.</span><span class="sxs-lookup"><span data-stu-id="495d3-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="495d3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="495d3-110">EXAMPLES</span></span>

### <span data-ttu-id="495d3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="495d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="495d3-112">Удаляйте упомянутые устройства как дочерние для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="495d3-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="495d3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="495d3-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="495d3-114">Удалите все неграничные устройства как дочерние устройства, заданные с краевым устройством.</span><span class="sxs-lookup"><span data-stu-id="495d3-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="495d3-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="495d3-115">PARAMETERS</span></span>

### <span data-ttu-id="495d3-116">-Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="495d3-116">-Children</span></span>
<span data-ttu-id="495d3-117">Дочерний список устройств (разделенный запятыми) включает только устройства без краев.</span><span class="sxs-lookup"><span data-stu-id="495d3-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495d3-118">-DefaultProfile</span></span>
<span data-ttu-id="495d3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="495d3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495d3-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="495d3-120">-DeviceId</span></span>
<span data-ttu-id="495d3-121">Идентификатор устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="495d3-121">Id of edge device.</span></span>

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

### <span data-ttu-id="495d3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="495d3-122">-InputObject</span></span>
<span data-ttu-id="495d3-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="495d3-123">IotHub object</span></span>

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

### <span data-ttu-id="495d3-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="495d3-124">-IotHubName</span></span>
<span data-ttu-id="495d3-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="495d3-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="495d3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="495d3-126">-PassThru</span></span>
<span data-ttu-id="495d3-127">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="495d3-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="495d3-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="495d3-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="495d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="495d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="495d3-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="495d3-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="495d3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="495d3-131">-ResourceId</span></span>
<span data-ttu-id="495d3-132">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="495d3-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="495d3-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="495d3-133">-Confirm</span></span>
<span data-ttu-id="495d3-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="495d3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="495d3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495d3-135">-WhatIf</span></span>
<span data-ttu-id="495d3-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="495d3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495d3-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="495d3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="495d3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495d3-138">CommonParameters</span></span>
<span data-ttu-id="495d3-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="495d3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495d3-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="495d3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495d3-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="495d3-141">INPUTS</span></span>

### <span data-ttu-id="495d3-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="495d3-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="495d3-143">System. String</span><span class="sxs-lookup"><span data-stu-id="495d3-143">System.String</span></span>

## <span data-ttu-id="495d3-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="495d3-144">OUTPUTS</span></span>

### <span data-ttu-id="495d3-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="495d3-145">System.Boolean</span></span>

## <span data-ttu-id="495d3-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="495d3-146">NOTES</span></span>

## <span data-ttu-id="495d3-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="495d3-147">RELATED LINKS</span></span>