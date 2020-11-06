---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmLoadBalancer.md
ms.openlocfilehash: 764d26c2b0b95b74277fc74dab03fe55d12261f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567106"
---
# <span data-ttu-id="a1bca-101">Get-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1bca-101">Get-AzureRmLoadBalancer</span></span>

## <span data-ttu-id="a1bca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1bca-102">SYNOPSIS</span></span>
<span data-ttu-id="a1bca-103">Получает подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1bca-103">Gets a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1bca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1bca-104">SYNTAX</span></span>

### <span data-ttu-id="a1bca-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="a1bca-105">NoExpand</span></span>
```
Get-AzureRmLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1bca-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="a1bca-106">Expand</span></span>
```
Get-AzureRmLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a1bca-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1bca-107">DESCRIPTION</span></span>
<span data-ttu-id="a1bca-108">Командлет **Get-AzureRmLoadBalancer** получает один или несколько подсистем балансировки нагрузки для Azure, которые содержатся в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a1bca-108">The **Get-AzureRmLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="a1bca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1bca-109">EXAMPLES</span></span>

### <span data-ttu-id="a1bca-110">Пример 1: получение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="a1bca-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzureRmLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="a1bca-111">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="a1bca-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="a1bca-112">Для выполнения этого командлета должна существовать подсистема балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="a1bca-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="a1bca-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1bca-113">PARAMETERS</span></span>

### <span data-ttu-id="a1bca-114">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="a1bca-114">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bca-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1bca-115">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bca-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1bca-116">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1bca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1bca-117">-DefaultProfile</span></span>
<span data-ttu-id="a1bca-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1bca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1bca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1bca-119">CommonParameters</span></span>
<span data-ttu-id="a1bca-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1bca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1bca-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1bca-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1bca-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1bca-122">INPUTS</span></span>

## <span data-ttu-id="a1bca-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1bca-123">OUTPUTS</span></span>

### <span data-ttu-id="a1bca-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1bca-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="a1bca-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1bca-125">NOTES</span></span>

## <span data-ttu-id="a1bca-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1bca-126">RELATED LINKS</span></span>

[<span data-ttu-id="a1bca-127">New-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1bca-127">New-AzureRmLoadBalancer</span></span>](./New-AzureRmLoadBalancer.md)

[<span data-ttu-id="a1bca-128">Remove-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1bca-128">Remove-AzureRmLoadBalancer</span></span>](./Remove-AzureRmLoadBalancer.md)

[<span data-ttu-id="a1bca-129">Set-AzureRmLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a1bca-129">Set-AzureRmLoadBalancer</span></span>](./Set-AzureRmLoadBalancer.md)


