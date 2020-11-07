---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 7937af38c7dd0becd57604a0a7c00e5d1f584e6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730014"
---
# <span data-ttu-id="100d3-101">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-101">Set-AzFirewall</span></span>

## <span data-ttu-id="100d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="100d3-102">SYNOPSIS</span></span>
<span data-ttu-id="100d3-103">Сохранение измененного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="100d3-103">Saves a modified Firewall.</span></span>

## <span data-ttu-id="100d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="100d3-104">SYNTAX</span></span>

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="100d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="100d3-105">DESCRIPTION</span></span>
<span data-ttu-id="100d3-106">Командлет **Set-AzFirewall** обновляет брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="100d3-106">The **Set-AzFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="100d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="100d3-107">EXAMPLES</span></span>

### <span data-ttu-id="100d3-108">1: обновление приоритета коллекции правил приложения брандмауэра</span><span class="sxs-lookup"><span data-stu-id="100d3-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

<span data-ttu-id="100d3-109">В этом примере обновляется приоритет существующей коллекции правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="100d3-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="100d3-110">Предполагается, что брандмауэр Azure "AzureFirewall" в группе ресурсов "RG" имеет коллекцию правил приложений с именем "ruleCollectionName", команды выше будут изменять приоритет этой коллекции правил и затем обновлять брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="100d3-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="100d3-111">Без команды Set-AzFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="100d3-111">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="100d3-112">2. Создание брандмауэра Azure и установка коллекции правил приложений позже</span><span class="sxs-lookup"><span data-stu-id="100d3-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

<span data-ttu-id="100d3-113">В этом примере брандмауэр создается в первую очередь без каких-либо коллекций правил приложений.</span><span class="sxs-lookup"><span data-stu-id="100d3-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="100d3-114">После этого создается правило приложения и коллекция правил приложения, а затем объект Firewall изменяется в памяти, не влияя на реальную конфигурацию в облаке.</span><span class="sxs-lookup"><span data-stu-id="100d3-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="100d3-115">Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="100d3-115">For changes to be reflected in cloud, Set-AzFirewall must be called.</span></span>

### <span data-ttu-id="100d3-116">3: обновление угрозы в режиме функционирования Intel в брандмауэре Azure</span><span class="sxs-lookup"><span data-stu-id="100d3-116">3:  Update Threat Intel operation mode of Azure Firewall</span></span>
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

<span data-ttu-id="100d3-117">В этом примере обновляется режим функционирования программного кода Intel для брандмауэра Azure "AzureFirewall" в группе ресурсов "RG".</span><span class="sxs-lookup"><span data-stu-id="100d3-117">This example updates the Threat Intel operation mode of Azure Firewall "AzureFirewall" in resource group "rg".</span></span>
<span data-ttu-id="100d3-118">Без команды Set-AzFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="100d3-118">Without the Set-AzFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

## <span data-ttu-id="100d3-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="100d3-119">PARAMETERS</span></span>

### <span data-ttu-id="100d3-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="100d3-120">-AsJob</span></span>
<span data-ttu-id="100d3-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="100d3-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="100d3-122">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-122">-AzureFirewall</span></span>
<span data-ttu-id="100d3-123">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-123">The AzureFirewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="100d3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="100d3-124">-DefaultProfile</span></span>
<span data-ttu-id="100d3-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="100d3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="100d3-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="100d3-126">-Confirm</span></span>
<span data-ttu-id="100d3-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="100d3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="100d3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="100d3-128">-WhatIf</span></span>
<span data-ttu-id="100d3-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="100d3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="100d3-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="100d3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="100d3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100d3-131">CommonParameters</span></span>
<span data-ttu-id="100d3-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="100d3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100d3-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="100d3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100d3-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="100d3-134">INPUTS</span></span>

### <span data-ttu-id="100d3-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="100d3-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="100d3-136">OUTPUTS</span></span>

### <span data-ttu-id="100d3-137">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="100d3-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="100d3-138">NOTES</span></span>

## <span data-ttu-id="100d3-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="100d3-139">RELATED LINKS</span></span>

[<span data-ttu-id="100d3-140">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-140">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="100d3-141">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-141">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="100d3-142">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="100d3-142">Remove-AzFirewall</span></span>](./Remove-AzFirewall.md)
