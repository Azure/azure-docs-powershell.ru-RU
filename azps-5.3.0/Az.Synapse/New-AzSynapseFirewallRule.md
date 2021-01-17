---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424284"
---
# <span data-ttu-id="8b41b-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b41b-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="8b41b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b41b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b41b-103">Создает правило брандмауэра synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="8b41b-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8b41b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b41b-104">SYNTAX</span></span>

### <span data-ttu-id="8b41b-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b41b-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b41b-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b41b-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b41b-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b41b-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b41b-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b41b-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b41b-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b41b-109">DESCRIPTION</span></span>
<span data-ttu-id="8b41b-110">Для создания правила брандмауэра Azure Synapse Analytics создается правило брандмауэра **New-AzSynapseFirewallRule.**</span><span class="sxs-lookup"><span data-stu-id="8b41b-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="8b41b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b41b-111">EXAMPLES</span></span>

### <span data-ttu-id="8b41b-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b41b-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="8b41b-113">Эта команда создает правило брандмауэра ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="8b41b-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="8b41b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b41b-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="8b41b-115">Эта команда создает правило брандмауэра ContosoFirewallRule в рабочей области через канал.</span><span class="sxs-lookup"><span data-stu-id="8b41b-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="8b41b-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8b41b-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="8b41b-117">Эта команда создает правило брандмауэра, разреша которое разрешает все ip-адреса Azure в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8b41b-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="8b41b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b41b-118">PARAMETERS</span></span>

### <span data-ttu-id="8b41b-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="8b41b-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="8b41b-120">Создает специальное правило брандмауэра, которое позволяет всем IP-данным Azure получать доступ.</span><span class="sxs-lookup"><span data-stu-id="8b41b-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="8b41b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b41b-121">-AsJob</span></span>
<span data-ttu-id="8b41b-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b41b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b41b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b41b-123">-DefaultProfile</span></span>
<span data-ttu-id="8b41b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b41b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b41b-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b41b-125">-EndIpAddress</span></span>
<span data-ttu-id="8b41b-126">Конечный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8b41b-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="8b41b-127">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="8b41b-127">Must be IPv4 format.</span></span>
<span data-ttu-id="8b41b-128">Должен быть больше или равен startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="8b41b-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="8b41b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="8b41b-129">-Name</span></span>
<span data-ttu-id="8b41b-130">Имя правила брандмауэра для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8b41b-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="8b41b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b41b-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b41b-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b41b-132">Resource group name.</span></span>

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

### <span data-ttu-id="8b41b-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="8b41b-133">-StartIpAddress</span></span>
<span data-ttu-id="8b41b-134">Начальный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8b41b-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="8b41b-135">Должен быть форматом IPv4.</span><span class="sxs-lookup"><span data-stu-id="8b41b-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="8b41b-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8b41b-136">-WorkspaceName</span></span>
<span data-ttu-id="8b41b-137">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="8b41b-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="8b41b-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8b41b-138">-WorkspaceObject</span></span>
<span data-ttu-id="8b41b-139">объект ввода рабочей области, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="8b41b-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="8b41b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b41b-140">-Confirm</span></span>
<span data-ttu-id="8b41b-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b41b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b41b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b41b-142">-WhatIf</span></span>
<span data-ttu-id="8b41b-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b41b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b41b-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b41b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b41b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b41b-145">CommonParameters</span></span>
<span data-ttu-id="8b41b-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b41b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b41b-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b41b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b41b-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b41b-148">INPUTS</span></span>

### <span data-ttu-id="8b41b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8b41b-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="8b41b-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b41b-150">OUTPUTS</span></span>

### <span data-ttu-id="8b41b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b41b-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="8b41b-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b41b-152">NOTES</span></span>

## <span data-ttu-id="8b41b-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b41b-153">RELATED LINKS</span></span>
