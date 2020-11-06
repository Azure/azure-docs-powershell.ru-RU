---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 855385b55922f6255b407ceafef7422113968516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562943"
---
# <span data-ttu-id="29f2d-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="29f2d-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="29f2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="29f2d-103">Получает текущее использование виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="29f2d-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29f2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29f2d-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29f2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29f2d-105">DESCRIPTION</span></span>
<span data-ttu-id="29f2d-106">Командлет **Get-AzureRmVirtualNetworkUsageList** получает использование подсети для указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="29f2d-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="29f2d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29f2d-107">EXAMPLES</span></span>

### <span data-ttu-id="29f2d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29f2d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="29f2d-109">Получает текущие значения для использования в подсети для виртуальной сети usagetest.</span><span class="sxs-lookup"><span data-stu-id="29f2d-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="29f2d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29f2d-110">PARAMETERS</span></span>

### <span data-ttu-id="29f2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29f2d-111">-DefaultProfile</span></span>
<span data-ttu-id="29f2d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29f2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29f2d-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29f2d-113">-Name</span></span>
<span data-ttu-id="29f2d-114">Указывает имя виртуальной сети, для которой нужно показать использование.</span><span class="sxs-lookup"><span data-stu-id="29f2d-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="29f2d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29f2d-115">-ResourceGroupName</span></span>
<span data-ttu-id="29f2d-116">Указывает имя группы ресурсов, к которой принадлежит виртуальная сеть.</span><span class="sxs-lookup"><span data-stu-id="29f2d-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="29f2d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29f2d-117">CommonParameters</span></span>
<span data-ttu-id="29f2d-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29f2d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29f2d-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29f2d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29f2d-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29f2d-120">INPUTS</span></span>

### <span data-ttu-id="29f2d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="29f2d-121">System.String</span></span>

## <span data-ttu-id="29f2d-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29f2d-122">OUTPUTS</span></span>

### <span data-ttu-id="29f2d-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="29f2d-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="29f2d-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="29f2d-124">NOTES</span></span>

## <span data-ttu-id="29f2d-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29f2d-125">RELATED LINKS</span></span>
