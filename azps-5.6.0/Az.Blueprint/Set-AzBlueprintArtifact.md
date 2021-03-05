---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7e4558d0ff48f2750ed3ac825b2358b5cad437ca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009347"
---
# <span data-ttu-id="a4d5e-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a4d5e-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="a4d5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d5e-103">Обновление артефакта в определении схемы.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="a4d5e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4d5e-104">SYNTAX</span></span>

### <span data-ttu-id="a4d5e-105">UpdateTemplateArtifact (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4d5e-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d5e-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="a4d5e-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d5e-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a4d5e-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4d5e-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a4d5e-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4d5e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4d5e-109">DESCRIPTION</span></span>
<span data-ttu-id="a4d5e-110">Обновление артефакта.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-110">Update an artifact.</span></span> <span data-ttu-id="a4d5e-111">Существует два способа обновления артефакта: с помощью артефакта JSON в качестве входного файла или путем предоставления вводимых параметров артефакта.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="a4d5e-112">Хотя метод JSON не требует предоставления артефакта в виде inline, пользователь должен укажить тип артефакта с помощью параметра -Type.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="a4d5e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4d5e-113">EXAMPLES</span></span>

### <span data-ttu-id="a4d5e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a4d5e-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="a4d5e-115">Обновление артефакта с помощью JSON-файла артефакта.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="a4d5e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a4d5e-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="a4d5e-117">Обновление артефакта с помощью inline parameters.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="a4d5e-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a4d5e-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="a4d5e-119">Обновление артефакта с помощью ARM шаблона.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="a4d5e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4d5e-120">PARAMETERS</span></span>

### <span data-ttu-id="a4d5e-121">-Артефакт</span><span class="sxs-lookup"><span data-stu-id="a4d5e-121">-ArtifactFile</span></span>
<span data-ttu-id="a4d5e-122">Расположение файла артефакта в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="a4d5e-123">-Blueprint</span></span>
<span data-ttu-id="a4d5e-124">Объект Blueprint.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d5e-125">-DefaultProfile</span></span>
<span data-ttu-id="a4d5e-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4d5e-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="a4d5e-127">-DependsOn</span></span>
<span data-ttu-id="a4d5e-128">Список имен артефактов, которые необходимо создать перед текущим артефактом.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-129">-Description</span><span class="sxs-lookup"><span data-stu-id="a4d5e-129">-Description</span></span>
<span data-ttu-id="a4d5e-130">Описание артефакта.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a4d5e-131">-Name</span></span>
<span data-ttu-id="a4d5e-132">Имя артефакта</span><span class="sxs-lookup"><span data-stu-id="a4d5e-132">Name of the artifact</span></span>

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

### <span data-ttu-id="a4d5e-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a4d5e-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="a4d5e-134">Определение определения определения политики.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="a4d5e-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="a4d5e-136">Возможность передавать параметры в артефакт определения политики.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4d5e-137">-ResourceGroupName</span></span>
<span data-ttu-id="a4d5e-138">Имя группы ресурсов, под которым будет входить артефакт.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a4d5e-139">-RoleDefinitionId</span></span>
<span data-ttu-id="a4d5e-140">Список определений ролей</span><span class="sxs-lookup"><span data-stu-id="a4d5e-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a4d5e-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="a4d5e-142">Список ид определения ролей.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="a4d5e-143">-TemplateFile</span></span>
<span data-ttu-id="a4d5e-144">Расположение файла шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="a4d5e-145">-TemplateParameterFile</span></span>
<span data-ttu-id="a4d5e-146">Расположение файла параметров ARM шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-147">-Type</span><span class="sxs-lookup"><span data-stu-id="a4d5e-147">-Type</span></span>
<span data-ttu-id="a4d5e-148">Тип артефакта.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-148">Type of the artifact.</span></span>
<span data-ttu-id="a4d5e-149">Поддерживаются три типа: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d5e-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4d5e-150">-Confirm</span></span>
<span data-ttu-id="a4d5e-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4d5e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4d5e-152">-WhatIf</span></span>
<span data-ttu-id="a4d5e-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4d5e-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4d5e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d5e-155">CommonParameters</span></span>
<span data-ttu-id="a4d5e-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4d5e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d5e-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4d5e-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d5e-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4d5e-158">INPUTS</span></span>

### <span data-ttu-id="a4d5e-159">System.String</span><span class="sxs-lookup"><span data-stu-id="a4d5e-159">System.String</span></span>

### <span data-ttu-id="a4d5e-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="a4d5e-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="a4d5e-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="a4d5e-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a4d5e-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a4d5e-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a4d5e-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a4d5e-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a4d5e-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a4d5e-164">System.String[]</span></span>

## <span data-ttu-id="a4d5e-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4d5e-165">OUTPUTS</span></span>

### <span data-ttu-id="a4d5e-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="a4d5e-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="a4d5e-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4d5e-167">NOTES</span></span>

## <span data-ttu-id="a4d5e-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4d5e-168">RELATED LINKS</span></span>
