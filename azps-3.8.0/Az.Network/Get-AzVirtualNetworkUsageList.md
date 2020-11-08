---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065836"
---
# <span data-ttu-id="81bb0-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="81bb0-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="81bb0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="81bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="81bb0-103">Получает текущее использование виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="81bb0-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="81bb0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="81bb0-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81bb0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="81bb0-106">Командлет **Get-AzVirtualNetworkUsageList** получает использование подсети для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="81bb0-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="81bb0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="81bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="81bb0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="81bb0-108">Example 1</span></span>
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

<span data-ttu-id="81bb0-109">Получает текущие значения для использования в подсети для виртуальной сети usagetest.</span><span class="sxs-lookup"><span data-stu-id="81bb0-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="81bb0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="81bb0-110">PARAMETERS</span></span>

### <span data-ttu-id="81bb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81bb0-111">-DefaultProfile</span></span>
<span data-ttu-id="81bb0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81bb0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81bb0-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="81bb0-113">-Name</span></span>
<span data-ttu-id="81bb0-114">Указывает имя виртуальной сети, для которой нужно показать использование.</span><span class="sxs-lookup"><span data-stu-id="81bb0-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="81bb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81bb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="81bb0-116">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="81bb0-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="81bb0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81bb0-117">CommonParameters</span></span>
<span data-ttu-id="81bb0-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="81bb0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81bb0-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="81bb0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81bb0-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="81bb0-120">INPUTS</span></span>

### <span data-ttu-id="81bb0-121">System. String</span><span class="sxs-lookup"><span data-stu-id="81bb0-121">System.String</span></span>

## <span data-ttu-id="81bb0-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="81bb0-122">OUTPUTS</span></span>

### <span data-ttu-id="81bb0-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="81bb0-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="81bb0-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="81bb0-124">NOTES</span></span>

## <span data-ttu-id="81bb0-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81bb0-125">RELATED LINKS</span></span>
