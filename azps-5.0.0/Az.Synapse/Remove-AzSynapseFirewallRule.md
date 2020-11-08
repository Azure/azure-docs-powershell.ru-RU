---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246603"
---
# <span data-ttu-id="b9575-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b9575-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="b9575-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9575-102">SYNOPSIS</span></span>
<span data-ttu-id="b9575-103">Удаляет правило брандмауэра Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b9575-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b9575-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9575-104">SYNTAX</span></span>

### <span data-ttu-id="b9575-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9575-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9575-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9575-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9575-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9575-107">DESCRIPTION</span></span>
<span data-ttu-id="b9575-108">Командлет **Remove-AzSynapseFirewallRule** окончательно удаляет правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="b9575-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="b9575-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9575-109">EXAMPLES</span></span>

### <span data-ttu-id="b9575-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9575-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="b9575-111">Эта команда удаляет правило брандмауэра с именем ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="b9575-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="b9575-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b9575-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="b9575-113">Эта команда удаляет правило брандмауэра с именем ContosoFirewallRule в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="b9575-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="b9575-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9575-114">PARAMETERS</span></span>

### <span data-ttu-id="b9575-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9575-115">-AsJob</span></span>
<span data-ttu-id="b9575-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b9575-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b9575-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9575-117">-DefaultProfile</span></span>
<span data-ttu-id="b9575-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9575-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9575-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b9575-119">-Name</span></span>
<span data-ttu-id="b9575-120">Имя правила firerwall для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b9575-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="b9575-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9575-121">-PassThru</span></span>
<span data-ttu-id="b9575-122">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b9575-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b9575-123">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="b9575-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="b9575-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9575-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9575-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b9575-125">Resource group name.</span></span>

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

### <span data-ttu-id="b9575-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b9575-126">-WorkspaceName</span></span>
<span data-ttu-id="b9575-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="b9575-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="b9575-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b9575-128">-WorkspaceObject</span></span>
<span data-ttu-id="b9575-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="b9575-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="b9575-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9575-130">-Confirm</span></span>
<span data-ttu-id="b9575-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9575-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9575-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9575-132">-WhatIf</span></span>
<span data-ttu-id="b9575-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9575-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9575-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9575-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9575-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9575-135">CommonParameters</span></span>
<span data-ttu-id="b9575-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9575-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9575-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9575-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9575-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9575-138">INPUTS</span></span>

### <span data-ttu-id="b9575-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="b9575-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="b9575-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9575-140">OUTPUTS</span></span>

### <span data-ttu-id="b9575-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9575-141">System.Boolean</span></span>

## <span data-ttu-id="b9575-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9575-142">NOTES</span></span>

## <span data-ttu-id="b9575-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9575-143">RELATED LINKS</span></span>
