---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414215"
---
# <span data-ttu-id="d119c-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d119c-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="d119c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d119c-102">SYNOPSIS</span></span>
<span data-ttu-id="d119c-103">Обновление роли для устройства</span><span class="sxs-lookup"><span data-stu-id="d119c-103">Updates a Role for a device</span></span>

## <span data-ttu-id="d119c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d119c-104">SYNTAX</span></span>

### <span data-ttu-id="d119c-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d119c-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d119c-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d119c-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d119c-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d119c-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d119c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d119c-108">DESCRIPTION</span></span>
<span data-ttu-id="d119c-109">При **этом для устройства Edge Data Box** роль IoT обновляется.</span><span class="sxs-lookup"><span data-stu-id="d119c-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="d119c-110">Старые установленные акции будут заменены новыми предоставленными в параметре ShareName.</span><span class="sxs-lookup"><span data-stu-id="d119c-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="d119c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d119c-111">EXAMPLES</span></span>

### <span data-ttu-id="d119c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d119c-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="d119c-113">Share Names will replace the old mounted shares with the newly provided ones</span><span class="sxs-lookup"><span data-stu-id="d119c-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="d119c-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d119c-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="d119c-115">Чтобы отовязать все акции</span><span class="sxs-lookup"><span data-stu-id="d119c-115">To unmount all shares</span></span>

## <span data-ttu-id="d119c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d119c-116">PARAMETERS</span></span>

### <span data-ttu-id="d119c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d119c-117">-DefaultProfile</span></span>
<span data-ttu-id="d119c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d119c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d119c-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d119c-119">-DeviceName</span></span>
<span data-ttu-id="d119c-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="d119c-120">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d119c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d119c-121">-InputObject</span></span>
<span data-ttu-id="d119c-122">Предосообщите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="d119c-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d119c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d119c-123">-Name</span></span>
<span data-ttu-id="d119c-124">Имя роли</span><span class="sxs-lookup"><span data-stu-id="d119c-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d119c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d119c-125">-ResourceGroupName</span></span>
<span data-ttu-id="d119c-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d119c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d119c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d119c-127">-ResourceId</span></span>
<span data-ttu-id="d119c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d119c-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d119c-129">-ShareName</span><span class="sxs-lookup"><span data-stu-id="d119c-129">-ShareName</span></span>
<span data-ttu-id="d119c-130">Совместное участие в роли</span><span class="sxs-lookup"><span data-stu-id="d119c-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d119c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d119c-131">-Confirm</span></span>
<span data-ttu-id="d119c-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d119c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d119c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d119c-133">-WhatIf</span></span>
<span data-ttu-id="d119c-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d119c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d119c-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d119c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d119c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d119c-136">CommonParameters</span></span>
<span data-ttu-id="d119c-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d119c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d119c-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d119c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d119c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d119c-139">INPUTS</span></span>

### <span data-ttu-id="d119c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="d119c-140">System.String</span></span>

### <span data-ttu-id="d119c-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d119c-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="d119c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d119c-142">OUTPUTS</span></span>

### <span data-ttu-id="d119c-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDAtaBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d119c-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="d119c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d119c-144">NOTES</span></span>

## <span data-ttu-id="d119c-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d119c-145">RELATED LINKS</span></span>
