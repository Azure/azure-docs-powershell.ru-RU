---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505325"
---
# <span data-ttu-id="8dc85-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="8dc85-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="8dc85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc85-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc85-103">Экспорт спецификации шаблона в локализованную файловую систему</span><span class="sxs-lookup"><span data-stu-id="8dc85-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="8dc85-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8dc85-104">SYNTAX</span></span>

### <span data-ttu-id="8dc85-105">ExportByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dc85-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc85-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dc85-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc85-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc85-107">DESCRIPTION</span></span>
<span data-ttu-id="8dc85-108">Экспорт определенной версии Шаблона Спецификации в локализованную систему файлов.</span><span class="sxs-lookup"><span data-stu-id="8dc85-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="8dc85-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc85-109">EXAMPLES</span></span>

### <span data-ttu-id="8dc85-110">Пример 1. Экспорт по имени</span><span class="sxs-lookup"><span data-stu-id="8dc85-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="8dc85-111">Экспортирует версию "v1.0" спецификации шаблона MyTemplateSpec в группе ресурсов myRG в локализованную папку вывода "v1".</span><span class="sxs-lookup"><span data-stu-id="8dc85-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="8dc85-112">Пример 2. Экспорт по ид ресурса</span><span class="sxs-lookup"><span data-stu-id="8dc85-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="8dc85-113">Экспортирует версию "v1.0" спецификации шаблона "MyTemplateSpec" в группе ресурсов myRG из subId подписки в локализованную папку вывода \{ \} "v1".</span><span class="sxs-lookup"><span data-stu-id="8dc85-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="8dc85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc85-114">PARAMETERS</span></span>

### <span data-ttu-id="8dc85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc85-115">-DefaultProfile</span></span>
<span data-ttu-id="8dc85-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc85-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc85-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc85-117">-Name</span></span>
<span data-ttu-id="8dc85-118">Имя спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="8dc85-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc85-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="8dc85-119">-OutputFolder</span></span>
<span data-ttu-id="8dc85-120">Путь к папке, в которой будет выводться версия спецификации шаблона.</span><span class="sxs-lookup"><span data-stu-id="8dc85-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="8dc85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc85-121">-ResourceGroupName</span></span>
<span data-ttu-id="8dc85-122">Имя группы ресурсов шаблона спецификации.</span><span class="sxs-lookup"><span data-stu-id="8dc85-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc85-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc85-123">-ResourceId</span></span>
<span data-ttu-id="8dc85-124">Полное имя ресурса спецификации шаблона. Пример: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="8dc85-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dc85-125">-Версия</span><span class="sxs-lookup"><span data-stu-id="8dc85-125">-Version</span></span>
<span data-ttu-id="8dc85-126">Версия спецификации шаблона для экспорта.</span><span class="sxs-lookup"><span data-stu-id="8dc85-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="8dc85-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc85-127">-Confirm</span></span>
<span data-ttu-id="8dc85-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc85-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc85-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc85-129">-WhatIf</span></span>
<span data-ttu-id="8dc85-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc85-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8dc85-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8dc85-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc85-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc85-132">CommonParameters</span></span>
<span data-ttu-id="8dc85-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc85-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc85-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dc85-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc85-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc85-135">INPUTS</span></span>

### <span data-ttu-id="8dc85-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8dc85-136">System.String</span></span>

## <span data-ttu-id="8dc85-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc85-137">OUTPUTS</span></span>

### <span data-ttu-id="8dc85-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="8dc85-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="8dc85-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8dc85-139">NOTES</span></span>

## <span data-ttu-id="8dc85-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc85-140">RELATED LINKS</span></span>
