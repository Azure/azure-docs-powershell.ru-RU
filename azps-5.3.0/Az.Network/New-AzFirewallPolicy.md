---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506929"
---
# <span data-ttu-id="f8ac5-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f8ac5-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="f8ac5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="f8ac5-103">Создание политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="f8ac5-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="f8ac5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8ac5-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8ac5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8ac5-105">DESCRIPTION</span></span>
<span data-ttu-id="f8ac5-106">С **помощью cmdlet New-AzFirewallPolicy** создается политика брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f8ac5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8ac5-107">EXAMPLES</span></span>

### <span data-ttu-id="f8ac5-108">Пример 1: 1.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-108">Example 1: 1.</span></span> <span data-ttu-id="f8ac5-109">Создание пустой политики</span><span class="sxs-lookup"><span data-stu-id="f8ac5-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="f8ac5-110">В этом примере создается политика брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="f8ac5-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="f8ac5-111">Пример 2: 2.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-111">Example 2: 2.</span></span> <span data-ttu-id="f8ac5-112">Создание пустой политики в режиме ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="f8ac5-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="f8ac5-113">В этом примере создается политика брандмауэра Azure с режимом intel-угрозы</span><span class="sxs-lookup"><span data-stu-id="f8ac5-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="f8ac5-114">Пример 3: 3.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-114">Example 3: 3.</span></span> <span data-ttu-id="f8ac5-115">Создание пустой политики с белым списком ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="f8ac5-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="f8ac5-116">В этом примере создается политика брандмауэра Azure с белым списком угроз Intel</span><span class="sxs-lookup"><span data-stu-id="f8ac5-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="f8ac5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8ac5-117">PARAMETERS</span></span>

### <span data-ttu-id="f8ac5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f8ac5-118">-AsJob</span></span>
<span data-ttu-id="f8ac5-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f8ac5-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f8ac5-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="f8ac5-120">-BasePolicy</span></span>
<span data-ttu-id="f8ac5-121">Базовая политика, наследуемая от</span><span class="sxs-lookup"><span data-stu-id="f8ac5-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="f8ac5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8ac5-122">-DefaultProfile</span></span>
<span data-ttu-id="f8ac5-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8ac5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f8ac5-124">-Force</span></span>
<span data-ttu-id="f8ac5-125">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="f8ac5-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f8ac5-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f8ac5-126">-Location</span></span>
<span data-ttu-id="f8ac5-127">расположение.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-127">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ac5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f8ac5-128">-Name</span></span>
<span data-ttu-id="f8ac5-129">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ac5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8ac5-130">-ResourceGroupName</span></span>
<span data-ttu-id="f8ac5-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8ac5-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="f8ac5-132">-Tag</span></span>
<span data-ttu-id="f8ac5-133">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f8ac5-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f8ac5-134">-ThreatIntelMode</span></span>
<span data-ttu-id="f8ac5-135">Режим операции для Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="f8ac5-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f8ac5-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="f8ac5-137">Белый список для Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="f8ac5-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="f8ac5-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f8ac5-138">-DnsSetting</span></span>
<span data-ttu-id="f8ac5-139">Параметр DNS</span><span class="sxs-lookup"><span data-stu-id="f8ac5-139">The DNS Setting</span></span>

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

### <span data-ttu-id="f8ac5-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8ac5-140">-Confirm</span></span>
<span data-ttu-id="f8ac5-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8ac5-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8ac5-142">-WhatIf</span></span>
<span data-ttu-id="f8ac5-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8ac5-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8ac5-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8ac5-145">CommonParameters</span></span>
<span data-ttu-id="f8ac5-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8ac5-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8ac5-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8ac5-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8ac5-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8ac5-148">INPUTS</span></span>

### <span data-ttu-id="f8ac5-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f8ac5-149">System.String</span></span>

### <span data-ttu-id="f8ac5-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f8ac5-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f8ac5-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8ac5-151">OUTPUTS</span></span>

### <span data-ttu-id="f8ac5-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f8ac5-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f8ac5-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8ac5-153">NOTES</span></span>

## <span data-ttu-id="f8ac5-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8ac5-154">RELATED LINKS</span></span>
