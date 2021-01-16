---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlactivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlActiveDirectoryAdministrator.md
ms.openlocfilehash: 21d7169f18a999f84adbc568da18c90cb2aa2424
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399871"
---
# <span data-ttu-id="8645b-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="8645b-101">Remove-AzSynapseSqlActiveDirectoryAdministrator</span></span>

## <span data-ttu-id="8645b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8645b-102">SYNOPSIS</span></span>
<span data-ttu-id="8645b-103">Удаление администратора Azure AD для рабочей области Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8645b-103">Removes an Azure AD administrator for Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="8645b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8645b-104">SYNTAX</span></span>

### <span data-ttu-id="8645b-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8645b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator [-ResourceGroupName <String>] -WorkspaceName <String>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8645b-106">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8645b-106">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -InputObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8645b-107">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8645b-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlActiveDirectoryAdministrator -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8645b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8645b-108">DESCRIPTION</span></span>
<span data-ttu-id="8645b-109">При **этом** удаляется администратор Azure Active Directory (Azure AD) для Azure Synapse Analytics Workspace.</span><span class="sxs-lookup"><span data-stu-id="8645b-109">The **Remove-AzSynapseSqlActiveDirectoryAdministrator** cmdlet removes an Azure Active Directory (Azure AD) administrator for Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="8645b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8645b-110">EXAMPLES</span></span>

### <span data-ttu-id="8645b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8645b-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlActiveDirectoryAdministrator -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="8645b-112">Эта команда удаляет администратор Azure AD для рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="8645b-112">This command removes the Azure AD administrator for the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="8645b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8645b-113">PARAMETERS</span></span>

### <span data-ttu-id="8645b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8645b-114">-AsJob</span></span>
<span data-ttu-id="8645b-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8645b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8645b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8645b-116">-DefaultProfile</span></span>
<span data-ttu-id="8645b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8645b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8645b-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8645b-118">-Force</span></span>
<span data-ttu-id="8645b-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8645b-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8645b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8645b-120">-InputObject</span></span>
<span data-ttu-id="8645b-121">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="8645b-121">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8645b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8645b-122">-PassThru</span></span>
<span data-ttu-id="8645b-123">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8645b-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8645b-124">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="8645b-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="8645b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8645b-125">-ResourceGroupName</span></span>
<span data-ttu-id="8645b-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8645b-126">Resource group name.</span></span>

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

### <span data-ttu-id="8645b-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8645b-127">-ResourceId</span></span>
<span data-ttu-id="8645b-128">Идентификатор ресурса рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8645b-128">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="8645b-129">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8645b-129">-WorkspaceName</span></span>
<span data-ttu-id="8645b-130">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8645b-130">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8645b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8645b-131">-Confirm</span></span>
<span data-ttu-id="8645b-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8645b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8645b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8645b-133">-WhatIf</span></span>
<span data-ttu-id="8645b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8645b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8645b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8645b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8645b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8645b-136">CommonParameters</span></span>
<span data-ttu-id="8645b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8645b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8645b-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8645b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8645b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8645b-139">INPUTS</span></span>

### <span data-ttu-id="8645b-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8645b-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8645b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8645b-141">OUTPUTS</span></span>

### <span data-ttu-id="8645b-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8645b-142">System.Boolean</span></span>

## <span data-ttu-id="8645b-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8645b-143">NOTES</span></span>

## <span data-ttu-id="8645b-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8645b-144">RELATED LINKS</span></span>
