---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 614B0634-154A-449A-83E7-051DEF5A3BEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancerinboundnatpoolconfig
schema: 2.0.0
ms.openlocfilehash: 20837f96bc17d2cfd71abc359ff4114b44e6c062
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913624"
---
# <span data-ttu-id="ae684-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span><span class="sxs-lookup"><span data-stu-id="ae684-101">Get-AzureRmLoadBalancerInboundNatPoolConfig</span></span>

## <span data-ttu-id="ae684-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae684-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae684-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae684-103">SYNTAX</span></span>

```
Get-AzureRmLoadBalancerInboundNatPoolConfig [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae684-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae684-104">DESCRIPTION</span></span>

## <span data-ttu-id="ae684-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae684-105">EXAMPLES</span></span>

### <span data-ttu-id="ae684-106">1:</span><span class="sxs-lookup"><span data-stu-id="ae684-106">1:</span></span>
```
PS C:\>
```

## <span data-ttu-id="ae684-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae684-107">PARAMETERS</span></span>

### <span data-ttu-id="ae684-108">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae684-108">-DefaultProfile</span></span>
<span data-ttu-id="ae684-109">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae684-109">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae684-110">-Подсистема балансировки</span><span class="sxs-lookup"><span data-stu-id="ae684-110">-LoadBalancer</span></span>
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

### <span data-ttu-id="ae684-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae684-111">-Name</span></span>
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

### <span data-ttu-id="ae684-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae684-112">CommonParameters</span></span>
<span data-ttu-id="ae684-113">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae684-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae684-114">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae684-114">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae684-115">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae684-115">INPUTS</span></span>

### <span data-ttu-id="ae684-116">PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="ae684-116">PSLoadBalancer</span></span>
<span data-ttu-id="ae684-117">Параметр "подсистема" "подсистемы" принимает значение типа "PSLoadBalancer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ae684-117">Parameter 'LoadBalancer' accepts value of type 'PSLoadBalancer' from the pipeline</span></span>

## <span data-ttu-id="ae684-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae684-118">OUTPUTS</span></span>

### <span data-ttu-id="ae684-119">Microsoft. Azure. Commands. Network. Models. PSInboundNatPool</span><span class="sxs-lookup"><span data-stu-id="ae684-119">Microsoft.Azure.Commands.Network.Models.PSInboundNatPool</span></span>

## <span data-ttu-id="ae684-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae684-120">NOTES</span></span>

## <span data-ttu-id="ae684-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae684-121">RELATED LINKS</span></span>

