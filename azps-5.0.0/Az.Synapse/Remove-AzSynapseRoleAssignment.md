---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319457"
---
# <span data-ttu-id="ef6ca-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="ef6ca-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="ef6ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef6ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ef6ca-103">Удаляет назначение роли аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="ef6ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef6ca-104">SYNTAX</span></span>

### <span data-ttu-id="ef6ca-105">RemoveByWorkspaceNameAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ef6ca-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ef6ca-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef6ca-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef6ca-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef6ca-115">DESCRIPTION</span></span>
<span data-ttu-id="ef6ca-116">Командлет **Remove-AzSynapseRoleAssignment** окончательно удаляет назначение роли Analytics Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="ef6ca-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef6ca-117">EXAMPLES</span></span>

### <span data-ttu-id="ef6ca-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef6ca-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="ef6ca-119">Эта команда удаляет назначение роли Azure Synapse Analytics с ИД назначения роли.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="ef6ca-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ef6ca-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="ef6ca-121">Эта команда удаляет назначение роли Azure Synapse Analytics с именем роли и именем участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="ef6ca-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ef6ca-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="ef6ca-123">Эта команда удаляет назначение роли Azure Synapse Analytics с ИД назначения роли с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="ef6ca-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef6ca-124">PARAMETERS</span></span>

### <span data-ttu-id="ef6ca-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef6ca-125">-AsJob</span></span>
<span data-ttu-id="ef6ca-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ef6ca-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef6ca-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef6ca-127">-DefaultProfile</span></span>
<span data-ttu-id="ef6ca-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef6ca-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ef6ca-129">-ObjectId</span></span>
<span data-ttu-id="ef6ca-130">ИД служб Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="ef6ca-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef6ca-131">-PassThru</span></span>
<span data-ttu-id="ef6ca-132">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ef6ca-133">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ef6ca-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="ef6ca-134">-RoleAssignmentId</span></span>
<span data-ttu-id="ef6ca-135">Идентификатор назначения роли.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="ef6ca-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ef6ca-136">-RoleDefinitionId</span></span>
<span data-ttu-id="ef6ca-137">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="ef6ca-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-138">-RoleDefinitionName</span></span>
<span data-ttu-id="ef6ca-139">Имя роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="ef6ca-140">-Намерено</span><span class="sxs-lookup"><span data-stu-id="ef6ca-140">-ServicePrincipalName</span></span>
<span data-ttu-id="ef6ca-141">Значение параметра безопасности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="ef6ca-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-142">-SignInName</span></span>
<span data-ttu-id="ef6ca-143">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="ef6ca-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ef6ca-144">-WorkspaceName</span></span>
<span data-ttu-id="ef6ca-145">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ef6ca-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ef6ca-146">-WorkspaceObject</span></span>
<span data-ttu-id="ef6ca-147">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ef6ca-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef6ca-148">-Confirm</span></span>
<span data-ttu-id="ef6ca-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef6ca-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef6ca-150">-WhatIf</span></span>
<span data-ttu-id="ef6ca-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef6ca-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef6ca-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef6ca-153">CommonParameters</span></span>
<span data-ttu-id="ef6ca-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef6ca-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef6ca-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef6ca-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef6ca-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef6ca-156">INPUTS</span></span>

### <span data-ttu-id="ef6ca-157">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef6ca-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ef6ca-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef6ca-158">OUTPUTS</span></span>

### <span data-ttu-id="ef6ca-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef6ca-159">System.Boolean</span></span>

## <span data-ttu-id="ef6ca-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef6ca-160">NOTES</span></span>

## <span data-ttu-id="ef6ca-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef6ca-161">RELATED LINKS</span></span>