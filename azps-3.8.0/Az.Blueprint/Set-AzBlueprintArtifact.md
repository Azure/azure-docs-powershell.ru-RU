---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: c71a587dc755ae1834198f14142d5a511fe17ea2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065457"
---
# <span data-ttu-id="44d39-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="44d39-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="44d39-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44d39-102">SYNOPSIS</span></span>
<span data-ttu-id="44d39-103">Обновление артефакта в определении чертежа.</span><span class="sxs-lookup"><span data-stu-id="44d39-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="44d39-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44d39-104">SYNTAX</span></span>


### <span data-ttu-id="44d39-105">UpdateTemplateArtifact (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44d39-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44d39-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="44d39-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44d39-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="44d39-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44d39-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="44d39-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44d39-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44d39-109">DESCRIPTION</span></span>
<span data-ttu-id="44d39-110">Обновите артефакт.</span><span class="sxs-lookup"><span data-stu-id="44d39-110">Update an artifact.</span></span> <span data-ttu-id="44d39-111">Изменить артефакт можно двумя способами: с помощью артефакта JSON в качестве входного файла или посредством предоставления встроенных параметров для артефакта.</span><span class="sxs-lookup"><span data-stu-id="44d39-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="44d39-112">Несмотря на то, что в методе JSON не требуется тип артефакта, который должен предоставляться в методе линейного параметра, необходимо, чтобы пользователь предоставил тип параметра артефакта с помощью типа.</span><span class="sxs-lookup"><span data-stu-id="44d39-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="44d39-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44d39-113">EXAMPLES</span></span>

### <span data-ttu-id="44d39-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44d39-114">Example 1</span></span>
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

<span data-ttu-id="44d39-115">Обновите артефакт с помощью JSON – файла артефакта.</span><span class="sxs-lookup"><span data-stu-id="44d39-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="44d39-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="44d39-116">Example 2</span></span>
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

<span data-ttu-id="44d39-117">Обновите артефакт с помощью встроенных параметров.</span><span class="sxs-lookup"><span data-stu-id="44d39-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="44d39-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="44d39-118">Example 3</span></span>
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

<span data-ttu-id="44d39-119">Обновление артефакта с помощью файла шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="44d39-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="44d39-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44d39-120">PARAMETERS</span></span>

### <span data-ttu-id="44d39-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="44d39-121">-ArtifactFile</span></span>
<span data-ttu-id="44d39-122">Расположение файла артефакта в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="44d39-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-123">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="44d39-123">-Blueprint</span></span>
<span data-ttu-id="44d39-124">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="44d39-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d39-125">-DefaultProfile</span></span>
<span data-ttu-id="44d39-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44d39-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="44d39-127">-DependsOn</span></span>
<span data-ttu-id="44d39-128">Список имен артефактов, которые необходимо создать перед созданием текущего артефакта.</span><span class="sxs-lookup"><span data-stu-id="44d39-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-129">-Описание</span><span class="sxs-lookup"><span data-stu-id="44d39-129">-Description</span></span>
<span data-ttu-id="44d39-130">Описание артефакта.</span><span class="sxs-lookup"><span data-stu-id="44d39-130">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44d39-131">-Name</span></span>
<span data-ttu-id="44d39-132">Имя артефакта</span><span class="sxs-lookup"><span data-stu-id="44d39-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="44d39-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="44d39-134">Идентификатор определения политики.</span><span class="sxs-lookup"><span data-stu-id="44d39-134">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="44d39-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="44d39-136">Хэш-таблица параметров, передаваемая артефакту определения политики.</span><span class="sxs-lookup"><span data-stu-id="44d39-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d39-137">-ResourceGroupName</span></span>
<span data-ttu-id="44d39-138">Имя группы ресурсов, под которой будет находиться артефакт.</span><span class="sxs-lookup"><span data-stu-id="44d39-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="44d39-139">-RoleDefinitionId</span></span>
<span data-ttu-id="44d39-140">Список определений ролей</span><span class="sxs-lookup"><span data-stu-id="44d39-140">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="44d39-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="44d39-142">Список идентификаторов участников определения роли.</span><span class="sxs-lookup"><span data-stu-id="44d39-142">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="44d39-143">-TemplateFile</span></span>
<span data-ttu-id="44d39-144">Расположение файла шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="44d39-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="44d39-145">-TemplateParameterFile</span></span>
<span data-ttu-id="44d39-146">Расположение файла параметров шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="44d39-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-147">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="44d39-147">-Type</span></span>
<span data-ttu-id="44d39-148">Тип артефакта.</span><span class="sxs-lookup"><span data-stu-id="44d39-148">Type of the artifact.</span></span>
<span data-ttu-id="44d39-149">Поддерживаются три типа: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="44d39-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44d39-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d39-150">CommonParameters</span></span>
<span data-ttu-id="44d39-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44d39-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="44d39-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d39-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d39-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44d39-153">INPUTS</span></span>

### <span data-ttu-id="44d39-154">System. String</span><span class="sxs-lookup"><span data-stu-id="44d39-154">System.String</span></span>

### <span data-ttu-id="44d39-155">Microsoft. Azure. Commands. чертеж. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="44d39-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="44d39-156">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="44d39-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="44d39-157">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="44d39-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="44d39-158">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="44d39-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="44d39-159">System. String []</span><span class="sxs-lookup"><span data-stu-id="44d39-159">System.String[]</span></span>

## <span data-ttu-id="44d39-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44d39-160">OUTPUTS</span></span>

### <span data-ttu-id="44d39-161">Microsoft. Azure. Management. чертежи. Models. артефакт</span><span class="sxs-lookup"><span data-stu-id="44d39-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="44d39-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="44d39-162">NOTES</span></span>

## <span data-ttu-id="44d39-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44d39-163">RELATED LINKS</span></span>
