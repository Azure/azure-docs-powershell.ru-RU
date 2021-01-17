---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424151"
---
# <span data-ttu-id="1dc3e-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="1dc3e-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="1dc3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="1dc3e-103">Удаление администратора Azure AD для рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1dc3e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1dc3e-104">SYNTAX</span></span>

### <span data-ttu-id="1dc3e-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1dc3e-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1dc3e-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc3e-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1dc3e-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1dc3e-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dc3e-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dc3e-108">DESCRIPTION</span></span>
<span data-ttu-id="1dc3e-109">При **этом** удаляется администратор Azure Active Directory (Azure AD) для Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="1dc3e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1dc3e-110">EXAMPLES</span></span>

### <span data-ttu-id="1dc3e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1dc3e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="1dc3e-112">Эта команда удаляет администратор Azure AD для рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="1dc3e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dc3e-113">PARAMETERS</span></span>

### <span data-ttu-id="1dc3e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dc3e-114">-AsJob</span></span>
<span data-ttu-id="1dc3e-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1dc3e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dc3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dc3e-116">-DefaultProfile</span></span>
<span data-ttu-id="1dc3e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dc3e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1dc3e-118">-Force</span></span>
<span data-ttu-id="1dc3e-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1dc3e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1dc3e-120">-InputObject</span></span>
<span data-ttu-id="1dc3e-121">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1dc3e-122">-PassThru</span></span>
<span data-ttu-id="1dc3e-123">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1dc3e-124">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1dc3e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dc3e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1dc3e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1dc3e-127">-ResourceId</span></span>
<span data-ttu-id="1dc3e-128">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-128">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3e-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1dc3e-129">-WorkspaceName</span></span>
<span data-ttu-id="1dc3e-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-130">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dc3e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1dc3e-131">-Confirm</span></span>
<span data-ttu-id="1dc3e-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dc3e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dc3e-133">-WhatIf</span></span>
<span data-ttu-id="1dc3e-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dc3e-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dc3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dc3e-136">CommonParameters</span></span>
<span data-ttu-id="1dc3e-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dc3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dc3e-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dc3e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dc3e-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1dc3e-139">INPUTS</span></span>

### <span data-ttu-id="1dc3e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dc3e-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="1dc3e-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1dc3e-141">OUTPUTS</span></span>

### <span data-ttu-id="1dc3e-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1dc3e-142">System.Boolean</span></span>

## <span data-ttu-id="1dc3e-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1dc3e-143">NOTES</span></span>

## <span data-ttu-id="1dc3e-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dc3e-144">RELATED LINKS</span></span>
