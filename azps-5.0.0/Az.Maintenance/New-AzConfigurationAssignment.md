---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzConfigurationAssignment.md
ms.openlocfilehash: 9754c3efc87d0e607c613789e6e27320f430aa06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247352"
---
# <span data-ttu-id="84509-101">New-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="84509-101">New-AzConfigurationAssignment</span></span>

## <span data-ttu-id="84509-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84509-102">SYNOPSIS</span></span>
<span data-ttu-id="84509-103">Регистрация конфигурации для ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-103">Register configuration for resource.</span></span>

## <span data-ttu-id="84509-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84509-104">SYNTAX</span></span>

```
New-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-ResourceId <String>] -Location <String>
 -MaintenanceConfigurationId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84509-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84509-105">DESCRIPTION</span></span>
<span data-ttu-id="84509-106">Регистрация конфигурации обслуживания для ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-106">Register maintenance configuration for resource.</span></span>

## <span data-ttu-id="84509-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84509-107">EXAMPLES</span></span>

### <span data-ttu-id="84509-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="84509-108">Example 1</span></span>
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

<span data-ttu-id="84509-109">Зарегистрируйте конфигурацию обслуживания для выделенного узла.</span><span class="sxs-lookup"><span data-stu-id="84509-109">Register maintenance configuration for dedicated host.</span></span>

## <span data-ttu-id="84509-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84509-110">PARAMETERS</span></span>

### <span data-ttu-id="84509-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84509-111">-AsJob</span></span>
<span data-ttu-id="84509-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="84509-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84509-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="84509-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="84509-114">Имя назначения конфигурации должно совпадать с MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="84509-114">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="84509-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84509-115">-DefaultProfile</span></span>
<span data-ttu-id="84509-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84509-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84509-117">-Location</span><span class="sxs-lookup"><span data-stu-id="84509-117">-Location</span></span>
<span data-ttu-id="84509-118">Расположение, в котором нет пробелов для ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-118">The location without spaces for the resource.</span></span>

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

### <span data-ttu-id="84509-119">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="84509-119">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="84509-120">Полное MaintenanceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="84509-120">The fully qualified MaintenanceConfiguration.</span></span>

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

### <span data-ttu-id="84509-121">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="84509-121">-ProviderName</span></span>
<span data-ttu-id="84509-122">Имя поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84509-122">The resource provider Name.</span></span>

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

### <span data-ttu-id="84509-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84509-123">-ResourceGroupName</span></span>
<span data-ttu-id="84509-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84509-124">The resource Group Name.</span></span>

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

### <span data-ttu-id="84509-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84509-125">-ResourceId</span></span>
<span data-ttu-id="84509-126">Имя назначения конфигурации должно совпадать с MaintenanceConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="84509-126">The configuration assignment name, should match the MaintenanceConfigurationName.</span></span>

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

### <span data-ttu-id="84509-127">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="84509-127">-ResourceName</span></span>
<span data-ttu-id="84509-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-128">The resource name.</span></span>

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

### <span data-ttu-id="84509-129">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="84509-129">-ResourceParentName</span></span>
<span data-ttu-id="84509-130">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-130">The parent resource name.</span></span>

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

### <span data-ttu-id="84509-131">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="84509-131">-ResourceParentType</span></span>
<span data-ttu-id="84509-132">Родительский тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-132">The parent resource type.</span></span>

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

### <span data-ttu-id="84509-133">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="84509-133">-ResourceType</span></span>
<span data-ttu-id="84509-134">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="84509-134">The resource type.</span></span>

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

### <span data-ttu-id="84509-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84509-135">-Confirm</span></span>
<span data-ttu-id="84509-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84509-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84509-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84509-137">-WhatIf</span></span>
<span data-ttu-id="84509-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84509-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84509-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84509-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84509-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84509-140">CommonParameters</span></span>
<span data-ttu-id="84509-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84509-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84509-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84509-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84509-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84509-143">INPUTS</span></span>

### <span data-ttu-id="84509-144">System. String</span><span class="sxs-lookup"><span data-stu-id="84509-144">System.String</span></span>

## <span data-ttu-id="84509-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84509-145">OUTPUTS</span></span>

### <span data-ttu-id="84509-146">Microsoft. Azure. Commands. Maintenance. Models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="84509-146">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="84509-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="84509-147">NOTES</span></span>

## <span data-ttu-id="84509-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84509-148">RELATED LINKS</span></span>
