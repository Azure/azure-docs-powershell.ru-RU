---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
ms.openlocfilehash: 348732794a0cf16233f9a139e86ed89658fc5ac2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914761"
---
# <span data-ttu-id="fc714-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="fc714-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc714-102">SYNOPSIS</span></span>
<span data-ttu-id="fc714-103">Задает состояние цели для сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="fc714-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc714-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc714-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc714-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc714-105">DESCRIPTION</span></span>
<span data-ttu-id="fc714-106">Командлет **Set-AzureRmNetworkSecurityGroup** задает состояние цели для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="fc714-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="fc714-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc714-107">EXAMPLES</span></span>

### <span data-ttu-id="fc714-108">Пример 1: Установка состояния цели для сетевой группы безопасности</span><span class="sxs-lookup"><span data-stu-id="fc714-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="fc714-109">Эта команда получает сетевую группу безопасности Azure с именем Nsg1 и добавляет правило сетевой безопасности с именем Rdp-Rule, чтобы разрешить Интернет-трафик для порта 3389 в полученный объект групповой группы безопасности с помощью Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="fc714-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="fc714-110">Эта команда сохраняет измененную группу сетевой безопасности Azure с помощью **Set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="fc714-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="fc714-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc714-111">PARAMETERS</span></span>

### <span data-ttu-id="fc714-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc714-112">-AsJob</span></span>
<span data-ttu-id="fc714-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fc714-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc714-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc714-114">-DefaultProfile</span></span>
<span data-ttu-id="fc714-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc714-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc714-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fc714-117">Объект Network Security Group, представляющий состояние цели, на которое командлет задает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="fc714-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc714-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc714-118">CommonParameters</span></span>
<span data-ttu-id="fc714-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc714-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc714-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc714-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc714-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc714-121">INPUTS</span></span>

### <span data-ttu-id="fc714-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="fc714-123">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fc714-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="fc714-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc714-124">OUTPUTS</span></span>

### <span data-ttu-id="fc714-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fc714-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc714-126">NOTES</span></span>

## <span data-ttu-id="fc714-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc714-127">RELATED LINKS</span></span>

[<span data-ttu-id="fc714-128">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-128">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="fc714-129">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-129">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="fc714-130">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fc714-130">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


