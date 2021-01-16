---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509441"
---
# <span data-ttu-id="0ad36-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="0ad36-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="0ad36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad36-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad36-103">Обновление артефакта в определении схемы.</span><span class="sxs-lookup"><span data-stu-id="0ad36-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="0ad36-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ad36-104">SYNTAX</span></span>

### <span data-ttu-id="0ad36-105">UpdateTemplateArtifact (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ad36-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad36-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="0ad36-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad36-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="0ad36-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ad36-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="0ad36-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ad36-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ad36-109">DESCRIPTION</span></span>
<span data-ttu-id="0ad36-110">Обновление артефакта.</span><span class="sxs-lookup"><span data-stu-id="0ad36-110">Update an artifact.</span></span> <span data-ttu-id="0ad36-111">Существует два способа обновить артефакт: через артефакт JSON в качестве входного файла или путем предоставления вводимых параметров артефакта.</span><span class="sxs-lookup"><span data-stu-id="0ad36-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="0ad36-112">Хотя метод JSON не требует, чтобы часть артефакта была задана в виде inline parameter, пользователь должен увести тип артефакта с помощью параметра -Type.</span><span class="sxs-lookup"><span data-stu-id="0ad36-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="0ad36-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ad36-113">EXAMPLES</span></span>

### <span data-ttu-id="0ad36-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ad36-114">Example 1</span></span>
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

<span data-ttu-id="0ad36-115">Обновление артефакта с помощью JSON-файла артефакта.</span><span class="sxs-lookup"><span data-stu-id="0ad36-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="0ad36-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0ad36-116">Example 2</span></span>
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

<span data-ttu-id="0ad36-117">Обновление артефакта с помощью inline parameters.</span><span class="sxs-lookup"><span data-stu-id="0ad36-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="0ad36-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0ad36-118">Example 3</span></span>
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

<span data-ttu-id="0ad36-119">Обновление артефакта с помощью ARM шаблона.</span><span class="sxs-lookup"><span data-stu-id="0ad36-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="0ad36-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ad36-120">PARAMETERS</span></span>

### <span data-ttu-id="0ad36-121">-Артефакт</span><span class="sxs-lookup"><span data-stu-id="0ad36-121">-ArtifactFile</span></span>
<span data-ttu-id="0ad36-122">Расположение файла артефакта в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="0ad36-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="0ad36-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="0ad36-123">-Blueprint</span></span>
<span data-ttu-id="0ad36-124">Объект Blueprint.</span><span class="sxs-lookup"><span data-stu-id="0ad36-124">Blueprint object.</span></span>

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

### <span data-ttu-id="0ad36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad36-125">-DefaultProfile</span></span>
<span data-ttu-id="0ad36-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad36-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad36-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="0ad36-127">-DependsOn</span></span>
<span data-ttu-id="0ad36-128">Список имен артефактов, которые необходимо создать перед текущим артефактом.</span><span class="sxs-lookup"><span data-stu-id="0ad36-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="0ad36-129">-Description</span><span class="sxs-lookup"><span data-stu-id="0ad36-129">-Description</span></span>
<span data-ttu-id="0ad36-130">Описание артефакта.</span><span class="sxs-lookup"><span data-stu-id="0ad36-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="0ad36-131">-Name</span><span class="sxs-lookup"><span data-stu-id="0ad36-131">-Name</span></span>
<span data-ttu-id="0ad36-132">Имя артефакта</span><span class="sxs-lookup"><span data-stu-id="0ad36-132">Name of the artifact</span></span>

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

### <span data-ttu-id="0ad36-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0ad36-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="0ad36-134">Определение определения определения политики.</span><span class="sxs-lookup"><span data-stu-id="0ad36-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="0ad36-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="0ad36-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="0ad36-136">Возможность передавать параметры в артефакт определения политики.</span><span class="sxs-lookup"><span data-stu-id="0ad36-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="0ad36-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ad36-137">-ResourceGroupName</span></span>
<span data-ttu-id="0ad36-138">Имя группы ресурсов, под которым будет входить артефакт.</span><span class="sxs-lookup"><span data-stu-id="0ad36-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="0ad36-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0ad36-139">-RoleDefinitionId</span></span>
<span data-ttu-id="0ad36-140">Список определений ролей</span><span class="sxs-lookup"><span data-stu-id="0ad36-140">List of role definition</span></span>

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

### <span data-ttu-id="0ad36-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="0ad36-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="0ad36-142">Список ид определения ролей.</span><span class="sxs-lookup"><span data-stu-id="0ad36-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="0ad36-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="0ad36-143">-TemplateFile</span></span>
<span data-ttu-id="0ad36-144">Расположение файла шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="0ad36-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="0ad36-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="0ad36-145">-TemplateParameterFile</span></span>
<span data-ttu-id="0ad36-146">Расположение файла параметров ARM шаблона на диске.</span><span class="sxs-lookup"><span data-stu-id="0ad36-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="0ad36-147">-Type</span><span class="sxs-lookup"><span data-stu-id="0ad36-147">-Type</span></span>
<span data-ttu-id="0ad36-148">Тип артефакта.</span><span class="sxs-lookup"><span data-stu-id="0ad36-148">Type of the artifact.</span></span>
<span data-ttu-id="0ad36-149">Поддерживаются три типа: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="0ad36-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="0ad36-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ad36-150">-Confirm</span></span>
<span data-ttu-id="0ad36-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0ad36-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ad36-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ad36-152">-WhatIf</span></span>
<span data-ttu-id="0ad36-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ad36-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ad36-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0ad36-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ad36-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad36-155">CommonParameters</span></span>
<span data-ttu-id="0ad36-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad36-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad36-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ad36-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad36-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ad36-158">INPUTS</span></span>

### <span data-ttu-id="0ad36-159">System.String</span><span class="sxs-lookup"><span data-stu-id="0ad36-159">System.String</span></span>

### <span data-ttu-id="0ad36-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="0ad36-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="0ad36-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="0ad36-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="0ad36-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0ad36-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0ad36-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ad36-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0ad36-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0ad36-164">System.String[]</span></span>

## <span data-ttu-id="0ad36-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ad36-165">OUTPUTS</span></span>

### <span data-ttu-id="0ad36-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="0ad36-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="0ad36-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ad36-167">NOTES</span></span>

## <span data-ttu-id="0ad36-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ad36-168">RELATED LINKS</span></span>
