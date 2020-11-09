---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 17aea8ab38582373420107df87e2b6837a83a1a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317141"
---
# <span data-ttu-id="24058-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="24058-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="24058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24058-102">SYNOPSIS</span></span>
<span data-ttu-id="24058-103">Создание новой политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="24058-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="24058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24058-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24058-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24058-105">DESCRIPTION</span></span>
<span data-ttu-id="24058-106">Командлет **New-AzFirewallPolicy** создает политику брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="24058-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="24058-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24058-107">EXAMPLES</span></span>

### <span data-ttu-id="24058-108">Пример 1:1.</span><span class="sxs-lookup"><span data-stu-id="24058-108">Example 1: 1.</span></span> <span data-ttu-id="24058-109">Создание пустой политики</span><span class="sxs-lookup"><span data-stu-id="24058-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="24058-110">В этом примере создается политика брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="24058-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="24058-111">Пример 2:2.</span><span class="sxs-lookup"><span data-stu-id="24058-111">Example 2: 2.</span></span> <span data-ttu-id="24058-112">Создание пустой политики с помощью режима ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="24058-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="24058-113">В этом примере создается политика брандмауэра Azure с режимом угроз Intel</span><span class="sxs-lookup"><span data-stu-id="24058-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="24058-114">Пример 3:3.</span><span class="sxs-lookup"><span data-stu-id="24058-114">Example 3: 3.</span></span> <span data-ttu-id="24058-115">Создание пустой политики с помощью ThreatIntel Добавление</span><span class="sxs-lookup"><span data-stu-id="24058-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="24058-116">В этом примере создается политика брандмауэра Azure с угрозой Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="24058-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

## <span data-ttu-id="24058-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24058-117">PARAMETERS</span></span>

### <span data-ttu-id="24058-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24058-118">-AsJob</span></span>
<span data-ttu-id="24058-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="24058-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24058-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="24058-120">-BasePolicy</span></span>
<span data-ttu-id="24058-121">Базовая политика для наследования от</span><span class="sxs-lookup"><span data-stu-id="24058-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="24058-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24058-122">-DefaultProfile</span></span>
<span data-ttu-id="24058-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="24058-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24058-124">-Force</span><span class="sxs-lookup"><span data-stu-id="24058-124">-Force</span></span>
<span data-ttu-id="24058-125">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="24058-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="24058-126">-Location</span><span class="sxs-lookup"><span data-stu-id="24058-126">-Location</span></span>
<span data-ttu-id="24058-127">поиска.</span><span class="sxs-lookup"><span data-stu-id="24058-127">location.</span></span>

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

### <span data-ttu-id="24058-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="24058-128">-Name</span></span>
<span data-ttu-id="24058-129">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="24058-129">The resource name.</span></span>

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

### <span data-ttu-id="24058-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24058-130">-ResourceGroupName</span></span>
<span data-ttu-id="24058-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24058-131">The resource group name.</span></span>

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

### <span data-ttu-id="24058-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="24058-132">-Tag</span></span>
<span data-ttu-id="24058-133">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24058-133">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="24058-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="24058-134">-ThreatIntelMode</span></span>
<span data-ttu-id="24058-135">Режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="24058-135">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="24058-136">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="24058-136">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="24058-137">Добавление для логики операций с угрозами</span><span class="sxs-lookup"><span data-stu-id="24058-137">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="24058-138">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="24058-138">-DnsSetting</span></span>
<span data-ttu-id="24058-139">Параметр DNS</span><span class="sxs-lookup"><span data-stu-id="24058-139">The DNS Setting</span></span>

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

### <span data-ttu-id="24058-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="24058-140">-Confirm</span></span>
<span data-ttu-id="24058-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="24058-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24058-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24058-142">-WhatIf</span></span>
<span data-ttu-id="24058-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="24058-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24058-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="24058-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24058-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24058-145">CommonParameters</span></span>
<span data-ttu-id="24058-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24058-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24058-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24058-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24058-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24058-148">INPUTS</span></span>

### <span data-ttu-id="24058-149">System. String</span><span class="sxs-lookup"><span data-stu-id="24058-149">System.String</span></span>

### <span data-ttu-id="24058-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="24058-150">System.Collections.Hashtable</span></span>

## <span data-ttu-id="24058-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24058-151">OUTPUTS</span></span>

### <span data-ttu-id="24058-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="24058-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="24058-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="24058-153">NOTES</span></span>

## <span data-ttu-id="24058-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24058-154">RELATED LINKS</span></span>
