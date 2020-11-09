---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246092"
---
# <span data-ttu-id="525b1-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="525b1-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="525b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="525b1-102">SYNOPSIS</span></span>
<span data-ttu-id="525b1-103">Обновление артефакта в определении чертежа.</span><span class="sxs-lookup"><span data-stu-id="525b1-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="525b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="525b1-104">SYNTAX</span></span>

### <span data-ttu-id="525b1-105">UpdateTemplateArtifact (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="525b1-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="525b1-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="525b1-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="525b1-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="525b1-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="525b1-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="525b1-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="525b1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="525b1-109">DESCRIPTION</span></span>
<span data-ttu-id="525b1-110">Обновите артефакт.</span><span class="sxs-lookup"><span data-stu-id="525b1-110">Update an artifact.</span></span> <span data-ttu-id="525b1-111">Изменить артефакт можно двумя способами: с помощью артефакта JSON в качестве входного файла или посредством предоставления встроенных параметров для артефакта.</span><span class="sxs-lookup"><span data-stu-id="525b1-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="525b1-112">Несмотря на то, что в методе JSON не требуется тип артефакта, который должен предоставляться в методе линейного параметра, необходимо, чтобы пользователь предоставил тип параметра артефакта с помощью типа.</span><span class="sxs-lookup"><span data-stu-id="525b1-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="525b1-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="525b1-113">EXAMPLES</span></span>

### <span data-ttu-id="525b1-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="525b1-114">Example 1</span></span>
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

<span data-ttu-id="525b1-115">Обновите артефакт с помощью JSON – файла артефакта.</span><span class="sxs-lookup"><span data-stu-id="525b1-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="525b1-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="525b1-116">Example 2</span></span>
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

<span data-ttu-id="525b1-117">Обновите артефакт с помощью встроенных параметров.</span><span class="sxs-lookup"><span data-stu-id="525b1-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="525b1-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="525b1-118">Example 3</span></span>
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

<span data-ttu-id="525b1-119">Обновление артефакта с помощью файла шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="525b1-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="525b1-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="525b1-120">PARAMETERS</span></span>

### <span data-ttu-id="525b1-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="525b1-121">-ArtifactFile</span></span>
<span data-ttu-id="525b1-122">Расположение файла артефакта в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="525b1-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="525b1-123">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="525b1-123">-Blueprint</span></span>
<span data-ttu-id="525b1-124">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="525b1-124">Blueprint object.</span></span>

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

### <span data-ttu-id="525b1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="525b1-125">-DefaultProfile</span></span>
<span data-ttu-id="525b1-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="525b1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="525b1-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="525b1-127">-DependsOn</span></span>
<span data-ttu-id="525b1-128">Список имен артефактов, которые необходимо создать перед созданием текущего артефакта.</span><span class="sxs-lookup"><span data-stu-id="525b1-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="525b1-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="525b1-129">-Description</span></span>
<span data-ttu-id="525b1-130">Описание артефакта.</span><span class="sxs-lookup"><span data-stu-id="525b1-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="525b1-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="525b1-131">-Name</span></span>
<span data-ttu-id="525b1-132">Имя артефакта</span><span class="sxs-lookup"><span data-stu-id="525b1-132">Name of the artifact</span></span>

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

### <span data-ttu-id="525b1-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="525b1-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="525b1-134">Идентификатор определения политики.</span><span class="sxs-lookup"><span data-stu-id="525b1-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="525b1-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="525b1-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="525b1-136">Хэш-таблица параметров, передаваемая артефакту определения политики.</span><span class="sxs-lookup"><span data-stu-id="525b1-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="525b1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="525b1-137">-ResourceGroupName</span></span>
<span data-ttu-id="525b1-138">Имя группы ресурсов, под которой будет находиться артефакт.</span><span class="sxs-lookup"><span data-stu-id="525b1-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="525b1-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="525b1-139">-RoleDefinitionId</span></span>
<span data-ttu-id="525b1-140">Список определений ролей</span><span class="sxs-lookup"><span data-stu-id="525b1-140">List of role definition</span></span>

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

### <span data-ttu-id="525b1-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="525b1-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="525b1-142">Список идентификаторов участников определения роли.</span><span class="sxs-lookup"><span data-stu-id="525b1-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="525b1-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="525b1-143">-TemplateFile</span></span>
<span data-ttu-id="525b1-144">Расположение файла шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="525b1-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="525b1-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="525b1-145">-TemplateParameterFile</span></span>
<span data-ttu-id="525b1-146">Расположение файла параметров шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="525b1-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="525b1-147">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="525b1-147">-Type</span></span>
<span data-ttu-id="525b1-148">Тип артефакта.</span><span class="sxs-lookup"><span data-stu-id="525b1-148">Type of the artifact.</span></span>
<span data-ttu-id="525b1-149">Поддерживаются три типа: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="525b1-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="525b1-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="525b1-150">-Confirm</span></span>
<span data-ttu-id="525b1-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="525b1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="525b1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="525b1-152">-WhatIf</span></span>
<span data-ttu-id="525b1-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="525b1-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="525b1-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="525b1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="525b1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="525b1-155">CommonParameters</span></span>
<span data-ttu-id="525b1-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="525b1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="525b1-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="525b1-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="525b1-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="525b1-158">INPUTS</span></span>

### <span data-ttu-id="525b1-159">System. String</span><span class="sxs-lookup"><span data-stu-id="525b1-159">System.String</span></span>

### <span data-ttu-id="525b1-160">Microsoft. Azure. Commands. чертеж. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="525b1-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="525b1-161">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="525b1-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="525b1-162">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="525b1-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="525b1-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="525b1-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="525b1-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="525b1-164">System.String[]</span></span>

## <span data-ttu-id="525b1-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="525b1-165">OUTPUTS</span></span>

### <span data-ttu-id="525b1-166">Microsoft. Azure. Management. чертежи. Models. артефакт</span><span class="sxs-lookup"><span data-stu-id="525b1-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="525b1-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="525b1-167">NOTES</span></span>

## <span data-ttu-id="525b1-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="525b1-168">RELATED LINKS</span></span>