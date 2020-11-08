---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073798"
---
# <span data-ttu-id="bf843-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="bf843-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="bf843-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf843-102">SYNOPSIS</span></span>
<span data-ttu-id="bf843-103">Удаляйте неграничные устройства как дочерние элементы с указанного пограничного устройства.</span><span class="sxs-lookup"><span data-stu-id="bf843-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="bf843-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf843-104">SYNTAX</span></span>

### <span data-ttu-id="bf843-105">Источник данных (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf843-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf843-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bf843-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf843-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="bf843-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf843-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf843-108">DESCRIPTION</span></span>
<span data-ttu-id="bf843-109">Удалите все или упомянутые неграничные устройства как дочерние, указанные на пограничном устройстве.</span><span class="sxs-lookup"><span data-stu-id="bf843-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="bf843-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf843-110">EXAMPLES</span></span>

### <span data-ttu-id="bf843-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bf843-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="bf843-112">Удаляйте упомянутые устройства как дочерние для указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="bf843-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="bf843-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bf843-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="bf843-114">Удалите все неграничные устройства как дочерние устройства, заданные с краевым устройством.</span><span class="sxs-lookup"><span data-stu-id="bf843-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="bf843-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf843-115">PARAMETERS</span></span>

### <span data-ttu-id="bf843-116">-Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bf843-116">-Children</span></span>
<span data-ttu-id="bf843-117">Дочерний список устройств (разделенный запятыми) включает только устройства без краев.</span><span class="sxs-lookup"><span data-stu-id="bf843-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="bf843-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf843-118">-DefaultProfile</span></span>
<span data-ttu-id="bf843-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf843-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf843-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="bf843-120">-DeviceId</span></span>
<span data-ttu-id="bf843-121">Идентификатор устройства Edge.</span><span class="sxs-lookup"><span data-stu-id="bf843-121">Id of edge device.</span></span>

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

### <span data-ttu-id="bf843-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bf843-122">-InputObject</span></span>
<span data-ttu-id="bf843-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="bf843-123">IotHub object</span></span>

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

### <span data-ttu-id="bf843-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="bf843-124">-IotHubName</span></span>
<span data-ttu-id="bf843-125">Имя центра Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="bf843-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="bf843-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf843-126">-PassThru</span></span>
<span data-ttu-id="bf843-127">Позволяет возвращать логический объект.</span><span class="sxs-lookup"><span data-stu-id="bf843-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="bf843-128">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="bf843-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bf843-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf843-129">-ResourceGroupName</span></span>
<span data-ttu-id="bf843-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bf843-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="bf843-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf843-131">-ResourceId</span></span>
<span data-ttu-id="bf843-132">Идентификатор ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="bf843-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="bf843-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf843-133">-Confirm</span></span>
<span data-ttu-id="bf843-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf843-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf843-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf843-135">-WhatIf</span></span>
<span data-ttu-id="bf843-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf843-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf843-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf843-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf843-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf843-138">CommonParameters</span></span>
<span data-ttu-id="bf843-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf843-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf843-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf843-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf843-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf843-141">INPUTS</span></span>

### <span data-ttu-id="bf843-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="bf843-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="bf843-143">System. String</span><span class="sxs-lookup"><span data-stu-id="bf843-143">System.String</span></span>

## <span data-ttu-id="bf843-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf843-144">OUTPUTS</span></span>

### <span data-ttu-id="bf843-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bf843-145">System.Boolean</span></span>

## <span data-ttu-id="bf843-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf843-146">NOTES</span></span>

## <span data-ttu-id="bf843-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf843-147">RELATED LINKS</span></span>
