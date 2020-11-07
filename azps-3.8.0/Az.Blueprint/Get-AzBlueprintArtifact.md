---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: d8541285cb8cef0565a06715910ff5b8cc8cc392
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93911805"
---
# <span data-ttu-id="b7e72-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="b7e72-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="b7e72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7e72-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e72-103">Получение артефактов из определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="b7e72-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="b7e72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7e72-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7e72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7e72-105">DESCRIPTION</span></span>
<span data-ttu-id="b7e72-106">Получение артефактов из определения чертежа.</span><span class="sxs-lookup"><span data-stu-id="b7e72-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="b7e72-107">Если версия определения схемы не задана, извлекается черновая версия.</span><span class="sxs-lookup"><span data-stu-id="b7e72-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="b7e72-108">В случае отсутствия черновой версии возвращается последнее определение опубликованного чертежа.</span><span class="sxs-lookup"><span data-stu-id="b7e72-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="b7e72-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7e72-109">EXAMPLES</span></span>

### <span data-ttu-id="b7e72-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7e72-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="b7e72-111">Получение артефактов из определения чертежа...</span><span class="sxs-lookup"><span data-stu-id="b7e72-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="b7e72-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7e72-112">PARAMETERS</span></span>

### <span data-ttu-id="b7e72-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="b7e72-113">-ArtifactFile</span></span>
<span data-ttu-id="b7e72-114">Расположение файла артефакта в формате JSON на диске.</span><span class="sxs-lookup"><span data-stu-id="b7e72-114">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="b7e72-115">-Чертеж</span><span class="sxs-lookup"><span data-stu-id="b7e72-115">-Blueprint</span></span>
<span data-ttu-id="b7e72-116">Объект чертежа.</span><span class="sxs-lookup"><span data-stu-id="b7e72-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="b7e72-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="b7e72-117">-BlueprintVersion</span></span>
<span data-ttu-id="b7e72-118">Версия чертежа, из которой нужно получить артефакты.</span><span class="sxs-lookup"><span data-stu-id="b7e72-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e72-119">-DefaultProfile</span></span>
<span data-ttu-id="b7e72-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7e72-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e72-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="b7e72-121">-DependsOn</span></span>
<span data-ttu-id="b7e72-122">Список имен артефактов, которые необходимо создать перед созданием текущего артефакта.</span><span class="sxs-lookup"><span data-stu-id="b7e72-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="b7e72-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="b7e72-123">-Description</span></span>
<span data-ttu-id="b7e72-124">Описание артефакта.</span><span class="sxs-lookup"><span data-stu-id="b7e72-124">Description of the artifact.</span></span>

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

### <span data-ttu-id="b7e72-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7e72-125">-Name</span></span>
<span data-ttu-id="b7e72-126">Имя артефакта</span><span class="sxs-lookup"><span data-stu-id="b7e72-126">Name of the artifact</span></span>

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

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e72-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b7e72-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="b7e72-128">Идентификатор определения политики.</span><span class="sxs-lookup"><span data-stu-id="b7e72-128">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="b7e72-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="b7e72-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="b7e72-130">Хэш-таблица параметров, передаваемая артефакту определения политики.</span><span class="sxs-lookup"><span data-stu-id="b7e72-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="b7e72-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7e72-131">-ResourceGroupName</span></span>
<span data-ttu-id="b7e72-132">Имя группы ресурсов, под которой будет находиться артефакт.</span><span class="sxs-lookup"><span data-stu-id="b7e72-132">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="b7e72-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b7e72-133">-RoleDefinitionId</span></span>
<span data-ttu-id="b7e72-134">Список определений ролей</span><span class="sxs-lookup"><span data-stu-id="b7e72-134">List of role definition</span></span>

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

### <span data-ttu-id="b7e72-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="b7e72-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="b7e72-136">Список идентификаторов участников определения роли.</span><span class="sxs-lookup"><span data-stu-id="b7e72-136">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="b7e72-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="b7e72-137">-TemplateFile</span></span>
<span data-ttu-id="b7e72-138">Расположение файла шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="b7e72-138">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="b7e72-139">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="b7e72-139">-TemplateParameterFile</span></span>
<span data-ttu-id="b7e72-140">Расположение файла параметров шаблона ARM на диске.</span><span class="sxs-lookup"><span data-stu-id="b7e72-140">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="b7e72-141">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="b7e72-141">-Type</span></span>
<span data-ttu-id="b7e72-142">Тип артефакта.</span><span class="sxs-lookup"><span data-stu-id="b7e72-142">Type of the artifact.</span></span>
<span data-ttu-id="b7e72-143">Поддерживаются три типа: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span><span class="sxs-lookup"><span data-stu-id="b7e72-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="b7e72-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7e72-144">-Confirm</span></span>
<span data-ttu-id="b7e72-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b7e72-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e72-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e72-146">-WhatIf</span></span>
<span data-ttu-id="b7e72-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b7e72-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e72-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b7e72-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7e72-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e72-149">CommonParameters</span></span>
<span data-ttu-id="b7e72-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7e72-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b7e72-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7e72-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e72-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7e72-152">INPUTS</span></span>

### <span data-ttu-id="b7e72-153">System. String</span><span class="sxs-lookup"><span data-stu-id="b7e72-153">System.String</span></span>

### <span data-ttu-id="b7e72-154">Microsoft. Azure. Commands. чертеж. Models. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="b7e72-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="b7e72-155">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="b7e72-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="b7e72-156">System. Collections. Generic. List "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="b7e72-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="b7e72-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7e72-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b7e72-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="b7e72-158">System.String[]</span></span>

## <span data-ttu-id="b7e72-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7e72-159">OUTPUTS</span></span>

### <span data-ttu-id="b7e72-160">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="b7e72-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="b7e72-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7e72-161">NOTES</span></span>

## <span data-ttu-id="b7e72-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7e72-162">RELATED LINKS</span></span>
