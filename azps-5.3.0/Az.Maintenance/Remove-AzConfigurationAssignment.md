---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: 137540ae71e097e98d390e2ab2efb2f6643928e1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506601"
---
# <span data-ttu-id="1f4d4-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="1f4d4-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="1f4d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f4d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4d4-103">Оторегистрация конфигурации ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="1f4d4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f4d4-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f4d4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f4d4-105">DESCRIPTION</span></span>
<span data-ttu-id="1f4d4-106">Оторегистрация конфигурации ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="1f4d4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f4d4-107">EXAMPLES</span></span>

### <span data-ttu-id="1f4d4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1f4d4-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="1f4d4-109">Оторегистрация конфигурации ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="1f4d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f4d4-110">PARAMETERS</span></span>

### <span data-ttu-id="1f4d4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f4d4-111">-AsJob</span></span>
<span data-ttu-id="1f4d4-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1f4d4-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f4d4-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="1f4d4-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="1f4d4-114">Имя назначения конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-114">The configuration assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4d4-115">-DefaultProfile</span></span>
<span data-ttu-id="1f4d4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4d4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1f4d4-117">-Force</span></span>
<span data-ttu-id="1f4d4-118">Принудительное удаление без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="1f4d4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f4d4-119">-PassThru</span></span>
<span data-ttu-id="1f4d4-120">Возвращает состояние операции удаления.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="1f4d4-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1f4d4-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="1f4d4-122">-ProviderName</span></span>
<span data-ttu-id="1f4d4-123">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f4d4-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f4d4-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1f4d4-126">-ResourceName</span></span>
<span data-ttu-id="1f4d4-127">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="1f4d4-128">-ResourceParentName</span></span>
<span data-ttu-id="1f4d4-129">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="1f4d4-130">-ResourceParentType</span></span>
<span data-ttu-id="1f4d4-131">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-131">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1f4d4-132">-ResourceType</span></span>
<span data-ttu-id="1f4d4-133">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-133">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f4d4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f4d4-134">-Confirm</span></span>
<span data-ttu-id="1f4d4-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f4d4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f4d4-136">-WhatIf</span></span>
<span data-ttu-id="1f4d4-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f4d4-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f4d4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4d4-139">CommonParameters</span></span>
<span data-ttu-id="1f4d4-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4d4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4d4-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f4d4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4d4-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f4d4-142">INPUTS</span></span>

### <span data-ttu-id="1f4d4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="1f4d4-143">System.String</span></span>

## <span data-ttu-id="1f4d4-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f4d4-144">OUTPUTS</span></span>

### <span data-ttu-id="1f4d4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f4d4-145">System.Boolean</span></span>

## <span data-ttu-id="1f4d4-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f4d4-146">NOTES</span></span>

## <span data-ttu-id="1f4d4-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f4d4-147">RELATED LINKS</span></span>
