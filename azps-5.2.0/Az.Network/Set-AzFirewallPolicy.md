---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397735"
---
# <span data-ttu-id="a6a24-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a6a24-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="a6a24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a24-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a24-103">Сохранение измененной политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="a6a24-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="a6a24-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a6a24-104">SYNTAX</span></span>

### <span data-ttu-id="a6a24-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a6a24-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a24-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a24-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a24-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a6a24-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a24-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a6a24-108">DESCRIPTION</span></span>
<span data-ttu-id="a6a24-109">**Cmdlet Set-AzFirewallPolicy** обновляет политику брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a24-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="a6a24-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a6a24-110">EXAMPLES</span></span>

### <span data-ttu-id="a6a24-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a6a24-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="a6a24-112">В этом примере для политики брандмауэра устанавливается значение новой политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="a6a24-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="a6a24-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a6a24-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="a6a24-114">В этом примере политика брандмауэра настраиваема в новом режиме intel-угрозы</span><span class="sxs-lookup"><span data-stu-id="a6a24-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="a6a24-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a6a24-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="a6a24-116">В этом примере политика брандмауэра настраиваема с помощью нового списка intel угроз.</span><span class="sxs-lookup"><span data-stu-id="a6a24-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="a6a24-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6a24-117">PARAMETERS</span></span>

### <span data-ttu-id="a6a24-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6a24-118">-AsJob</span></span>
<span data-ttu-id="a6a24-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a6a24-119">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="a6a24-120">-BasePolicy</span></span>
<span data-ttu-id="a6a24-121">Базовая политика, наследуемая от</span><span class="sxs-lookup"><span data-stu-id="a6a24-121">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a24-122">-DefaultProfile</span></span>
<span data-ttu-id="a6a24-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a6a24-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="a6a24-124">-DnsSetting</span></span>
<span data-ttu-id="a6a24-125">Параметр DNS</span><span class="sxs-lookup"><span data-stu-id="a6a24-125">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6a24-126">-InputObject</span></span>
<span data-ttu-id="a6a24-127">Политика AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a6a24-127">The AzureFirewall Policy</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-128">-Location</span><span class="sxs-lookup"><span data-stu-id="a6a24-128">-Location</span></span>
<span data-ttu-id="a6a24-129">расположение.</span><span class="sxs-lookup"><span data-stu-id="a6a24-129">location.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-130">-Name</span><span class="sxs-lookup"><span data-stu-id="a6a24-130">-Name</span></span>
<span data-ttu-id="a6a24-131">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6a24-131">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a24-132">-ResourceGroupName</span></span>
<span data-ttu-id="a6a24-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a6a24-133">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6a24-134">-ResourceId</span></span>
<span data-ttu-id="a6a24-135">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="a6a24-135">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="a6a24-136">-Tag</span></span>
<span data-ttu-id="a6a24-137">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="a6a24-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="a6a24-138">-ThreatIntelMode</span></span>
<span data-ttu-id="a6a24-139">Режим операции для Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="a6a24-139">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="a6a24-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="a6a24-141">Белый список для Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="a6a24-141">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6a24-142">-Confirm</span></span>
<span data-ttu-id="a6a24-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a6a24-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a24-144">-WhatIf</span></span>
<span data-ttu-id="a6a24-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6a24-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a24-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a6a24-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a24-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a24-147">CommonParameters</span></span>
<span data-ttu-id="a6a24-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6a24-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a24-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a6a24-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a24-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a6a24-150">INPUTS</span></span>

### <span data-ttu-id="a6a24-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a6a24-151">System.String</span></span>

### <span data-ttu-id="a6a24-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="a6a24-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="a6a24-153">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a6a24-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a6a24-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a6a24-154">OUTPUTS</span></span>

### <span data-ttu-id="a6a24-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="a6a24-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="a6a24-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a6a24-156">NOTES</span></span>

## <span data-ttu-id="a6a24-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a6a24-157">RELATED LINKS</span></span>
