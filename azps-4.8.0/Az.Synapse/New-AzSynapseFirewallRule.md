---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseFirewallRule.md
ms.openlocfilehash: b4579d01ed6dd5a7d742cbb82afb424151579772
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077469"
---
# <span data-ttu-id="88507-101">New-AzSynapseFirewallRule</span><span class="sxs-lookup"><span data-stu-id="88507-101">New-AzSynapseFirewallRule</span></span>

## <span data-ttu-id="88507-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88507-102">SYNOPSIS</span></span>
<span data-ttu-id="88507-103">Создает правило брандмауэра Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="88507-103">Creates a Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="88507-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88507-104">SYNTAX</span></span>

### <span data-ttu-id="88507-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88507-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -StartIpAddress <String> -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88507-106">CreateByNameAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="88507-106">CreateByNameAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule [-ResourceGroupName <String>] -WorkspaceName <String> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88507-107">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88507-107">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> -Name <String> -StartIpAddress <String>
 -EndIpAddress <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88507-108">CreateByParentObjectAllowAllIpParameterSet</span><span class="sxs-lookup"><span data-stu-id="88507-108">CreateByParentObjectAllowAllIpParameterSet</span></span>
```
New-AzSynapseFirewallRule -WorkspaceObject <PSSynapseWorkspace> [-AllowAllAzureIP] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88507-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88507-109">DESCRIPTION</span></span>
<span data-ttu-id="88507-110">Командлет **New-AzSynapseFirewallRule** создает правило брандмауэра Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="88507-110">The **New-AzSynapseFirewallRule** cmdlet creates an Azure Synapse Analytics Firewall Rule.</span></span>

## <span data-ttu-id="88507-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88507-111">EXAMPLES</span></span>

### <span data-ttu-id="88507-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="88507-112">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="88507-113">Эта команда создает правило межсетевого экрана с именем ContosoFirewallRule в рабочей области ContosoWorkspace с именем ContosoFirewallRule.</span><span class="sxs-lookup"><span data-stu-id="88507-113">This command creates firewall rule named ContosoFirewallRule under workspace ContosoWorkspace with name ContosoFirewallRule.</span></span>

### <span data-ttu-id="88507-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="88507-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseFirewallRule -Name ContosoFirewallRule -StartIpAddress "0.0.0.0" -EndIpAddress "255.255.255.255"
```

<span data-ttu-id="88507-115">Эта команда создает правило межсетевого экрана с именем ContosoFirewallRule в рабочей области с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="88507-115">This command creates firewall rule named ContosoFirewallRule under a workspace through pipeline.</span></span>

### <span data-ttu-id="88507-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="88507-116">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseFirewallRule -WorkspaceName ContosoWorkspace -AllowAllAzureIP
```

<span data-ttu-id="88507-117">Эта команда создает правило межсетевого экрана, разрешающее все IP-адреса Azure в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="88507-117">This command creates firewall rule that allow all azure ips under a workspace.</span></span>

## <span data-ttu-id="88507-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88507-118">PARAMETERS</span></span>

### <span data-ttu-id="88507-119">-AllowAllAzureIP</span><span class="sxs-lookup"><span data-stu-id="88507-119">-AllowAllAzureIP</span></span>
<span data-ttu-id="88507-120">Создание специального правила брандмауэра, позволяющего получить доступ ко всем IP-адресам Azure.</span><span class="sxs-lookup"><span data-stu-id="88507-120">Creates a special firewall rule that permits all Azure IPs to have access.</span></span>

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

### <span data-ttu-id="88507-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88507-121">-AsJob</span></span>
<span data-ttu-id="88507-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="88507-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88507-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88507-123">-DefaultProfile</span></span>
<span data-ttu-id="88507-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88507-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88507-125">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="88507-125">-EndIpAddress</span></span>
<span data-ttu-id="88507-126">Конечный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="88507-126">The end IP address of the firewall rule.</span></span>
<span data-ttu-id="88507-127">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="88507-127">Must be IPv4 format.</span></span>
<span data-ttu-id="88507-128">Оно должно быть больше или равно startIpAddress.</span><span class="sxs-lookup"><span data-stu-id="88507-128">Must be greater than or equal to startIpAddress.</span></span>

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

### <span data-ttu-id="88507-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88507-129">-Name</span></span>
<span data-ttu-id="88507-130">Имя правила firerwall для рабочей области.</span><span class="sxs-lookup"><span data-stu-id="88507-130">The firerwall rule name for the workspace.</span></span>

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

### <span data-ttu-id="88507-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88507-131">-ResourceGroupName</span></span>
<span data-ttu-id="88507-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="88507-132">Resource group name.</span></span>

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

### <span data-ttu-id="88507-133">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="88507-133">-StartIpAddress</span></span>
<span data-ttu-id="88507-134">Начальный IP-адрес правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="88507-134">The start IP address of the firewall rule.</span></span>
<span data-ttu-id="88507-135">Требуется формат IPv4.</span><span class="sxs-lookup"><span data-stu-id="88507-135">Must be IPv4 format.</span></span>

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

### <span data-ttu-id="88507-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88507-136">-WorkspaceName</span></span>
<span data-ttu-id="88507-137">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="88507-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="88507-138">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88507-138">-WorkspaceObject</span></span>
<span data-ttu-id="88507-139">объект ввода в рабочую область, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="88507-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="88507-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88507-140">-Confirm</span></span>
<span data-ttu-id="88507-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88507-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88507-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88507-142">-WhatIf</span></span>
<span data-ttu-id="88507-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88507-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88507-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88507-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88507-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88507-145">CommonParameters</span></span>
<span data-ttu-id="88507-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88507-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88507-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88507-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88507-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88507-148">INPUTS</span></span>

### <span data-ttu-id="88507-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="88507-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="88507-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88507-150">OUTPUTS</span></span>

### <span data-ttu-id="88507-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseIpFirewallRule</span><span class="sxs-lookup"><span data-stu-id="88507-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseIpFirewallRule</span></span>

## <span data-ttu-id="88507-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="88507-152">NOTES</span></span>

## <span data-ttu-id="88507-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88507-153">RELATED LINKS</span></span>