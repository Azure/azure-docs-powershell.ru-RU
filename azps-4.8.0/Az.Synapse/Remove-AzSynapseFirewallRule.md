---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseFirewallRule.md
ms.openlocfilehash: 6094c8d7e75136c9a9abf220ccfcb8775bda5dd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079914"
---
# <span data-ttu-id="ce40f-101">Remove-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ce40f-101">Remove-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="ce40f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce40f-102">SYNOPSIS</span></span>
<span data-ttu-id="ce40f-103">Удаляет правило брандмауэра Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce40f-103">Deletes a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ce40f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce40f-104">SYNTAX</span></span>

### <span data-ttu-id="ce40f-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce40f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce40f-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce40f-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseFirewallRule -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce40f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce40f-107">DESCRIPTION</span></span>
<span data-ttu-id="ce40f-108">Командлет **Remove-AzSynapseFirewallRule** окончательно удаляет правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ce40f-108">The **Remove-AzSynapseFirewallRule** cmdlet permanently deletes an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="ce40f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce40f-109">EXAMPLES</span></span>

### <span data-ttu-id="ce40f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ce40f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule
```

<span data-ttu-id="ce40f-111">Эта команда удаляет правило брандмауэра с именем ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="ce40f-111">This command deletes firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="ce40f-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ce40f-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseFirewallRule -Name ContosoFirewallRule
```

<span data-ttu-id="ce40f-113">Эта команда удаляет правило брандмауэра с именем ContosoFirewallRule в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="ce40f-113">This command deletes firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="ce40f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce40f-114">PARAMETERS</span></span>

### <span data-ttu-id="ce40f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce40f-115">-AsJob</span></span>
<span data-ttu-id="ce40f-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ce40f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce40f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce40f-117">-DefaultProfile</span></span>
<span data-ttu-id="ce40f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce40f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce40f-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce40f-119">-Name</span></span>
<span data-ttu-id="ce40f-120">Имя правила firerwall для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ce40f-120">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="ce40f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce40f-121">-PassThru</span></span>
<span data-ttu-id="ce40f-122">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ce40f-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ce40f-123">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="ce40f-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ce40f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce40f-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce40f-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ce40f-125">Resource group name.</span></span>

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

### <span data-ttu-id="ce40f-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce40f-126">-WorkspaceName</span></span>
<span data-ttu-id="ce40f-127">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ce40f-127">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ce40f-128">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ce40f-128">-WorkspaceObject</span></span>
<span data-ttu-id="ce40f-129">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="ce40f-129">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="ce40f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce40f-130">-Confirm</span></span>
<span data-ttu-id="ce40f-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce40f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce40f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce40f-132">-WhatIf</span></span>
<span data-ttu-id="ce40f-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce40f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce40f-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce40f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce40f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce40f-135">CommonParameters</span></span>
<span data-ttu-id="ce40f-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce40f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce40f-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce40f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce40f-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce40f-138">INPUTS</span></span>

### <span data-ttu-id="ce40f-139">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ce40f-139">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ce40f-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce40f-140">OUTPUTS</span></span>

### <span data-ttu-id="ce40f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ce40f-141">System.Boolean</span></span>

## <span data-ttu-id="ce40f-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce40f-142">NOTES</span></span>

## <span data-ttu-id="ce40f-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce40f-143">RELATED LINKS</span></span>
