---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeRole.md
ms.openlocfilehash: 22dee84aadc590d140d64cbd71eeaed3c16f03e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910427"
---
# <span data-ttu-id="3866d-101">Set-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3866d-101">Set-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="3866d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3866d-102">SYNOPSIS</span></span>
<span data-ttu-id="3866d-103">Обновляет роль устройства</span><span class="sxs-lookup"><span data-stu-id="3866d-103">Updates a Role for a device</span></span>

## <span data-ttu-id="3866d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3866d-104">SYNTAX</span></span>

### <span data-ttu-id="3866d-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3866d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3866d-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3866d-106">SetByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ResourceId <String> -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3866d-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3866d-107">SetByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeRole -ShareName <String[]> [-DefaultProfile <IAzureContextContainer>]
 -InputObject <PSDataBoxEdgeRole> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3866d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3866d-108">DESCRIPTION</span></span>
<span data-ttu-id="3866d-109">Командлет **Set-AzDataBoxEdgeRole** обновляет роль IOT для поля данных Device Edge.</span><span class="sxs-lookup"><span data-stu-id="3866d-109">The **Set-AzDataBoxEdgeRole** cmdlet updates an IoT role for a Data Box Edge device.</span></span> <span data-ttu-id="3866d-110">Старые смонтированные общие ресурсы будут заменены новыми, предоставленными в параметре ShareName.</span><span class="sxs-lookup"><span data-stu-id="3866d-110">The old mounted shares will be replaced with the newly provided ones in the ShareName parameter.</span></span>

## <span data-ttu-id="3866d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3866d-111">EXAMPLES</span></span>

### <span data-ttu-id="3866d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3866d-112">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName sharename1,sharename2,sharename3

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="3866d-113">Общий доступ к именам заменяет старые подключенные общие ресурсы с помощью вновь предоставленных файлов</span><span class="sxs-lookup"><span data-stu-id="3866d-113">Share Names will replace the old mounted shares with the newly provided ones</span></span>

### <span data-ttu-id="3866d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3866d-114">Example 2</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name roleiot -ShareName @()

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
roleiot ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

<span data-ttu-id="3866d-115">Отключение всех общих ресурсов</span><span class="sxs-lookup"><span data-stu-id="3866d-115">To unmount all shares</span></span>

## <span data-ttu-id="3866d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3866d-116">PARAMETERS</span></span>

### <span data-ttu-id="3866d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3866d-117">-DefaultProfile</span></span>
<span data-ttu-id="3866d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3866d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3866d-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="3866d-119">-DeviceName</span></span>
<span data-ttu-id="3866d-120">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="3866d-120">Device Name</span></span>

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

### <span data-ttu-id="3866d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3866d-121">-InputObject</span></span>
<span data-ttu-id="3866d-122">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="3866d-122">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3866d-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3866d-123">-Name</span></span>
<span data-ttu-id="3866d-124">Имя роли</span><span class="sxs-lookup"><span data-stu-id="3866d-124">Name of the Role</span></span>

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

### <span data-ttu-id="3866d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3866d-125">-ResourceGroupName</span></span>
<span data-ttu-id="3866d-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3866d-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3866d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3866d-127">-ResourceId</span></span>
<span data-ttu-id="3866d-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3866d-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="3866d-129">-Имя_общего_ресурса</span><span class="sxs-lookup"><span data-stu-id="3866d-129">-ShareName</span></span>
<span data-ttu-id="3866d-130">Общий доступ (-ы) к роли</span><span class="sxs-lookup"><span data-stu-id="3866d-130">Share(s) in a role</span></span>

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

### <span data-ttu-id="3866d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3866d-131">-Confirm</span></span>
<span data-ttu-id="3866d-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3866d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3866d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3866d-133">-WhatIf</span></span>
<span data-ttu-id="3866d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3866d-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3866d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3866d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3866d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3866d-136">CommonParameters</span></span>
<span data-ttu-id="3866d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3866d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3866d-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3866d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3866d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3866d-139">INPUTS</span></span>

### <span data-ttu-id="3866d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3866d-140">System.String</span></span>

### <span data-ttu-id="3866d-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3866d-141">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3866d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3866d-142">OUTPUTS</span></span>

### <span data-ttu-id="3866d-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="3866d-143">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="3866d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="3866d-144">NOTES</span></span>

## <span data-ttu-id="3866d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3866d-145">RELATED LINKS</span></span>
