---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 4fbc25b919b7fbb3caa972f4e64467dee1df7116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008243"
---
# <span data-ttu-id="db5fe-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="db5fe-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="db5fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db5fe-102">SYNOPSIS</span></span>
<span data-ttu-id="db5fe-103">Удаляет назначение роли Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="db5fe-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="db5fe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db5fe-104">SYNTAX</span></span>

### <span data-ttu-id="db5fe-105">RemoveByWorkspaceNameAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db5fe-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5fe-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5fe-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5fe-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5fe-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5fe-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db5fe-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db5fe-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db5fe-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="db5fe-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="db5fe-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db5fe-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db5fe-115">DESCRIPTION</span></span>
<span data-ttu-id="db5fe-116">При наступлении функции **Remove-AzSynapseRoleAssignment** назначение роли Azure Synapse Analytics удаляется без возможности выполнения.</span><span class="sxs-lookup"><span data-stu-id="db5fe-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="db5fe-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db5fe-117">EXAMPLES</span></span>

### <span data-ttu-id="db5fe-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db5fe-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="db5fe-119">Эта команда удаляет назначение роли Azure Synapse Analytics с помощью ее ИД.</span><span class="sxs-lookup"><span data-stu-id="db5fe-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="db5fe-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db5fe-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="db5fe-121">Эта команда удаляет назначение роли Azure Synapse Analytics с именем роли и именем директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="db5fe-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="db5fe-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="db5fe-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="db5fe-123">Эта команда удаляет назначение ролей Azure Synapse Analytics с помощью ID назначения ролей в конвейере.</span><span class="sxs-lookup"><span data-stu-id="db5fe-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="db5fe-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db5fe-124">PARAMETERS</span></span>

### <span data-ttu-id="db5fe-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db5fe-125">-AsJob</span></span>
<span data-ttu-id="db5fe-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="db5fe-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db5fe-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5fe-127">-DefaultProfile</span></span>
<span data-ttu-id="db5fe-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db5fe-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5fe-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db5fe-129">-ObjectId</span></span>
<span data-ttu-id="db5fe-130">ОбъектId Azure AD пользователя, группы или директора службы.</span><span class="sxs-lookup"><span data-stu-id="db5fe-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="db5fe-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db5fe-131">-PassThru</span></span>
<span data-ttu-id="db5fe-132">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db5fe-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="db5fe-133">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="db5fe-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="db5fe-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="db5fe-134">-RoleAssignmentId</span></span>
<span data-ttu-id="db5fe-135">ИД назначения роли.</span><span class="sxs-lookup"><span data-stu-id="db5fe-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="db5fe-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="db5fe-136">-RoleDefinitionId</span></span>
<span data-ttu-id="db5fe-137">ИД роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="db5fe-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="db5fe-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="db5fe-138">-RoleDefinitionName</span></span>
<span data-ttu-id="db5fe-139">Имя роли, которая назначена основному.</span><span class="sxs-lookup"><span data-stu-id="db5fe-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="db5fe-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="db5fe-140">-ServicePrincipalName</span></span>
<span data-ttu-id="db5fe-141">ServicePrincipalName основной услуги.</span><span class="sxs-lookup"><span data-stu-id="db5fe-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="db5fe-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="db5fe-142">-SignInName</span></span>
<span data-ttu-id="db5fe-143">Адрес электронной почты или имя директора пользователя.</span><span class="sxs-lookup"><span data-stu-id="db5fe-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="db5fe-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db5fe-144">-WorkspaceName</span></span>
<span data-ttu-id="db5fe-145">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="db5fe-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="db5fe-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="db5fe-146">-WorkspaceObject</span></span>
<span data-ttu-id="db5fe-147">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="db5fe-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="db5fe-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db5fe-148">-Confirm</span></span>
<span data-ttu-id="db5fe-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5fe-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5fe-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5fe-150">-WhatIf</span></span>
<span data-ttu-id="db5fe-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5fe-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db5fe-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db5fe-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5fe-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5fe-153">CommonParameters</span></span>
<span data-ttu-id="db5fe-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5fe-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5fe-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db5fe-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5fe-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db5fe-156">INPUTS</span></span>

### <span data-ttu-id="db5fe-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="db5fe-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="db5fe-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db5fe-158">OUTPUTS</span></span>

### <span data-ttu-id="db5fe-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="db5fe-159">System.Boolean</span></span>

## <span data-ttu-id="db5fe-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db5fe-160">NOTES</span></span>

## <span data-ttu-id="db5fe-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db5fe-161">RELATED LINKS</span></span>
