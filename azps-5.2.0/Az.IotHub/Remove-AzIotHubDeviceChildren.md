---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406484"
---
# <span data-ttu-id="19404-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="19404-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="19404-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19404-102">SYNOPSIS</span></span>
<span data-ttu-id="19404-103">Удаление не edge-устройств как детей с указанного edge-устройства.</span><span class="sxs-lookup"><span data-stu-id="19404-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="19404-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19404-104">SYNTAX</span></span>

### <span data-ttu-id="19404-105">Набор ресурсов (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19404-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19404-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="19404-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19404-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="19404-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19404-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19404-108">DESCRIPTION</span></span>
<span data-ttu-id="19404-109">Удалите все или упомянутые вне границы устройства как устройства, указанные детьми.</span><span class="sxs-lookup"><span data-stu-id="19404-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="19404-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19404-110">EXAMPLES</span></span>

### <span data-ttu-id="19404-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19404-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="19404-112">Удалите упомянутые устройства как дети указанного устройства.</span><span class="sxs-lookup"><span data-stu-id="19404-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="19404-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="19404-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="19404-114">Удалите все не edge-устройства как устройства, указанные детьми.</span><span class="sxs-lookup"><span data-stu-id="19404-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="19404-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19404-115">PARAMETERS</span></span>

### <span data-ttu-id="19404-116">-Дети</span><span class="sxs-lookup"><span data-stu-id="19404-116">-Children</span></span>
<span data-ttu-id="19404-117">Список устройств ребенка (разделенный запятой) включает только устройства, не включающее в себя границы.</span><span class="sxs-lookup"><span data-stu-id="19404-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="19404-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19404-118">-DefaultProfile</span></span>
<span data-ttu-id="19404-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19404-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19404-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="19404-120">-DeviceId</span></span>
<span data-ttu-id="19404-121">Id of edge device.</span><span class="sxs-lookup"><span data-stu-id="19404-121">Id of edge device.</span></span>

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

### <span data-ttu-id="19404-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19404-122">-InputObject</span></span>
<span data-ttu-id="19404-123">Объект IotHub</span><span class="sxs-lookup"><span data-stu-id="19404-123">IotHub object</span></span>

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

### <span data-ttu-id="19404-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="19404-124">-IotHubName</span></span>
<span data-ttu-id="19404-125">Имя концентратора Iot</span><span class="sxs-lookup"><span data-stu-id="19404-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="19404-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19404-126">-PassThru</span></span>
<span data-ttu-id="19404-127">Возвращает объект boolean.</span><span class="sxs-lookup"><span data-stu-id="19404-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="19404-128">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="19404-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19404-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19404-129">-ResourceGroupName</span></span>
<span data-ttu-id="19404-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="19404-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="19404-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19404-131">-ResourceId</span></span>
<span data-ttu-id="19404-132">ИД ресурса IotHub</span><span class="sxs-lookup"><span data-stu-id="19404-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="19404-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19404-133">-Confirm</span></span>
<span data-ttu-id="19404-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19404-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19404-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19404-135">-WhatIf</span></span>
<span data-ttu-id="19404-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19404-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19404-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19404-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19404-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19404-138">CommonParameters</span></span>
<span data-ttu-id="19404-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19404-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19404-140">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19404-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19404-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19404-141">INPUTS</span></span>

### <span data-ttu-id="19404-142">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="19404-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="19404-143">System.String</span><span class="sxs-lookup"><span data-stu-id="19404-143">System.String</span></span>

## <span data-ttu-id="19404-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19404-144">OUTPUTS</span></span>

### <span data-ttu-id="19404-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19404-145">System.Boolean</span></span>

## <span data-ttu-id="19404-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19404-146">NOTES</span></span>

## <span data-ttu-id="19404-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19404-147">RELATED LINKS</span></span>
