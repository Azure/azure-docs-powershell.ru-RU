---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 71e1cd6ea8f7aaa228ccdc5032971decfb21b2f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94314165"
---
# <span data-ttu-id="cf5ad-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cf5ad-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="cf5ad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cf5ad-102">SYNOPSIS</span></span>
<span data-ttu-id="cf5ad-103">Обновляет роль устройства</span><span class="sxs-lookup"><span data-stu-id="cf5ad-103">Updates a Role for a device</span></span>

## <span data-ttu-id="cf5ad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cf5ad-104">SYNTAX</span></span>

### <span data-ttu-id="cf5ad-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cf5ad-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf5ad-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf5ad-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf5ad-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf5ad-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf5ad-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf5ad-108">DESCRIPTION</span></span>
<span data-ttu-id="cf5ad-109">Командлет **Set-AzDataBoxEdgeRole** обновляет роль IOT для поля данных Device Edge.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="cf5ad-110">Старые смонтированные общие ресурсы будут заменены новыми, предоставленными в параметре ShareName.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="cf5ad-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cf5ad-111">EXAMPLES</span></span>

### <span data-ttu-id="cf5ad-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cf5ad-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="cf5ad-113">Общий доступ к именам заменяет старые подключенные общие ресурсы с помощью вновь предоставленных файлов</span><span class="sxs-lookup"><span data-stu-id="cf5ad-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="cf5ad-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cf5ad-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name IotRole -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
IotRole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="cf5ad-115">Отключение всех общих ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf5ad-115">To unmount all shares</span></span>

## <span data-ttu-id="cf5ad-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cf5ad-116">PARAMETERS</span></span>

### <span data-ttu-id="cf5ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf5ad-117">-DefaultProfile</span></span>
<span data-ttu-id="cf5ad-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf5ad-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="cf5ad-119">-DeviceName</span></span>
<span data-ttu-id="cf5ad-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="cf5ad-120">Device Name</span></span>

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

### <span data-ttu-id="cf5ad-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf5ad-121">-InputObject</span></span>
<span data-ttu-id="cf5ad-122">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="cf5ad-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="cf5ad-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cf5ad-123">-Name</span></span>
<span data-ttu-id="cf5ad-124">Имя роли</span><span class="sxs-lookup"><span data-stu-id="cf5ad-124">Name of the Role</span></span>

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

### <span data-ttu-id="cf5ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf5ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="cf5ad-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cf5ad-126">Resource Group Name</span></span>

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

### <span data-ttu-id="cf5ad-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf5ad-127">-ResourceId</span></span>
<span data-ttu-id="cf5ad-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf5ad-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="cf5ad-129">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="cf5ad-129">-ShareName</span></span>
<span data-ttu-id="cf5ad-130">Общий доступ (-ы) к роли</span><span class="sxs-lookup"><span data-stu-id="cf5ad-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="cf5ad-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf5ad-131">-Confirm</span></span>
<span data-ttu-id="cf5ad-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf5ad-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf5ad-133">-WhatIf</span></span>
<span data-ttu-id="cf5ad-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf5ad-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf5ad-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf5ad-136">CommonParameters</span></span>
<span data-ttu-id="cf5ad-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cf5ad-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf5ad-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cf5ad-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf5ad-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cf5ad-139">INPUTS</span></span>

### <span data-ttu-id="cf5ad-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cf5ad-140">System.String</span></span>

### <span data-ttu-id="cf5ad-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cf5ad-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="cf5ad-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cf5ad-142">OUTPUTS</span></span>

### <span data-ttu-id="cf5ad-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cf5ad-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="cf5ad-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="cf5ad-144">NOTES</span></span>

## <span data-ttu-id="cf5ad-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cf5ad-145">RELATED LINKS</span></span>