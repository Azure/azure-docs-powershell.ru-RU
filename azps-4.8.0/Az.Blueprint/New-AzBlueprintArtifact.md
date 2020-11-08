---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079830"
---
# <span data-ttu-id="692f0-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="692f0-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="692f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="692f0-102">SYNOPSIS</span></span>
<span data-ttu-id="692f0-103">Создайте новый артефакт и сохраните его в определении чертежа.</span><span class="sxs-lookup"><span data-stu-id="692f0-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="692f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="692f0-104">SYNTAX</span></span>

### <span data-ttu-id="692f0-105">CreateTemplateArtifact (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="692f0-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="692f0-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="692f0-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="692f0-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="692f0-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="692f0-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="692f0-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="692f0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="692f0-109">DESCRIPTION</span></span>
<span data-ttu-id="692f0-110">Создание нового артефакта.</span><span class="sxs-lookup"><span data-stu-id="692f0-110">Create a new artifact.</span></span> <span data-ttu-id="692f0-111">Создать артефакт можно двумя способами: с помощью артефакта JSON в качестве входного файла или посредством предоставления встроенных параметров для артефакта.</span><span class="sxs-lookup"><span data-stu-id="692f0-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="692f0-112">Несмотря на то, что в методе JSON не требуется тип артефакта, который должен предоставляться в методе линейного параметра, необходимо, чтобы пользователь предоставил тип параметра артефакта с помощью типа.</span><span class="sxs-lookup"><span data-stu-id="692f0-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="692f0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="692f0-113">EXAMPLES</span></span>

### <span data-ttu-id="692f0-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="692f0-114">Example 1</span></span>
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

<span data-ttu-id="692f0-115">Создание нового артефакта с помощью JSON-файла артефакта.</span><span class="sxs-lookup"><span data-stu-id="692f0-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="692f0-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="692f0-116">Example 2</span></span>
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

<span data-ttu-id="692f0-117">Создание нового артефакта с помощью встроенных параметров.</span><span class="sxs-lookup"><span data-stu-id="692f0-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="692f0-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="692f0-118">Example 3</span></span>
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

<span data-ttu-id="692f0-119">Создание нового артефакта с помощью файла шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="692f0-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="692f0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="692f0-120">PARAMETERS</span></span>

### <span data-ttu-id="692f0-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="692f0-121">-ArtifactFile</span></span>
<span data-ttu-id="692f0-122">Расположение файла артефакта в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="692f0-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-123">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="692f0-123">-Blueprint</span></span>
<span data-ttu-id="692f0-124">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="692f0-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692f0-125">-DefaultProfile</span></span>
<span data-ttu-id="692f0-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="692f0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="692f0-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="692f0-127">-DependsOn</span></span>
<span data-ttu-id="692f0-128">Список имен артефактов, которые необходимо создать перед созданием текущего артефакта.</span><span class="sxs-lookup"><span data-stu-id="692f0-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="692f0-129">-Description</span></span>
<span data-ttu-id="692f0-130">Описание артефакта.</span><span class="sxs-lookup"><span data-stu-id="692f0-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="692f0-131">-Name</span></span>
<span data-ttu-id="692f0-132">Имя артефакта</span><span class="sxs-lookup"><span data-stu-id="692f0-132">Name of the artifact</span></span>

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

### <span data-ttu-id="692f0-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="692f0-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="692f0-134">Идентификатор определения политики.</span><span class="sxs-lookup"><span data-stu-id="692f0-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="692f0-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="692f0-136">Хэш-таблица параметров, передаваемая артефакту определения политики.</span><span class="sxs-lookup"><span data-stu-id="692f0-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="692f0-137">-ResourceGroupName</span></span>
<span data-ttu-id="692f0-138">Имя группы ресурсов, под которой будет находиться артефакт.</span><span class="sxs-lookup"><span data-stu-id="692f0-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="692f0-139">-RoleDefinitionId</span></span>
<span data-ttu-id="692f0-140">Список определений ролей</span><span class="sxs-lookup"><span data-stu-id="692f0-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="692f0-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="692f0-142">Список идентификаторов участников определения роли.</span><span class="sxs-lookup"><span data-stu-id="692f0-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="692f0-143">-TemplateFile</span></span>
<span data-ttu-id="692f0-144">Расположение файла шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="692f0-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="692f0-145">-TemplateParameterFile</span></span>
<span data-ttu-id="692f0-146">Расположение файла параметров шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="692f0-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-147">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="692f0-147">-Type</span></span>
<span data-ttu-id="692f0-148">Тип артефакта.</span><span class="sxs-lookup"><span data-stu-id="692f0-148">Type of the artifact.</span></span>
<span data-ttu-id="692f0-149">Поддерживаются три типа: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="692f0-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692f0-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="692f0-150">-Confirm</span></span>
<span data-ttu-id="692f0-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="692f0-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="692f0-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="692f0-152">-WhatIf</span></span>
<span data-ttu-id="692f0-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="692f0-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="692f0-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="692f0-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="692f0-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692f0-155">CommonParameters</span></span>
<span data-ttu-id="692f0-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="692f0-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692f0-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="692f0-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692f0-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="692f0-158">INPUTS</span></span>

### <span data-ttu-id="692f0-159">System. String</span><span class="sxs-lookup"><span data-stu-id="692f0-159">System.String</span></span>

### <span data-ttu-id="692f0-160">Microsoft. Azure. Commands. чертеж. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="692f0-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="692f0-161">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="692f0-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="692f0-162">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="692f0-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="692f0-163">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="692f0-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="692f0-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="692f0-164">System.String[]</span></span>

## <span data-ttu-id="692f0-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="692f0-165">OUTPUTS</span></span>

### <span data-ttu-id="692f0-166">Microsoft. Azure. Management. чертежи. Models. артефакт</span><span class="sxs-lookup"><span data-stu-id="692f0-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="692f0-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="692f0-167">NOTES</span></span>

## <span data-ttu-id="692f0-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="692f0-168">RELATED LINKS</span></span>
