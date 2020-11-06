---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 903738f1cb2e816ce18c9e5e3c9b01cf3d4baa9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569319"
---
# <span data-ttu-id="c7538-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7538-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="c7538-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7538-102">SYNOPSIS</span></span>
<span data-ttu-id="c7538-103">Получение конфигурации правила сетевой безопасности для группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="c7538-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7538-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7538-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7538-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7538-105">DESCRIPTION</span></span>
<span data-ttu-id="c7538-106">Командлет **Get-AzureRmNetworkSecurityRuleConfig** получает конфигурацию правила сетевой безопасности для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="c7538-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="c7538-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7538-107">EXAMPLES</span></span>

### <span data-ttu-id="c7538-108">1: получение конфигурации правила сетевой безопасности</span><span class="sxs-lookup"><span data-stu-id="c7538-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="c7538-109">Эта команда извлекает правило по умолчанию с именем "AllowInternetOutBound" из группы безопасности сети Azure с именем "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="c7538-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="c7538-110">2. получение конфигурации правила сетевой безопасности с использованием только имени</span><span class="sxs-lookup"><span data-stu-id="c7538-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="c7538-111">Эта команда извлекает определяемое пользователем правило с именем "RDP-правило" из группы безопасности сети Azure с именем "nsg1" в группе ресурсов "Rg1"</span><span class="sxs-lookup"><span data-stu-id="c7538-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="c7538-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7538-112">PARAMETERS</span></span>

### <span data-ttu-id="c7538-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7538-113">-DefaultProfile</span></span>
<span data-ttu-id="c7538-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7538-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7538-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="c7538-115">-DefaultRules</span></span>
<span data-ttu-id="c7538-116">Указывает, получает ли этот командлет конфигурацию правила, созданную пользователем, или конфигурацию правила по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7538-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="c7538-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7538-117">-Name</span></span>
<span data-ttu-id="c7538-118">Указывает имя конфигурации правила сетевой безопасности, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c7538-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="c7538-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c7538-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="c7538-120">Указывает объект **NetworkSecurityGroup** , содержащий конфигурацию правила сетевой безопасности, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="c7538-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="c7538-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7538-121">CommonParameters</span></span>
<span data-ttu-id="c7538-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7538-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7538-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7538-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7538-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7538-124">INPUTS</span></span>

### <span data-ttu-id="c7538-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c7538-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="c7538-126">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c7538-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="c7538-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7538-127">OUTPUTS</span></span>

### <span data-ttu-id="c7538-128">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="c7538-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="c7538-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7538-129">NOTES</span></span>

## <span data-ttu-id="c7538-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7538-130">RELATED LINKS</span></span>

[<span data-ttu-id="c7538-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7538-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c7538-132">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7538-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c7538-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7538-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="c7538-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="c7538-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


