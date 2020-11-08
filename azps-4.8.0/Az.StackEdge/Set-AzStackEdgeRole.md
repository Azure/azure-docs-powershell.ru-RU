---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeRole.md
ms.openlocfilehash: 17e152d9fb94dc8c2d8d27157f278952a0844ecd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243204"
---
# <span data-ttu-id="b8a08-101">Set-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b8a08-101">Set-AzStackEdgeRole</span></span>

## <span data-ttu-id="b8a08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b8a08-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a08-103">Обновляет роль устройства</span><span class="sxs-lookup"><span data-stu-id="b8a08-103">Updates a Role for a device</span></span>

## <span data-ttu-id="b8a08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b8a08-104">SYNTAX</span></span>

### <span data-ttu-id="b8a08-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b8a08-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -ShareName <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a08-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a08-106">SetByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8a08-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8a08-107">SetByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSStackEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a08-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a08-108">DESCRIPTION</span></span>
<span data-ttu-id="b8a08-109">Командлет **Set-AzStackEdgeRole** обновляет роль IOT для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="b8a08-109">The **Set-AzStackEdgeRole** cmdlet updates an IoT role for a Stack Edge device.</span></span> <span data-ttu-id="b8a08-110">Старые смонтированные общие ресурсы будут заменены новыми, предоставленными в параметре ShareName.</span><span class="sxs-lookup"><span data-stu-id="b8a08-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="b8a08-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b8a08-111">EXAMPLES</span></span>

### <span data-ttu-id="b8a08-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b8a08-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="b8a08-113">Общий доступ к именам заменяет старые подключенные общие ресурсы с помощью вновь предоставленных файлов</span><span class="sxs-lookup"><span data-stu-id="b8a08-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="b8a08-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b8a08-114">Example 2</span></span>
```powershell
PS C:\> Set-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="b8a08-115">Отключение всех общих ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8a08-115">To unmount all shares</span></span>

## <span data-ttu-id="b8a08-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b8a08-116">PARAMETERS</span></span>

### <span data-ttu-id="b8a08-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a08-117">-DefaultProfile</span></span>
<span data-ttu-id="b8a08-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8a08-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a08-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="b8a08-119">-DeviceName</span></span>
<span data-ttu-id="b8a08-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="b8a08-120">Device Name</span></span>

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

### <span data-ttu-id="b8a08-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8a08-121">-InputObject</span></span>
<span data-ttu-id="b8a08-122">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="b8a08-122">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole
Parameter Sets: SetByInputObjectParameterSet
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b8a08-123">-Name</span></span>
<span data-ttu-id="b8a08-124">Имя роли</span><span class="sxs-lookup"><span data-stu-id="b8a08-124">Name of the Role</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a08-125">-ResourceGroupName</span></span>
<span data-ttu-id="b8a08-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b8a08-126">Resource Group Name</span></span>

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

### <span data-ttu-id="b8a08-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8a08-127">-ResourceId</span></span>
<span data-ttu-id="b8a08-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8a08-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="b8a08-129">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="b8a08-129">-ShareName</span></span>
<span data-ttu-id="b8a08-130">Общий доступ (-ы) к роли</span><span class="sxs-lookup"><span data-stu-id="b8a08-130">Share(s) in a role</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8a08-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8a08-131">-Confirm</span></span>
<span data-ttu-id="b8a08-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b8a08-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a08-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a08-133">-WhatIf</span></span>
<span data-ttu-id="b8a08-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b8a08-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8a08-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b8a08-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a08-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a08-136">CommonParameters</span></span>
<span data-ttu-id="b8a08-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b8a08-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a08-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8a08-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a08-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b8a08-139">INPUTS</span></span>

### <span data-ttu-id="b8a08-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b8a08-140">System.String</span></span>

### <span data-ttu-id="b8a08-141">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b8a08-141">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b8a08-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8a08-142">OUTPUTS</span></span>

### <span data-ttu-id="b8a08-143">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b8a08-143">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="b8a08-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="b8a08-144">NOTES</span></span>

## <span data-ttu-id="b8a08-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8a08-145">RELATED LINKS</span></span>
