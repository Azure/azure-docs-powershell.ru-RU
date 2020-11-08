---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246317"
---
# <span data-ttu-id="79a67-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="79a67-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="79a67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79a67-102">SYNOPSIS</span></span>
<span data-ttu-id="79a67-103">Создание назначения роли аналитики Synapse.</span><span class="sxs-lookup"><span data-stu-id="79a67-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="79a67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79a67-104">SYNTAX</span></span>

### <span data-ttu-id="79a67-105">NewByWorkspaceNameAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79a67-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a67-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a67-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a67-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a67-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a67-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a67-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a67-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="79a67-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79a67-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79a67-113">DESCRIPTION</span></span>
<span data-ttu-id="79a67-114">Командлет **New-AzSynapseRoleAssignment** создает назначение роли Analytics для Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="79a67-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="79a67-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79a67-115">EXAMPLES</span></span>

### <span data-ttu-id="79a67-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79a67-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="79a67-117">Эта команда назначает ContosoRole пользователю, чье имя участника — ContosoName.</span><span class="sxs-lookup"><span data-stu-id="79a67-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="79a67-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="79a67-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="79a67-119">Эта команда назначает ContosoRole пользователю, имя участника которого ContosoName через конвейер.</span><span class="sxs-lookup"><span data-stu-id="79a67-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="79a67-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79a67-120">PARAMETERS</span></span>

### <span data-ttu-id="79a67-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79a67-121">-AsJob</span></span>
<span data-ttu-id="79a67-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="79a67-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79a67-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a67-123">-DefaultProfile</span></span>
<span data-ttu-id="79a67-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79a67-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a67-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="79a67-125">-ObjectId</span></span>
<span data-ttu-id="79a67-126">ИД служб Azure AD ObjectId для пользователя, группы или участника-службы.</span><span class="sxs-lookup"><span data-stu-id="79a67-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="79a67-127">-RoleDefinitionId</span></span>
<span data-ttu-id="79a67-128">Идентификатор роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="79a67-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="79a67-129">-RoleDefinitionName</span></span>
<span data-ttu-id="79a67-130">Имя роли, назначенной участнику.</span><span class="sxs-lookup"><span data-stu-id="79a67-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-131">-Намерено</span><span class="sxs-lookup"><span data-stu-id="79a67-131">-ServicePrincipalName</span></span>
<span data-ttu-id="79a67-132">Значение параметра безопасности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="79a67-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="79a67-133">-SignInName</span></span>
<span data-ttu-id="79a67-134">Адрес электронной почты или имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="79a67-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="79a67-135">-WorkspaceName</span></span>
<span data-ttu-id="79a67-136">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="79a67-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="79a67-137">-WorkspaceObject</span></span>
<span data-ttu-id="79a67-138">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="79a67-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79a67-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79a67-139">-Confirm</span></span>
<span data-ttu-id="79a67-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79a67-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a67-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a67-141">-WhatIf</span></span>
<span data-ttu-id="79a67-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79a67-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a67-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79a67-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a67-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a67-144">CommonParameters</span></span>
<span data-ttu-id="79a67-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79a67-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a67-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79a67-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a67-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79a67-147">INPUTS</span></span>

### <span data-ttu-id="79a67-148">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="79a67-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="79a67-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79a67-149">OUTPUTS</span></span>

### <span data-ttu-id="79a67-150">Microsoft. Azure. Commands. Synapse. Models. PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="79a67-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="79a67-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="79a67-151">NOTES</span></span>

## <span data-ttu-id="79a67-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79a67-152">RELATED LINKS</span></span>
