---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 9cb5a19adaf5c9d7371196a5ed917a557ef7c6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562408"
---
# <span data-ttu-id="806c1-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="806c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="806c1-102">SYNOPSIS</span></span>
<span data-ttu-id="806c1-103">Задает состояние цели для сетевой группы безопасности.</span><span class="sxs-lookup"><span data-stu-id="806c1-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="806c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="806c1-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="806c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="806c1-105">DESCRIPTION</span></span>
<span data-ttu-id="806c1-106">Командлет **Set-AzureRmNetworkSecurityGroup** задает состояние цели для группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="806c1-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="806c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="806c1-107">EXAMPLES</span></span>

### <span data-ttu-id="806c1-108">Пример 1: Установка состояния цели для сетевой группы безопасности</span><span class="sxs-lookup"><span data-stu-id="806c1-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="806c1-109">Эта команда получает сетевую группу безопасности Azure с именем Nsg1 и добавляет правило сетевой безопасности с именем Rdp-Rule, чтобы разрешить Интернет-трафик для порта 3389 в полученный объект групповой группы безопасности с помощью Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="806c1-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="806c1-110">Эта команда сохраняет измененную группу сетевой безопасности Azure с помощью **Set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="806c1-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="806c1-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="806c1-111">PARAMETERS</span></span>

### <span data-ttu-id="806c1-112">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-112">-NetworkSecurityGroup</span></span>
<span data-ttu-id="806c1-113">Объект Network Security Group, представляющий состояние цели, на которое командлет задает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="806c1-113">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="806c1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="806c1-114">-DefaultProfile</span></span>
<span data-ttu-id="806c1-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="806c1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="806c1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="806c1-116">CommonParameters</span></span>
<span data-ttu-id="806c1-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="806c1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="806c1-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="806c1-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="806c1-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="806c1-119">INPUTS</span></span>

### <span data-ttu-id="806c1-120">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-120">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="806c1-121">Параметр "NetworkSecurityGroup" принимает значение типа "PSNetworkSecurityGroup" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="806c1-121">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="806c1-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="806c1-122">OUTPUTS</span></span>

### <span data-ttu-id="806c1-123">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-123">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="806c1-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="806c1-124">NOTES</span></span>

## <span data-ttu-id="806c1-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="806c1-125">RELATED LINKS</span></span>

[<span data-ttu-id="806c1-126">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-126">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="806c1-127">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-127">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="806c1-128">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="806c1-128">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


