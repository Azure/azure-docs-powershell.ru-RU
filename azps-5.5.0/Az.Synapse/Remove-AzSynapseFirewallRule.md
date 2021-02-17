---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 8dd3321804afb2f7901a8acd22cfdab3dd990c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232428"
---
# <span data-ttu-id="b5ca5-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b5ca5-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="b5ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ca5-103">Удаляет правило брандмауэра synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b5ca5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b5ca5-104">SYNTAX</span></span>

### <span data-ttu-id="b5ca5-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5ca5-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ca5-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5ca5-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5ca5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-107">DESCRIPTION</span></span>
<span data-ttu-id="b5ca5-108">С **помощью cmdlet Remove-AzSynapseFirewallRule** вы удалите правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b5ca5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-109">EXAMPLES</span></span>

### <span data-ttu-id="b5ca5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b5ca5-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="b5ca5-111">Эта команда удаляет правило брандмауэра ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="b5ca5-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b5ca5-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="b5ca5-113">Эта команда удаляет правило брандмауэра ContosoFirewallRule в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="b5ca5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5ca5-114">PARAMETERS</span></span>

### <span data-ttu-id="b5ca5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5ca5-115">-AsJob</span></span>
<span data-ttu-id="b5ca5-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b5ca5-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5ca5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ca5-117">-DefaultProfile</span></span>
<span data-ttu-id="b5ca5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5ca5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b5ca5-119">-Force</span></span>
<span data-ttu-id="b5ca5-120">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b5ca5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b5ca5-121">-Name</span></span>
<span data-ttu-id="b5ca5-122">Имя правила брандмауэра для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-122">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ca5-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5ca5-123">-PassThru</span></span>
<span data-ttu-id="b5ca5-124">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b5ca5-125">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b5ca5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ca5-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5ca5-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ca5-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b5ca5-128">-WorkspaceName</span></span>
<span data-ttu-id="b5ca5-129">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-129">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5ca5-130">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b5ca5-130">-WorkspaceObject</span></span>
<span data-ttu-id="b5ca5-131">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-131">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5ca5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5ca5-132">-Confirm</span></span>
<span data-ttu-id="b5ca5-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ca5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ca5-134">-WhatIf</span></span>
<span data-ttu-id="b5ca5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ca5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ca5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ca5-137">CommonParameters</span></span>
<span data-ttu-id="b5ca5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ca5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ca5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5ca5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ca5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b5ca5-140">INPUTS</span></span>

### <span data-ttu-id="b5ca5-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b5ca5-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b5ca5-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b5ca5-142">OUTPUTS</span></span>

### <span data-ttu-id="b5ca5-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5ca5-143">System.Boolean</span></span>

## <span data-ttu-id="b5ca5-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-144">NOTES</span></span>

## <span data-ttu-id="b5ca5-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5ca5-145">RELATED LINKS</span></span>
