---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556611"
---
# <span data-ttu-id="fe1c9-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="fe1c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe1c9-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1c9-103">Сохранение измененного брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe1c9-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe1c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1c9-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1c9-106">Командлет **Set-AzureRmFirewall** обновляет брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="fe1c9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe1c9-107">EXAMPLES</span></span>

### <span data-ttu-id="fe1c9-108">1: обновление приоритета коллекции правил приложения брандмауэра</span><span class="sxs-lookup"><span data-stu-id="fe1c9-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="fe1c9-109">В этом примере обновляется приоритет существующей коллекции правил брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="fe1c9-110">Предполагается, что брандмауэр Azure "AzureFirewall" в группе ресурсов "RG" имеет коллекцию правил приложений с именем "ruleCollectionName", команды выше будут изменять приоритет этой коллекции правил и затем обновлять брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="fe1c9-111">Без команды Set-AzureRmFirewall все операции, выполненные на локальном объекте $azFw, не отражаются на сервере.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="fe1c9-112">2. Создание брандмауэра Azure и установка коллекции правил приложений позже</span><span class="sxs-lookup"><span data-stu-id="fe1c9-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="fe1c9-113">В этом примере брандмауэр создается в первую очередь без каких-либо коллекций правил приложений.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="fe1c9-114">После этого создается правило приложения и коллекция правил приложения, а затем объект Firewall изменяется в памяти, не влияя на реальную конфигурацию в облаке.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="fe1c9-115">Чтобы изменения были отражены в облаке, необходимо вызвать Set-AzureRmFirewall.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="fe1c9-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1c9-116">PARAMETERS</span></span>

### <span data-ttu-id="fe1c9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe1c9-117">-AsJob</span></span>
<span data-ttu-id="fe1c9-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fe1c9-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe1c9-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-119">-AzureFirewall</span></span>
<span data-ttu-id="fe1c9-120">AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1c9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1c9-121">-DefaultProfile</span></span>
<span data-ttu-id="fe1c9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1c9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe1c9-123">-Confirm</span></span>
<span data-ttu-id="fe1c9-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe1c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1c9-125">-WhatIf</span></span>
<span data-ttu-id="fe1c9-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe1c9-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe1c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1c9-128">CommonParameters</span></span>
<span data-ttu-id="fe1c9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1c9-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1c9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1c9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe1c9-131">INPUTS</span></span>

### <span data-ttu-id="fe1c9-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-132">PSAzureFirewall</span></span>
<span data-ttu-id="fe1c9-133">Параметр "AzureFirewall" принимает значение типа "PSAzureFirewall" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fe1c9-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="fe1c9-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1c9-134">OUTPUTS</span></span>

### <span data-ttu-id="fe1c9-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="fe1c9-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe1c9-136">NOTES</span></span>

## <span data-ttu-id="fe1c9-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1c9-137">RELATED LINKS</span></span>

[<span data-ttu-id="fe1c9-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="fe1c9-139">New-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="fe1c9-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="fe1c9-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
