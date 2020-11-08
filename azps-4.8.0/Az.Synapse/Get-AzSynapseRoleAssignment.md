---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077481"
---
# <span data-ttu-id="0306b-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="0306b-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="0306b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0306b-102">SYNOPSIS</span></span>
<span data-ttu-id="0306b-103">Возвращает назначение роли аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="0306b-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="0306b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0306b-104">SYNTAX</span></span>

### <span data-ttu-id="0306b-105">GetByWorkspaceNameAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0306b-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0306b-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0306b-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0306b-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0306b-115">DESCRIPTION</span></span>
<span data-ttu-id="0306b-116">Командлет **Get-AzSynapseRoleAssignment** получает назначение роли Analytics Synapse Azure.</span><span class="sxs-lookup"><span data-stu-id="0306b-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="0306b-117">Если не указать определение роли или имя участника-пользователя, этот командлет получает все назначения ролей.</span><span class="sxs-lookup"><span data-stu-id="0306b-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="0306b-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0306b-118">EXAMPLES</span></span>

### <span data-ttu-id="0306b-119">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0306b-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0306b-120">Эта команда получает все назначения ролей в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0306b-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="0306b-121">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0306b-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="0306b-122">Эта команда получает все назначения ролей в рабочей области ContosoWorkspace с именем role ContosoRole.</span><span class="sxs-lookup"><span data-stu-id="0306b-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="0306b-123">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0306b-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="0306b-124">Эта команда получает назначение роли в разделе Рабочая область ContosoWorkspace с именем роли ContosoRole и именем участника-пользователя ContosoName.</span><span class="sxs-lookup"><span data-stu-id="0306b-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="0306b-125">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0306b-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="0306b-126">Эта команда получает все назначения ролей в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="0306b-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="0306b-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0306b-127">PARAMETERS</span></span>

### <span data-ttu-id="0306b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0306b-128">-DefaultProfile</span></span>
<span data-ttu-id="0306b-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0306b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0306b-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0306b-130">-ObjectId</span></span>
<span data-ttu-id="0306b-131">ИД служб Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="0306b-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="0306b-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="0306b-132">-RoleAssignmentId</span></span>
<span data-ttu-id="0306b-133">Идентификатор назначения роли.</span><span class="sxs-lookup"><span data-stu-id="0306b-133">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="0306b-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="0306b-134">-RoleDefinitionId</span></span>
<span data-ttu-id="0306b-135">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="0306b-135">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="0306b-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="0306b-136">-RoleDefinitionName</span></span>
<span data-ttu-id="0306b-137">Имя роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="0306b-137">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="0306b-138">-Намерено</span><span class="sxs-lookup"><span data-stu-id="0306b-138">-ServicePrincipalName</span></span>
<span data-ttu-id="0306b-139">Значение параметра безопасности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="0306b-139">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="0306b-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="0306b-140">-SignInName</span></span>
<span data-ttu-id="0306b-141">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="0306b-141">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="0306b-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0306b-142">-WorkspaceName</span></span>
<span data-ttu-id="0306b-143">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0306b-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="0306b-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0306b-144">-WorkspaceObject</span></span>
<span data-ttu-id="0306b-145">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="0306b-145">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="0306b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0306b-146">CommonParameters</span></span>
<span data-ttu-id="0306b-147">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0306b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0306b-148">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0306b-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0306b-149">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0306b-149">INPUTS</span></span>

### <span data-ttu-id="0306b-150">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0306b-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0306b-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0306b-151">OUTPUTS</span></span>

### <span data-ttu-id="0306b-152">Microsoft. Azure. Commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="0306b-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="0306b-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="0306b-153">NOTES</span></span>

## <span data-ttu-id="0306b-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0306b-154">RELATED LINKS</span></span>
