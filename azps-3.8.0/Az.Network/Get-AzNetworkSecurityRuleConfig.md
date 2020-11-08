---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073315"
---
# <span data-ttu-id="db8bb-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db8bb-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="db8bb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db8bb-102">SYNOPSIS</span></span>
<span data-ttu-id="db8bb-103">Получение конфигурации правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="db8bb-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="db8bb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db8bb-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db8bb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db8bb-105">DESCRIPTION</span></span>
<span data-ttu-id="db8bb-106">Командлет **Get-AzNetworkSecurityRuleConfig** получает конфигурацию правила сетевой безопасности для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="db8bb-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="db8bb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db8bb-107">EXAMPLES</span></span>

### <span data-ttu-id="db8bb-108">1: получение конфигурации правила сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="db8bb-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="db8bb-109">Эта команда извлекает правило по умолчанию с именем "AllowInternetOutBound" из группы безопасности сети Azure с именем "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="db8bb-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="db8bb-110">2. получение конфигурации правила сетевой безопасности с использованием только имени</span><span class="sxs-lookup"><span data-stu-id="db8bb-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="db8bb-111">Эта команда извлекает определяемое пользователем правило с именем "RDP-правило" из группы безопасности сети Azure с именем "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="db8bb-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="db8bb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db8bb-112">PARAMETERS</span></span>

### <span data-ttu-id="db8bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db8bb-113">-DefaultProfile</span></span>
<span data-ttu-id="db8bb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db8bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db8bb-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="db8bb-115">-DefaultRules</span></span>
<span data-ttu-id="db8bb-116">Указывает, получает ли этот командлет конфигурацию правила, созданную пользователем, или конфигурацию правила по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="db8bb-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="db8bb-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db8bb-117">-Name</span></span>
<span data-ttu-id="db8bb-118">Указывает имя конфигурации правила сетевой безопасности, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="db8bb-118">Specifies the name of the network security rule configuration to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db8bb-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db8bb-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="db8bb-120">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="db8bb-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="db8bb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db8bb-121">CommonParameters</span></span>
<span data-ttu-id="db8bb-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db8bb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db8bb-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db8bb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db8bb-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db8bb-124">INPUTS</span></span>

### <span data-ttu-id="db8bb-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="db8bb-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="db8bb-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db8bb-126">OUTPUTS</span></span>

### <span data-ttu-id="db8bb-127">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="db8bb-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="db8bb-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="db8bb-128">NOTES</span></span>

## <span data-ttu-id="db8bb-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db8bb-129">RELATED LINKS</span></span>

[<span data-ttu-id="db8bb-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db8bb-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="db8bb-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db8bb-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="db8bb-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db8bb-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="db8bb-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="db8bb-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


