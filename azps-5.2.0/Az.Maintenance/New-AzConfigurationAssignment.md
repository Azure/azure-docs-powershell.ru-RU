---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398340"
---
# <span data-ttu-id="d437a-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="d437a-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="d437a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d437a-102">SYNOPSIS</span></span>
<span data-ttu-id="d437a-103">Зарегистрируйте конфигурацию для ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-103">Register configuration for resource.</span></span>

## <span data-ttu-id="d437a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d437a-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d437a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d437a-105">DESCRIPTION</span></span>
<span data-ttu-id="d437a-106">Зарегистрируйте конфигурацию обслуживания для ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="d437a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d437a-107">EXAMPLES</span></span>

### <span data-ttu-id="d437a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d437a-108">Example 1</span></span>
```powershell
PS C:\> New-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName -MaintenanceConfigurationId $maintenanceConfigurationCreated.Id -Location $location


Location                   : westus2
MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
ResourceId                 : 7b32ed22-dc7b-4a17-9c42-36c024f4c9f9
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="d437a-109">Зарегистрируйте конфигурацию обслуживания выделенного хоста.</span><span class="sxs-lookup"><span data-stu-id="d437a-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="d437a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d437a-110">PARAMETERS</span></span>

### <span data-ttu-id="d437a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d437a-111">-AsJob</span></span>
<span data-ttu-id="d437a-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d437a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d437a-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d437a-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="d437a-114">Имя назначения конфигурации должно совпадать с именем MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="d437a-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="d437a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d437a-115">-DefaultProfile</span></span>
<span data-ttu-id="d437a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d437a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d437a-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d437a-117">-Location</span></span>
<span data-ttu-id="d437a-118">Расположение без пробелов для ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-118">The location without spaces for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d437a-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d437a-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="d437a-120">Полное обслуживаниеConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d437a-120">The fully qualified MaintenanceConfiguration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d437a-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="d437a-121">-ProviderName</span></span>
<span data-ttu-id="d437a-122">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d437a-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="d437a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d437a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d437a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d437a-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="d437a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d437a-125">-ResourceId</span></span>
<span data-ttu-id="d437a-126">Имя назначения конфигурации должно совпадать с именем MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="d437a-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d437a-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d437a-127">-ResourceName</span></span>
<span data-ttu-id="d437a-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-128">The resource name.</span></span>

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

### <span data-ttu-id="d437a-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="d437a-129">-ResourceParentName</span></span>
<span data-ttu-id="d437a-130">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-130">The parent resource name.</span></span>

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

### <span data-ttu-id="d437a-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="d437a-131">-ResourceParentType</span></span>
<span data-ttu-id="d437a-132">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-132">The parent resource type.</span></span>

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

### <span data-ttu-id="d437a-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d437a-133">-ResourceType</span></span>
<span data-ttu-id="d437a-134">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="d437a-134">The resource type.</span></span>

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

### <span data-ttu-id="d437a-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d437a-135">-Confirm</span></span>
<span data-ttu-id="d437a-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d437a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d437a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d437a-137">-WhatIf</span></span>
<span data-ttu-id="d437a-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d437a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d437a-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d437a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d437a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d437a-140">CommonParameters</span></span>
<span data-ttu-id="d437a-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d437a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d437a-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d437a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d437a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d437a-143">INPUTS</span></span>

### <span data-ttu-id="d437a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d437a-144">System.String</span></span>

## <span data-ttu-id="d437a-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d437a-145">OUTPUTS</span></span>

### <span data-ttu-id="d437a-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="d437a-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="d437a-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d437a-147">NOTES</span></span>

## <span data-ttu-id="d437a-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d437a-148">RELATED LINKS</span></span>
