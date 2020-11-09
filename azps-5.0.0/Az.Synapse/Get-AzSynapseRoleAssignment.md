---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316877"
---
# <span data-ttu-id="e6b16-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="e6b16-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="e6b16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6b16-102">SYNOPSIS</span></span>
<span data-ttu-id="e6b16-103">Возвращает назначение роли аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="e6b16-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="e6b16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6b16-104">SYNTAX</span></span>

### <span data-ttu-id="e6b16-105">GetByWorkspaceNameAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6b16-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6b16-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6b16-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6b16-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b16-115">DESCRIPTION</span></span>
<span data-ttu-id="e6b16-116">Командлет **Get-AzSynapseRoleAssignment** получает назначение роли Analytics Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b16-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="e6b16-117">Если не указать определение роли или имя участника-пользователя, этот командлет получает все назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="e6b16-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="e6b16-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6b16-118">EXAMPLES</span></span>

### <span data-ttu-id="e6b16-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6b16-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="e6b16-120">Эта команда получает все назначения ролей в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e6b16-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="e6b16-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e6b16-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="e6b16-122">Эта команда получает все назначения ролей в рабочей области ContosoWorkspace с именем role ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="e6b16-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="e6b16-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e6b16-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="e6b16-124">Эта команда получает назначение роли в разделе Рабочая область ContosoWorkspace с именем роли ContosoRole и именем участника-пользователя ContosoName.</span><span class="sxs-lookup"><span data-stu-id="e6b16-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="e6b16-125">Пример 4</span><span class="sxs-lookup"><span data-stu-id="e6b16-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="e6b16-126">Эта команда получает все назначения ролей в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6b16-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="e6b16-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6b16-127">PARAMETERS</span></span>

### <span data-ttu-id="e6b16-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6b16-128">-DefaultProfile</span></span>
<span data-ttu-id="e6b16-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6b16-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6b16-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e6b16-130">-ObjectId</span></span>
<span data-ttu-id="e6b16-131">ИД служб Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="e6b16-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="e6b16-132">-RoleAssignmentId</span></span>
<span data-ttu-id="e6b16-133">Идентификатор назначения роли.</span><span class="sxs-lookup"><span data-stu-id="e6b16-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e6b16-134">-RoleDefinitionId</span></span>
<span data-ttu-id="e6b16-135">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="e6b16-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="e6b16-136">-RoleDefinitionName</span></span>
<span data-ttu-id="e6b16-137">Имя роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="e6b16-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-138">-Намерено</span><span class="sxs-lookup"><span data-stu-id="e6b16-138">-ServicePrincipalName</span></span>
<span data-ttu-id="e6b16-139">Значение параметра безопасности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="e6b16-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="e6b16-140">-SignInName</span></span>
<span data-ttu-id="e6b16-141">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6b16-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6b16-142">-WorkspaceName</span></span>
<span data-ttu-id="e6b16-143">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e6b16-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6b16-144">-WorkspaceObject</span></span>
<span data-ttu-id="e6b16-145">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e6b16-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6b16-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6b16-146">CommonParameters</span></span>
<span data-ttu-id="e6b16-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6b16-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6b16-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6b16-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6b16-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6b16-149">INPUTS</span></span>

### <span data-ttu-id="e6b16-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6b16-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="e6b16-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6b16-151">OUTPUTS</span></span>

### <span data-ttu-id="e6b16-152">Microsoft. Azure. Commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="e6b16-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="e6b16-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6b16-153">NOTES</span></span>

## <span data-ttu-id="e6b16-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6b16-154">RELATED LINKS</span></span>
