---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216796"
---
# <span data-ttu-id="d8dd7-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d8dd7-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="d8dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="d8dd7-103">Удаляет назначение роли Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="d8dd7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8dd7-104">SYNTAX</span></span>

### <span data-ttu-id="d8dd7-105">RemoveByWorkspaceNameAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8dd7-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8dd7-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8dd7-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8dd7-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8dd7-115">DESCRIPTION</span></span>
<span data-ttu-id="d8dd7-116">Cmdlet **Remove-AzSynapseRoleAssignment** окончательно удаляет назначение ролей Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="d8dd7-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8dd7-117">EXAMPLES</span></span>

### <span data-ttu-id="d8dd7-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8dd7-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="d8dd7-119">Эта команда удаляет назначение ролей Azure Synapse Analytics с помощью ИД назначения роли.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="d8dd7-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8dd7-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="d8dd7-121">Эта команда удаляет назначение роли Azure Synapse Analytics с именем роли и именем директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="d8dd7-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d8dd7-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="d8dd7-123">Эта команда удаляет назначение роли Azure Synapse Analytics с помощью ИД назначения роли в конвейере.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="d8dd7-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8dd7-124">PARAMETERS</span></span>

### <span data-ttu-id="d8dd7-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8dd7-125">-AsJob</span></span>
<span data-ttu-id="d8dd7-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8dd7-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8dd7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8dd7-127">-DefaultProfile</span></span>
<span data-ttu-id="d8dd7-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8dd7-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d8dd7-129">-ObjectId</span></span>
<span data-ttu-id="d8dd7-130">ОбъектId Azure AD пользователя, группы или директора службы.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8dd7-131">-PassThru</span></span>
<span data-ttu-id="d8dd7-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d8dd7-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d8dd7-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="d8dd7-134">-RoleAssignmentId</span></span>
<span data-ttu-id="d8dd7-135">ИД назначения роли.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d8dd7-136">-RoleDefinitionId</span></span>
<span data-ttu-id="d8dd7-137">ИД роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d8dd7-138">-RoleDefinitionName</span></span>
<span data-ttu-id="d8dd7-139">Имя роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8dd7-140">-ServicePrincipalName</span></span>
<span data-ttu-id="d8dd7-141">ServicePrincipalName основной услуги.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d8dd7-142">-SignInName</span></span>
<span data-ttu-id="d8dd7-143">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8dd7-144">-WorkspaceName</span></span>
<span data-ttu-id="d8dd7-145">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8dd7-146">-WorkspaceObject</span></span>
<span data-ttu-id="d8dd7-147">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8dd7-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8dd7-148">-Confirm</span></span>
<span data-ttu-id="d8dd7-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8dd7-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8dd7-150">-WhatIf</span></span>
<span data-ttu-id="d8dd7-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8dd7-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8dd7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8dd7-153">CommonParameters</span></span>
<span data-ttu-id="d8dd7-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8dd7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8dd7-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8dd7-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8dd7-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8dd7-156">INPUTS</span></span>

### <span data-ttu-id="d8dd7-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8dd7-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d8dd7-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8dd7-158">OUTPUTS</span></span>

### <span data-ttu-id="d8dd7-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8dd7-159">System.Boolean</span></span>

## <span data-ttu-id="d8dd7-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8dd7-160">NOTES</span></span>

## <span data-ttu-id="d8dd7-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8dd7-161">RELATED LINKS</span></span>
