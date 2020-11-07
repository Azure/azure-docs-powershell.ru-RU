---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: fffc77c4cfdd74a910086befb88d665351ae36a8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730463"
---
# <span data-ttu-id="9a23d-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="9a23d-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="9a23d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a23d-102">SYNOPSIS</span></span>
<span data-ttu-id="9a23d-103">Получает текущее использование виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a23d-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="9a23d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a23d-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a23d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a23d-105">DESCRIPTION</span></span>
<span data-ttu-id="9a23d-106">Командлет **Get-AzVirtualNetworkUsageList** получает использование подсети для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9a23d-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="9a23d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a23d-107">EXAMPLES</span></span>

### <span data-ttu-id="9a23d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9a23d-108">Example 1</span></span>
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

<span data-ttu-id="9a23d-109">Получает текущие значения для использования в подсети для виртуальной сети usagetest.</span><span class="sxs-lookup"><span data-stu-id="9a23d-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="9a23d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a23d-110">PARAMETERS</span></span>

### <span data-ttu-id="9a23d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a23d-111">-DefaultProfile</span></span>
<span data-ttu-id="9a23d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a23d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a23d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a23d-113">-Name</span></span>
<span data-ttu-id="9a23d-114">Указывает имя виртуальной сети, для которой нужно показать использование.</span><span class="sxs-lookup"><span data-stu-id="9a23d-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="9a23d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a23d-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a23d-116">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="9a23d-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="9a23d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a23d-117">CommonParameters</span></span>
<span data-ttu-id="9a23d-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a23d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a23d-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a23d-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a23d-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a23d-120">INPUTS</span></span>

### <span data-ttu-id="9a23d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9a23d-121">System.String</span></span>

## <span data-ttu-id="9a23d-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a23d-122">OUTPUTS</span></span>

### <span data-ttu-id="9a23d-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="9a23d-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="9a23d-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a23d-124">NOTES</span></span>

## <span data-ttu-id="9a23d-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a23d-125">RELATED LINKS</span></span>
