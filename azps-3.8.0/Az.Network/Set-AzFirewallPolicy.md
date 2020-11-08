---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewallPolicy.md
ms.openlocfilehash: 1e5fbeba85431ab593d4daedff0f8b71af13ace4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066980"
---
# <span data-ttu-id="3d18d-101">Set-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3d18d-101">Set-AzFirewallPolicy</span></span>

## <span data-ttu-id="3d18d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d18d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d18d-103">Сохранение измененной политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="3d18d-103">Saves a modified azure firewall policy</span></span>

## <span data-ttu-id="3d18d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d18d-104">SYNTAX</span></span>

### <span data-ttu-id="3d18d-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3d18d-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d18d-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d18d-106">SetByInputObjectParameterSet</span></span>
```
Set-AzFirewallPolicy [-Name <String>] -InputObject <PSAzureFirewallPolicy> [-AsJob] [-ThreatIntelMode <String>]
 [-BasePolicy <String>] [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d18d-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d18d-107">SetByResourceIdParameterSet</span></span>
```
Set-AzFirewallPolicy [-AsJob] -ResourceId <String> [-ThreatIntelMode <String>] [-BasePolicy <String>]
 -Location <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d18d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d18d-108">DESCRIPTION</span></span>
<span data-ttu-id="3d18d-109">Командлет **Set-AzFirewallPolicy** обновляет политику брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="3d18d-109">The **Set-AzFirewallPolicy** cmdlet updates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="3d18d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d18d-110">EXAMPLES</span></span>

### <span data-ttu-id="3d18d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d18d-111">Example 1</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="3d18d-112">В этом примере для политики брандмауэра задается новое значение политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="3d18d-112">This example sets the firewall policy with the new firewall policy value</span></span>

### <span data-ttu-id="3d18d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3d18d-113">Example 2</span></span>
```powershell
PS C:\> Set-AzFirewallPolicy -Name firewallPolicy1 -ResourceGroupName TestRg -Location westcentralus -ThreatIntelMode "Alert"
```

<span data-ttu-id="3d18d-114">В этом примере Настройка политики брандмауэра осуществляется с помощью нового режима угроз Intel</span><span class="sxs-lookup"><span data-stu-id="3d18d-114">This example sets the firewall policy with the new threat intel mode</span></span>

## <span data-ttu-id="3d18d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d18d-115">PARAMETERS</span></span>

### <span data-ttu-id="3d18d-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d18d-116">-AsJob</span></span>
<span data-ttu-id="3d18d-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3d18d-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d18d-118">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="3d18d-118">-BasePolicy</span></span>
<span data-ttu-id="3d18d-119">Базовая политика для наследования от</span><span class="sxs-lookup"><span data-stu-id="3d18d-119">The base policy to inherit from</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d18d-120">-DefaultProfile</span></span>
<span data-ttu-id="3d18d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d18d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d18d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d18d-122">-InputObject</span></span>
<span data-ttu-id="3d18d-123">Политика AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3d18d-123">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-124">-Location</span><span class="sxs-lookup"><span data-stu-id="3d18d-124">-Location</span></span>
<span data-ttu-id="3d18d-125">поиска.</span><span class="sxs-lookup"><span data-stu-id="3d18d-125">location.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d18d-126">-Name</span></span>
<span data-ttu-id="3d18d-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d18d-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d18d-128">-ResourceGroupName</span></span>
<span data-ttu-id="3d18d-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d18d-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3d18d-130">-ResourceId</span></span>
<span data-ttu-id="3d18d-131">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="3d18d-131">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-132">-Тег</span><span class="sxs-lookup"><span data-stu-id="3d18d-132">-Tag</span></span>
<span data-ttu-id="3d18d-133">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3d18d-133">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-134">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="3d18d-134">-ThreatIntelMode</span></span>
<span data-ttu-id="3d18d-135">Режим работы для логики операций с угрозами.</span><span class="sxs-lookup"><span data-stu-id="3d18d-135">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d18d-136">-Confirm</span></span>
<span data-ttu-id="3d18d-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d18d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d18d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d18d-138">-WhatIf</span></span>
<span data-ttu-id="3d18d-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d18d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d18d-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d18d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d18d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d18d-141">CommonParameters</span></span>
<span data-ttu-id="3d18d-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d18d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d18d-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3d18d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d18d-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d18d-144">INPUTS</span></span>

### <span data-ttu-id="3d18d-145">System. String</span><span class="sxs-lookup"><span data-stu-id="3d18d-145">System.String</span></span>

### <span data-ttu-id="3d18d-146">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="3d18d-146">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

### <span data-ttu-id="3d18d-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d18d-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d18d-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d18d-148">OUTPUTS</span></span>

### <span data-ttu-id="3d18d-149">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="3d18d-149">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="3d18d-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d18d-150">NOTES</span></span>

## <span data-ttu-id="3d18d-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d18d-151">RELATED LINKS</span></span>
