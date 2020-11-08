---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077458"
---
# <span data-ttu-id="98acb-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98acb-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="98acb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98acb-102">SYNOPSIS</span></span>
<span data-ttu-id="98acb-103">Обновляет правило брандмауэра Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="98acb-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="98acb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98acb-104">SYNTAX</span></span>

### <span data-ttu-id="98acb-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98acb-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98acb-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98acb-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98acb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98acb-107">DESCRIPTION</span></span>
<span data-ttu-id="98acb-108">Командлет **Update-AzSynapseFirewallRule** изменяет правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="98acb-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="98acb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98acb-109">EXAMPLES</span></span>

### <span data-ttu-id="98acb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98acb-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="98acb-111">Эта команда обновляет правило брандмауэра с именем ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="98acb-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="98acb-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="98acb-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="98acb-113">Эта команда обновляет правило брандмауэра с именем ContosoFirewallRule в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="98acb-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="98acb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98acb-114">PARAMETERS</span></span>

### <span data-ttu-id="98acb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98acb-115">-AsJob</span></span>
<span data-ttu-id="98acb-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="98acb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98acb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98acb-117">-DefaultProfile</span></span>
<span data-ttu-id="98acb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98acb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98acb-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="98acb-119">-EndIpAddress</span></span>
<span data-ttu-id="98acb-120">Конечный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="98acb-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="98acb-121">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="98acb-121">Must be IPv4 format.</span></span>
<span data-ttu-id="98acb-122">Оно должно быть больше или равно startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="98acb-122">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98acb-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98acb-123">-Name</span></span>
<span data-ttu-id="98acb-124">Имя правила firerwall для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="98acb-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="98acb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98acb-125">-ResourceGroupName</span></span>
<span data-ttu-id="98acb-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="98acb-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98acb-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="98acb-127">-StartIpAddress</span></span>
<span data-ttu-id="98acb-128">Начальный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="98acb-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="98acb-129">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="98acb-129">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98acb-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98acb-130">-WorkspaceName</span></span>
<span data-ttu-id="98acb-131">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="98acb-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98acb-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="98acb-132">-WorkspaceObject</span></span>
<span data-ttu-id="98acb-133">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="98acb-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98acb-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98acb-134">-Confirm</span></span>
<span data-ttu-id="98acb-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="98acb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98acb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98acb-136">-WhatIf</span></span>
<span data-ttu-id="98acb-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="98acb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98acb-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="98acb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98acb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98acb-139">CommonParameters</span></span>
<span data-ttu-id="98acb-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98acb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98acb-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98acb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98acb-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98acb-142">INPUTS</span></span>

### <span data-ttu-id="98acb-143">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="98acb-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="98acb-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98acb-144">OUTPUTS</span></span>

### <span data-ttu-id="98acb-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="98acb-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="98acb-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="98acb-146">NOTES</span></span>

## <span data-ttu-id="98acb-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98acb-147">RELATED LINKS</span></span>