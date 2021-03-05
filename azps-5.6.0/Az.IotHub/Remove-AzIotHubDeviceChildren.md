---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 296793309dbcae7317353e41f9f3562a020c9be2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013011"
---
# <span data-ttu-id="26fd2-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="26fd2-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="26fd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="26fd2-103">Удалите устройства, не ом границевые, как дети с указанного edgeного устройства.</span><span class="sxs-lookup"><span data-stu-id="26fd2-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="26fd2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26fd2-104">SYNTAX</span></span>

### <span data-ttu-id="26fd2-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26fd2-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26fd2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="26fd2-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26fd2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="26fd2-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26fd2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26fd2-108">DESCRIPTION</span></span>
<span data-ttu-id="26fd2-109">Удалите все или упомянутые вне границы устройства как устройства, указанные детьми.</span><span class="sxs-lookup"><span data-stu-id="26fd2-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="26fd2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26fd2-110">EXAMPLES</span></span>

### <span data-ttu-id="26fd2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26fd2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="26fd2-112">Удалите указанные устройства как дети указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="26fd2-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="26fd2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="26fd2-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="26fd2-114">Удалите все не edge-устройства как устройства, указанные детьми.</span><span class="sxs-lookup"><span data-stu-id="26fd2-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="26fd2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26fd2-115">PARAMETERS</span></span>

### <span data-ttu-id="26fd2-116">-Дети</span><span class="sxs-lookup"><span data-stu-id="26fd2-116">-Children</span></span>
<span data-ttu-id="26fd2-117">Список устройств ребенка (разделенный запятой) включает только устройства, не включающее в себя границы.</span><span class="sxs-lookup"><span data-stu-id="26fd2-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="26fd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26fd2-118">-DefaultProfile</span></span>
<span data-ttu-id="26fd2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26fd2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26fd2-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="26fd2-120">-DeviceId</span></span>
<span data-ttu-id="26fd2-121">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="26fd2-121">Id of edge device.</span></span>

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

### <span data-ttu-id="26fd2-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26fd2-122">-InputObject</span></span>
<span data-ttu-id="26fd2-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="26fd2-123">IotHub object</span></span>

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

### <span data-ttu-id="26fd2-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="26fd2-124">-IotHubName</span></span>
<span data-ttu-id="26fd2-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="26fd2-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="26fd2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26fd2-126">-PassThru</span></span>
<span data-ttu-id="26fd2-127">Разрешает возвращать boolean object.</span><span class="sxs-lookup"><span data-stu-id="26fd2-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="26fd2-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="26fd2-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26fd2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26fd2-129">-ResourceGroupName</span></span>
<span data-ttu-id="26fd2-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="26fd2-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="26fd2-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26fd2-131">-ResourceId</span></span>
<span data-ttu-id="26fd2-132">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="26fd2-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="26fd2-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26fd2-133">-Confirm</span></span>
<span data-ttu-id="26fd2-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="26fd2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26fd2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26fd2-135">-WhatIf</span></span>
<span data-ttu-id="26fd2-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26fd2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26fd2-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26fd2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26fd2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26fd2-138">CommonParameters</span></span>
<span data-ttu-id="26fd2-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26fd2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26fd2-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26fd2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26fd2-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26fd2-141">INPUTS</span></span>

### <span data-ttu-id="26fd2-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="26fd2-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="26fd2-143">System.String</span><span class="sxs-lookup"><span data-stu-id="26fd2-143">System.String</span></span>

## <span data-ttu-id="26fd2-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26fd2-144">OUTPUTS</span></span>

### <span data-ttu-id="26fd2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="26fd2-145">System.Boolean</span></span>

## <span data-ttu-id="26fd2-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26fd2-146">NOTES</span></span>

## <span data-ttu-id="26fd2-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26fd2-147">RELATED LINKS</span></span>
