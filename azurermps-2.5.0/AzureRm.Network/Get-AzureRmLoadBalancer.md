---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermloadbalancer
schema: 2.0.0
ms.openlocfilehash: 39bbf3a30f4334e35f58109da86b9b07208682af
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913833"
---
# <span data-ttu-id="315a9-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="315a9-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="315a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="315a9-102">SYNOPSIS</span></span>
<span data-ttu-id="315a9-103">Получает подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="315a9-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="315a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="315a9-104">SYNTAX</span></span>

### <span data-ttu-id="315a9-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="315a9-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="315a9-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="315a9-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="315a9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="315a9-107">DESCRIPTION</span></span>
<span data-ttu-id="315a9-108">Командлет **Get-AzureRmLoadBalancer** получает один или несколько подсистем балансировки нагрузки для Azure, которые содержатся в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="315a9-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="315a9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="315a9-109">EXAMPLES</span></span>

### <span data-ttu-id="315a9-110">Пример 1: получение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="315a9-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="315a9-111">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="315a9-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="315a9-112">Для выполнения этого командлета должна существовать подсистема балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="315a9-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="315a9-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="315a9-113">PARAMETERS</span></span>

### <span data-ttu-id="315a9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="315a9-114">-DefaultProfile</span></span>
<span data-ttu-id="315a9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="315a9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="315a9-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="315a9-116">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315a9-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="315a9-117">-Name</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315a9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="315a9-118">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="315a9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="315a9-119">CommonParameters</span></span>
<span data-ttu-id="315a9-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="315a9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="315a9-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="315a9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="315a9-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="315a9-122">INPUTS</span></span>

## <span data-ttu-id="315a9-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="315a9-123">OUTPUTS</span></span>

### <span data-ttu-id="315a9-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="315a9-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="315a9-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="315a9-125">NOTES</span></span>

## <span data-ttu-id="315a9-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="315a9-126">RELATED LINKS</span></span>

[<span data-ttu-id="315a9-127">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="315a9-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="315a9-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="315a9-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="315a9-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="315a9-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


