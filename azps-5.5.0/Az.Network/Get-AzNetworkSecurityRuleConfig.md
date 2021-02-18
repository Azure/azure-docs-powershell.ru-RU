---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241008"
---
# <span data-ttu-id="5dcfb-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dcfb-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="5dcfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="5dcfb-103">Настройка правил безопасности сети для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="5dcfb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5dcfb-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dcfb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5dcfb-105">DESCRIPTION</span></span>
<span data-ttu-id="5dcfb-106">Командлет **Get-AzNetworkSecurityRuleConfig** получает конфигурацию правила безопасности сети для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="5dcfb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5dcfb-107">EXAMPLES</span></span>

### <span data-ttu-id="5dcfb-108">1. Просмотр config правил безопасности сети</span><span class="sxs-lookup"><span data-stu-id="5dcfb-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="5dcfb-109">Эта команда извлекает правило по умолчанию AllowInternetOutBound из группы безопасности сети Azure "nsg1" в группе ресурсов "rg1"</span><span class="sxs-lookup"><span data-stu-id="5dcfb-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="5dcfb-110">2. Искомые сетевые правила безопасности, используя только имя</span><span class="sxs-lookup"><span data-stu-id="5dcfb-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="5dcfb-111">Эта команда извлекает определенное пользователем правило rdp-rule из группы безопасности сети Azure "nsg1" в группе ресурсов "rg1"</span><span class="sxs-lookup"><span data-stu-id="5dcfb-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="5dcfb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5dcfb-112">PARAMETERS</span></span>

### <span data-ttu-id="5dcfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dcfb-113">-DefaultProfile</span></span>
<span data-ttu-id="5dcfb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dcfb-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="5dcfb-115">-DefaultRules</span></span>
<span data-ttu-id="5dcfb-116">Указывает, получает ли этот cmdlet конфигурацию правил, созданную пользователем, или настройку правила по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="5dcfb-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5dcfb-117">-Name</span></span>
<span data-ttu-id="5dcfb-118">Указывает имя нужной конфигурации правила безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="5dcfb-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5dcfb-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="5dcfb-120">Объект **NetworkSecurityGroup,** который содержит конфигурацию правила безопасности сети, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="5dcfb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dcfb-121">CommonParameters</span></span>
<span data-ttu-id="5dcfb-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dcfb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dcfb-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5dcfb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dcfb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5dcfb-124">INPUTS</span></span>

### <span data-ttu-id="5dcfb-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="5dcfb-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="5dcfb-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5dcfb-126">OUTPUTS</span></span>

### <span data-ttu-id="5dcfb-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="5dcfb-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="5dcfb-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5dcfb-128">NOTES</span></span>

## <span data-ttu-id="5dcfb-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5dcfb-129">RELATED LINKS</span></span>

[<span data-ttu-id="5dcfb-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dcfb-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5dcfb-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dcfb-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5dcfb-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dcfb-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="5dcfb-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="5dcfb-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


