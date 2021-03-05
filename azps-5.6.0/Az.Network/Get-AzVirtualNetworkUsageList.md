---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: b4daa24f787633d2f18896910faed340a969a0f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997713"
---
# <span data-ttu-id="8ebe5-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="8ebe5-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="8ebe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ebe5-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebe5-103">Возвращает текущее использование виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="8ebe5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ebe5-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ebe5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ebe5-105">DESCRIPTION</span></span>
<span data-ttu-id="8ebe5-106">Командлет **Get-AzVirtualNetworkUsageList** получает данные об использовании подсети для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="8ebe5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ebe5-107">EXAMPLES</span></span>

### <span data-ttu-id="8ebe5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ebe5-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="8ebe5-109">Возвращает текущие значения использования для подсети для виртуальной сети usagetest.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="8ebe5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ebe5-110">PARAMETERS</span></span>

### <span data-ttu-id="8ebe5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebe5-111">-DefaultProfile</span></span>
<span data-ttu-id="8ebe5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ebe5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8ebe5-113">-Name</span></span>
<span data-ttu-id="8ebe5-114">Указывает имя виртуальной сети, для которого нужно показать использование.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebe5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebe5-115">-ResourceGroupName</span></span>
<span data-ttu-id="8ebe5-116">Имя группы ресурсов, к которой относится виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ebe5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebe5-117">CommonParameters</span></span>
<span data-ttu-id="8ebe5-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebe5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebe5-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ebe5-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebe5-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ebe5-120">INPUTS</span></span>

### <span data-ttu-id="8ebe5-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8ebe5-121">System.String</span></span>

## <span data-ttu-id="8ebe5-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ebe5-122">OUTPUTS</span></span>

### <span data-ttu-id="8ebe5-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="8ebe5-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="8ebe5-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ebe5-124">NOTES</span></span>

## <span data-ttu-id="8ebe5-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ebe5-125">RELATED LINKS</span></span>
