---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeDevice.md
ms.openlocfilehash: 431726e1bcbc0045cb1b9958ce9513638259bd8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243184"
---
# <span data-ttu-id="c890f-101">Remove-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c890f-101">Remove-AzStackEdgeDevice</span></span>

## <span data-ttu-id="c890f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c890f-102">SYNOPSIS</span></span>
<span data-ttu-id="c890f-103">Удаляет устройство Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="c890f-103">Removes a Stack Edge device.</span></span>

## <span data-ttu-id="c890f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c890f-104">SYNTAX</span></span>

### <span data-ttu-id="c890f-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c890f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c890f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c890f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c890f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c890f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeDevice -DeviceObject <PSStackEdgeDevice> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c890f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c890f-108">DESCRIPTION</span></span>
<span data-ttu-id="c890f-109">При наложении на устройство Stack Edge конфигурация удаляется с вашего устройства **AzStackEdgeDevice.**</span><span class="sxs-lookup"><span data-stu-id="c890f-109">The **Remove-AzStackEdgeDevice** cmdlet removes the configuration for a Stack Edge device.</span></span>
<span data-ttu-id="c890f-110">Обратите внимание, что устройство можно удалить только после того, как вы разместили заказ и не подготовили его к отправке.</span><span class="sxs-lookup"><span data-stu-id="c890f-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="c890f-111">Перед использованием этого [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) сослаться на документацию об удалении ресурса</span><span class="sxs-lookup"><span data-stu-id="c890f-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="c890f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c890f-112">EXAMPLES</span></span>

### <span data-ttu-id="c890f-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c890f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="c890f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c890f-114">PARAMETERS</span></span>

### <span data-ttu-id="c890f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c890f-115">-AsJob</span></span>
<span data-ttu-id="c890f-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c890f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c890f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c890f-117">-DefaultProfile</span></span>
<span data-ttu-id="c890f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c890f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c890f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="c890f-119">-DeviceObject</span></span>
<span data-ttu-id="c890f-120">Объект Input</span><span class="sxs-lookup"><span data-stu-id="c890f-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c890f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c890f-121">-Name</span></span>
<span data-ttu-id="c890f-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="c890f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c890f-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c890f-123">-PassThru</span></span>
<span data-ttu-id="c890f-124">Возвращает "Истина" в случае успеха.</span><span class="sxs-lookup"><span data-stu-id="c890f-124">returns true if successful</span></span>

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

### <span data-ttu-id="c890f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c890f-125">-ResourceGroupName</span></span>
<span data-ttu-id="c890f-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c890f-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c890f-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c890f-127">-ResourceId</span></span>
<span data-ttu-id="c890f-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="c890f-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c890f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c890f-129">-Confirm</span></span>
<span data-ttu-id="c890f-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c890f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c890f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c890f-131">-WhatIf</span></span>
<span data-ttu-id="c890f-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c890f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c890f-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c890f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c890f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c890f-134">CommonParameters</span></span>
<span data-ttu-id="c890f-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c890f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c890f-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c890f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c890f-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c890f-137">INPUTS</span></span>

### <span data-ttu-id="c890f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c890f-138">System.String</span></span>

### <span data-ttu-id="c890f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="c890f-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="c890f-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c890f-140">OUTPUTS</span></span>

### <span data-ttu-id="c890f-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c890f-141">System.Boolean</span></span>

## <span data-ttu-id="c890f-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c890f-142">NOTES</span></span>

## <span data-ttu-id="c890f-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c890f-143">RELATED LINKS</span></span>
