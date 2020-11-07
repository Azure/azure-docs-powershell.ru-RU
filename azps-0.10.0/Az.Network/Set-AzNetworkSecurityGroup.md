---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 1c61af223b97ac60dd74f55504ce623b26b5233e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911033"
---
# <span data-ttu-id="3a2a4-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="3a2a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="3a2a4-103">Задает состояние цели для сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-103">Sets the goal state for a network security group.</span></span>

## <span data-ttu-id="3a2a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a2a4-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a2a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a2a4-105">DESCRIPTION</span></span>
<span data-ttu-id="3a2a4-106">Командлет **Set-AzNetworkSecurityGroup** задает состояние цели для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-106">The **Set-AzNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="3a2a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a2a4-107">EXAMPLES</span></span>

### <span data-ttu-id="3a2a4-108">Пример 1: Установка состояния цели для сетевой группы безопасности</span><span class="sxs-lookup"><span data-stu-id="3a2a4-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="3a2a4-109">Эта команда получает сетевую группу безопасности Azure с именем Nsg1 и добавляет правило сетевой безопасности с именем Rdp-Rule, чтобы разрешить Интернет-трафик для порта 3389 в полученный объект групповой группы безопасности с помощью Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="3a2a4-110">Эта команда сохраняет измененную группу сетевой безопасности Azure с помощью **Set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="3a2a4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a2a4-111">PARAMETERS</span></span>

### <span data-ttu-id="3a2a4-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a2a4-112">-AsJob</span></span>
<span data-ttu-id="3a2a4-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a2a4-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a2a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a2a4-114">-DefaultProfile</span></span>
<span data-ttu-id="3a2a4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a2a4-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3a2a4-117">Объект Network Security Group, представляющий состояние цели, на которое командлет задает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="3a2a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a2a4-118">CommonParameters</span></span>
<span data-ttu-id="3a2a4-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a2a4-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a2a4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a2a4-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a2a4-121">INPUTS</span></span>

### <span data-ttu-id="3a2a4-122">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-122">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="3a2a4-123">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3a2a4-123">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="3a2a4-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a2a4-124">OUTPUTS</span></span>

### <span data-ttu-id="3a2a4-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3a2a4-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a2a4-126">NOTES</span></span>

## <span data-ttu-id="3a2a4-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a2a4-127">RELATED LINKS</span></span>

[<span data-ttu-id="3a2a4-128">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-128">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3a2a4-129">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-129">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3a2a4-130">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3a2a4-130">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


