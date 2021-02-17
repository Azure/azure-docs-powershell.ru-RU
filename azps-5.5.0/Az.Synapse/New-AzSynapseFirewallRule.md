---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231409"
---
# <span data-ttu-id="257f4-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="257f4-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="257f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="257f4-102">SYNOPSIS</span></span>
<span data-ttu-id="257f4-103">Создает правило брандмауэра synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="257f4-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="257f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="257f4-104">SYNTAX</span></span>

### <span data-ttu-id="257f4-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="257f4-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257f4-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="257f4-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="257f4-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="257f4-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="257f4-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="257f4-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="257f4-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="257f4-109">DESCRIPTION</span></span>
<span data-ttu-id="257f4-110">Для создания правила брандмауэра Azure Synapse Analytics создается правило брандмауэра **New-AzSynapseFirewallRule.**</span><span class="sxs-lookup"><span data-stu-id="257f4-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="257f4-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="257f4-111">EXAMPLES</span></span>

### <span data-ttu-id="257f4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="257f4-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="257f4-113">Эта команда создает правило брандмауэра ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="257f4-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="257f4-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="257f4-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="257f4-115">Эта команда создает правило брандмауэра ContosoFirewallRule в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="257f4-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="257f4-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="257f4-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="257f4-117">Эта команда создает правило брандмауэра, разреша которое разрешает все ip-адреса Azure в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="257f4-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="257f4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="257f4-118">PARAMETERS</span></span>

### <span data-ttu-id="257f4-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="257f4-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="257f4-120">Создает специальное правило брандмауэра, которое позволяет всем IP-данным Azure получать доступ.</span><span class="sxs-lookup"><span data-stu-id="257f4-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateByNameAllowAllIpParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="257f4-121">-AsJob</span></span>
<span data-ttu-id="257f4-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="257f4-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="257f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="257f4-123">-DefaultProfile</span></span>
<span data-ttu-id="257f4-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="257f4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="257f4-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="257f4-125">-EndIpAddress</span></span>
<span data-ttu-id="257f4-126">Конечный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="257f4-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="257f4-127">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="257f4-127">Must be IPv4 format.</span></span>
<span data-ttu-id="257f4-128">Должен быть больше или равен startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="257f4-128">Must be greater than or equal to startIpAddress.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-129">-Name</span><span class="sxs-lookup"><span data-stu-id="257f4-129">-Name</span></span>
<span data-ttu-id="257f4-130">Имя правила брандмауэра для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="257f4-130">The firerwall rule name for the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="257f4-131">-ResourceGroupName</span></span>
<span data-ttu-id="257f4-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="257f4-132">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="257f4-133">-StartIpAddress</span></span>
<span data-ttu-id="257f4-134">Начальный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="257f4-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="257f4-135">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="257f4-135">Must be IPv4 format.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="257f4-136">-WorkspaceName</span></span>
<span data-ttu-id="257f4-137">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="257f4-137">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByNameAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="257f4-138">-WorkspaceObject</span></span>
<span data-ttu-id="257f4-139">объект ввода рабочей области, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="257f4-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateByParentObjectParameterSet, CreateByParentObjectAllowAllIpParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="257f4-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="257f4-140">-Confirm</span></span>
<span data-ttu-id="257f4-141">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="257f4-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="257f4-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="257f4-142">-WhatIf</span></span>
<span data-ttu-id="257f4-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="257f4-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="257f4-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="257f4-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="257f4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="257f4-145">CommonParameters</span></span>
<span data-ttu-id="257f4-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="257f4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="257f4-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="257f4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="257f4-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="257f4-148">INPUTS</span></span>

### <span data-ttu-id="257f4-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="257f4-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="257f4-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="257f4-150">OUTPUTS</span></span>

### <span data-ttu-id="257f4-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="257f4-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="257f4-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="257f4-152">NOTES</span></span>

## <span data-ttu-id="257f4-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="257f4-153">RELATED LINKS</span></span>
