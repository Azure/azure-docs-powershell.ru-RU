---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: f861c1589d6f35c9650f0c20800b577e1724d66b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902378"
---
# <span data-ttu-id="5124d-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5124d-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="5124d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5124d-102">SYNOPSIS</span></span>
<span data-ttu-id="5124d-103">Получение конфигурации правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5124d-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5124d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5124d-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5124d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5124d-105">DESCRIPTION</span></span>
<span data-ttu-id="5124d-106">Командлет **Get-AzNetworkSecurityRuleConfig** получает конфигурацию правила сетевой безопасности для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="5124d-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="5124d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5124d-107">EXAMPLES</span></span>

### <span data-ttu-id="5124d-108">1: получение конфигурации правила сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="5124d-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="5124d-109">Эта команда извлекает правило по умолчанию с именем "AllowInternetOutBound" из группы безопасности сети Azure с именем "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="5124d-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="5124d-110">2. получение конфигурации правила сетевой безопасности с использованием только имени</span><span class="sxs-lookup"><span data-stu-id="5124d-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="5124d-111">Эта команда извлекает определяемое пользователем правило с именем "RDP-правило" из группы безопасности сети Azure с именем "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="5124d-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="5124d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5124d-112">PARAMETERS</span></span>

### <span data-ttu-id="5124d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5124d-113">-DefaultProfile</span></span>
<span data-ttu-id="5124d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5124d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5124d-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="5124d-115">-DefaultRules</span></span>
<span data-ttu-id="5124d-116">Указывает, получает ли этот командлет конфигурацию правила, созданную пользователем, или конфигурацию правила по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5124d-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="5124d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5124d-117">-Name</span></span>
<span data-ttu-id="5124d-118">Указывает имя конфигурации правила сетевой безопасности, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5124d-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="5124d-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5124d-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5124d-120">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5124d-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="5124d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5124d-121">CommonParameters</span></span>
<span data-ttu-id="5124d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5124d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5124d-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5124d-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5124d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5124d-124">INPUTS</span></span>

### <span data-ttu-id="5124d-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5124d-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5124d-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5124d-126">OUTPUTS</span></span>

### <span data-ttu-id="5124d-127">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="5124d-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="5124d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5124d-128">NOTES</span></span>

## <span data-ttu-id="5124d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5124d-129">RELATED LINKS</span></span>

[<span data-ttu-id="5124d-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5124d-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5124d-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5124d-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5124d-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5124d-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5124d-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5124d-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


