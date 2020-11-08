---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8ce5369605f419821994c771dc9200e138e5ad7a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073344"
---
# <span data-ttu-id="46e2b-101">Get-AzFirewallPolicyRuleCollectionGroup</span><span class="sxs-lookup"><span data-stu-id="46e2b-101">Get-AzFirewallPolicyRuleCollectionGroup</span></span>

## <span data-ttu-id="46e2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="46e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="46e2b-103">Получает группу набора правил политики брандмауэра для Azure</span><span class="sxs-lookup"><span data-stu-id="46e2b-103">Gets a Azure Firewall Policy Rule Collection Group</span></span>

## <span data-ttu-id="46e2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="46e2b-104">SYNTAX</span></span>

### <span data-ttu-id="46e2b-105">GetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46e2b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -ResourceGroupName <String>
 -AzureFirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2b-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46e2b-106">GetByInputObjectParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -Name <String> -AzureFirewallPolicy <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2b-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46e2b-107">GetByResourceIdParameterSet</span></span>
```
Get-AzFirewallPolicyRuleCollectionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46e2b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e2b-108">DESCRIPTION</span></span>
<span data-ttu-id="46e2b-109">Командлет **Get-AzFirewallPolicyRuleCollectionGroup** получает RuleCollectionGroup, упомянутый в политике брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="46e2b-109">The **Get-AzFirewallPolicyRuleCollectionGroup** cmdlet gets the RuleCollectionGroup mentioned from a Firewall Policy</span></span>

## <span data-ttu-id="46e2b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="46e2b-110">EXAMPLES</span></span>

### <span data-ttu-id="46e2b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46e2b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzFirewallPolicyRuleCollectionGroup -Name rg1 -AzureFirewallPolicy $fp
```

<span data-ttu-id="46e2b-112">В этом примере показано, как получить правило collectionGroup в политике брандмауэра $fp</span><span class="sxs-lookup"><span data-stu-id="46e2b-112">This example get the rule collectionGroup in the firewall policy $fp</span></span>

## <span data-ttu-id="46e2b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="46e2b-113">PARAMETERS</span></span>

### <span data-ttu-id="46e2b-114">-AzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="46e2b-114">-AzureFirewallPolicy</span></span>
<span data-ttu-id="46e2b-115">Политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="46e2b-115">Firewall Policy.</span></span>

```yaml
Type: PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e2b-116">-AzureFirewallPolicyName</span><span class="sxs-lookup"><span data-stu-id="46e2b-116">-AzureFirewallPolicyName</span></span>
<span data-ttu-id="46e2b-117">Имя политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="46e2b-117">The Firewall policy name</span></span>

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

### <span data-ttu-id="46e2b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e2b-118">-DefaultProfile</span></span>
<span data-ttu-id="46e2b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46e2b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e2b-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="46e2b-120">-Name</span></span>
<span data-ttu-id="46e2b-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="46e2b-121">The resource name.</span></span>

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

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="46e2b-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="46e2b-123">The resource group name.</span></span>

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

### <span data-ttu-id="46e2b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46e2b-124">-ResourceId</span></span>
<span data-ttu-id="46e2b-125">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="46e2b-125">The resource Id.</span></span>

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

### <span data-ttu-id="46e2b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e2b-126">CommonParameters</span></span>
<span data-ttu-id="46e2b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="46e2b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e2b-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46e2b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e2b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="46e2b-129">INPUTS</span></span>

### <span data-ttu-id="46e2b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="46e2b-130">System.String</span></span>

### <span data-ttu-id="46e2b-131">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="46e2b-131">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="46e2b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="46e2b-132">OUTPUTS</span></span>

### <span data-ttu-id="46e2b-133">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="46e2b-133">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

### <span data-ttu-id="46e2b-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network.. PSAzureFirewall, Microsoft. Azure. PowerShell. командлеты. Network, Version = 1.12.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="46e2b-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewall, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="46e2b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="46e2b-135">NOTES</span></span>

## <span data-ttu-id="46e2b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46e2b-136">RELATED LINKS</span></span>
