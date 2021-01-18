---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseFirewallRule.md
ms.openlocfilehash: 9188a1cc8dde39db4d755fb2059f3633fc85ead8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516953"
---
# <span data-ttu-id="d7e1e-101">Update-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d7e1e-101">Update-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="d7e1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7e1e-102">SYNOPSIS</span></span>
<span data-ttu-id="d7e1e-103">Обновляет правило брандмауэра synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-103">Updates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="d7e1e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7e1e-104">SYNTAX</span></span>

### <span data-ttu-id="d7e1e-105">UpdateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7e1e-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-StartIpAddress <String>] [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7e1e-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d7e1e-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-StartIpAddress <String>]
 [-EndIpAddress <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7e1e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7e1e-107">DESCRIPTION</span></span>
<span data-ttu-id="d7e1e-108">Для **брандмауэра Update-AzSynapseFirewallRule** обновляется правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-108">The **Update-AzSynapseFirewallRule** cmdlet modifys an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="d7e1e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7e1e-109">EXAMPLES</span></span>

### <span data-ttu-id="d7e1e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d7e1e-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseFirewallRule -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="d7e1e-111">Эта команда обновляет правило брандмауэра ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-111">This command updates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="d7e1e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d7e1e-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAssdress "255.255.255.255"
```

<span data-ttu-id="d7e1e-113">Эта команда обновляет правило брандмауэра ContosoFirewallRule в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-113">This command updates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

## <span data-ttu-id="d7e1e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7e1e-114">PARAMETERS</span></span>

### <span data-ttu-id="d7e1e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7e1e-115">-AsJob</span></span>
<span data-ttu-id="d7e1e-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d7e1e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d7e1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7e1e-117">-DefaultProfile</span></span>
<span data-ttu-id="d7e1e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7e1e-119">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="d7e1e-119">-EndIpAddress</span></span>
<span data-ttu-id="d7e1e-120">Конечный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-120">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="d7e1e-121">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-121">Must be IPv4 format.</span></span>
<span data-ttu-id="d7e1e-122">Должен быть больше или равен startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-122">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="d7e1e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d7e1e-123">-Name</span></span>
<span data-ttu-id="d7e1e-124">Имя правила брандмауэра для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-124">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="d7e1e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7e1e-125">-ResourceGroupName</span></span>
<span data-ttu-id="d7e1e-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-126">Resource group name.</span></span>

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

### <span data-ttu-id="d7e1e-127">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="d7e1e-127">-StartIpAddress</span></span>
<span data-ttu-id="d7e1e-128">Начальный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-128">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="d7e1e-129">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-129">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="d7e1e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d7e1e-130">-WorkspaceName</span></span>
<span data-ttu-id="d7e1e-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="d7e1e-132">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d7e1e-132">-WorkspaceObject</span></span>
<span data-ttu-id="d7e1e-133">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="d7e1e-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7e1e-134">-Confirm</span></span>
<span data-ttu-id="d7e1e-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7e1e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7e1e-136">-WhatIf</span></span>
<span data-ttu-id="d7e1e-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7e1e-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7e1e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7e1e-139">CommonParameters</span></span>
<span data-ttu-id="d7e1e-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7e1e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7e1e-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7e1e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7e1e-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7e1e-142">INPUTS</span></span>

### <span data-ttu-id="d7e1e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d7e1e-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d7e1e-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7e1e-144">OUTPUTS</span></span>

### <span data-ttu-id="d7e1e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d7e1e-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="d7e1e-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7e1e-146">NOTES</span></span>

## <span data-ttu-id="d7e1e-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7e1e-147">RELATED LINKS</span></span>
