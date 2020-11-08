---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 3cffe65b1b8e4ba811ee00b7537dc95d9d6dfb72
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249618"
---
# <span data-ttu-id="f91a7-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f91a7-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="f91a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f91a7-102">SYNOPSIS</span></span>
<span data-ttu-id="f91a7-103">Сохранение измененной политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="f91a7-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="f91a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f91a7-104">SYNTAX</span></span>

### <span data-ttu-id="f91a7-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f91a7-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f91a7-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f91a7-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Location <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f91a7-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f91a7-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f91a7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f91a7-108">DESCRIPTION</span></span>
<span data-ttu-id="f91a7-109">Командлет **Set-AzFirewallPolicy** обновляет политику брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="f91a7-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="f91a7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f91a7-110">EXAMPLES</span></span>

### <span data-ttu-id="f91a7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f91a7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="f91a7-112">В этом примере для политики брандмауэра задается новое значение политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="f91a7-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="f91a7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f91a7-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="f91a7-114">В этом примере Настройка политики брандмауэра осуществляется с помощью нового режима угроз Intel</span><span class="sxs-lookup"><span data-stu-id="f91a7-114">This example sets the firewall policy with the new threat intel mode</span></span>

### <span data-ttu-id="f91a7-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f91a7-115">Example 3</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="f91a7-116">В этом примере Настройка политики брандмауэра осуществляется с помощью новой угрозы Intel Добавление</span><span class="sxs-lookup"><span data-stu-id="f91a7-116">This example sets the firewall policy with the new threat intel whitelist</span></span>

## <span data-ttu-id="f91a7-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f91a7-117">PARAMETERS</span></span>

### <span data-ttu-id="f91a7-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f91a7-118">-AsJob</span></span>
<span data-ttu-id="f91a7-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f91a7-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f91a7-120">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="f91a7-120">-BasePolicy</span></span>
<span data-ttu-id="f91a7-121">Базовая политика для наследования от</span><span class="sxs-lookup"><span data-stu-id="f91a7-121">The base policy to inherit from</span></span>

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

### <span data-ttu-id="f91a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f91a7-122">-DefaultProfile</span></span>
<span data-ttu-id="f91a7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f91a7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f91a7-124">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="f91a7-124">-DnsSetting</span></span>
<span data-ttu-id="f91a7-125">Параметр DNS</span><span class="sxs-lookup"><span data-stu-id="f91a7-125">The DNS Setting</span></span>

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

### <span data-ttu-id="f91a7-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f91a7-126">-InputObject</span></span>
<span data-ttu-id="f91a7-127">Политика AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f91a7-127">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="f91a7-128">-Location</span><span class="sxs-lookup"><span data-stu-id="f91a7-128">-Location</span></span>
<span data-ttu-id="f91a7-129">поиска.</span><span class="sxs-lookup"><span data-stu-id="f91a7-129">location.</span></span>

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

### <span data-ttu-id="f91a7-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f91a7-130">-Name</span></span>
<span data-ttu-id="f91a7-131">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="f91a7-131">The resource name.</span></span>

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

### <span data-ttu-id="f91a7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f91a7-132">-ResourceGroupName</span></span>
<span data-ttu-id="f91a7-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f91a7-133">The resource group name.</span></span>

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

### <span data-ttu-id="f91a7-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f91a7-134">-ResourceId</span></span>
<span data-ttu-id="f91a7-135">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f91a7-135">The resource Id.</span></span>

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

### <span data-ttu-id="f91a7-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="f91a7-136">-Tag</span></span>
<span data-ttu-id="f91a7-137">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f91a7-137">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f91a7-138">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="f91a7-138">-ThreatIntelMode</span></span>
<span data-ttu-id="f91a7-139">Режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="f91a7-139">The operation mode for Threat Intelligence.</span></span>

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

### <span data-ttu-id="f91a7-140">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="f91a7-140">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="f91a7-141">Добавление для логики операций с угрозами</span><span class="sxs-lookup"><span data-stu-id="f91a7-141">The whitelist for Threat Intelligence</span></span>

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

### <span data-ttu-id="f91a7-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f91a7-142">-Confirm</span></span>
<span data-ttu-id="f91a7-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f91a7-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f91a7-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f91a7-144">-WhatIf</span></span>
<span data-ttu-id="f91a7-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f91a7-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f91a7-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f91a7-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f91a7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f91a7-147">CommonParameters</span></span>
<span data-ttu-id="f91a7-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f91a7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f91a7-149">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f91a7-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f91a7-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f91a7-150">INPUTS</span></span>

### <span data-ttu-id="f91a7-151">System. String</span><span class="sxs-lookup"><span data-stu-id="f91a7-151">System.String</span></span>

### <span data-ttu-id="f91a7-152">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f91a7-152">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="f91a7-153">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f91a7-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f91a7-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f91a7-154">OUTPUTS</span></span>

### <span data-ttu-id="f91a7-155">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="f91a7-155">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="f91a7-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="f91a7-156">NOTES</span></span>

## <span data-ttu-id="f91a7-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f91a7-157">RELATED LINKS</span></span>
