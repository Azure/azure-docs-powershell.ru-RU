---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98D2EB70-440F-45C4-A79A-EB87BBDC6256
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmLoadBalancerInboundNatPoolConfig.md
ms.openlocfilehash: fd2a38a7b17e32a12cda0de7b5b620cffef9dfa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560255"
---
# <span data-ttu-id="e663a-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="e663a-101">Remove-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="e663a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e663a-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e663a-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e663a-103">SYNTAX</span></span>

```
Remove-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e663a-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e663a-104">DESCRIPTION</span></span>

## <span data-ttu-id="e663a-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e663a-105">EXAMPLES</span></span>

### <span data-ttu-id="e663a-106">1:</span><span class="sxs-lookup"><span data-stu-id="e663a-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="e663a-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e663a-107">PARAMETERS</span></span>

### <span data-ttu-id="e663a-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e663a-108">-DefaultProfile</span></span>
<span data-ttu-id="e663a-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e663a-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e663a-110">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="e663a-110">-LoadBalancer</span></span>
```yaml
Type: PSLoadBalancer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e663a-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e663a-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e663a-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e663a-112">CommonParameters</span></span>
<span data-ttu-id="e663a-113">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e663a-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e663a-114">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e663a-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e663a-115">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e663a-115">INPUTS</span></span>

### <span data-ttu-id="e663a-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e663a-116">PSLoadBalancer</span></span>
<span data-ttu-id="e663a-117">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e663a-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="e663a-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e663a-118">OUTPUTS</span></span>

### <span data-ttu-id="e663a-119">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="e663a-119">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="e663a-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="e663a-120">NOTES</span></span>

## <span data-ttu-id="e663a-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e663a-121">RELATED LINKS</span></span>

