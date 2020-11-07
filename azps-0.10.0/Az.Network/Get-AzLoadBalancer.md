---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: f5f0ce9768226c79210db3a38c5c09303e94a852
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909989"
---
# <span data-ttu-id="79c95-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79c95-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="79c95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79c95-102">SYNOPSIS</span></span>
<span data-ttu-id="79c95-103">Получает подсистему балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79c95-103">Gets a load balancer.</span></span>

## <span data-ttu-id="79c95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79c95-104">SYNTAX</span></span>

### <span data-ttu-id="79c95-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="79c95-105">NoExpand</span></span>
```
Get-AzLoadBalancer [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79c95-106">Кройте</span><span class="sxs-lookup"><span data-stu-id="79c95-106">Expand</span></span>
```
Get-AzLoadBalancer -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c95-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c95-107">DESCRIPTION</span></span>
<span data-ttu-id="79c95-108">Командлет **Get-AzLoadBalancer** получает один или несколько подсистем балансировки нагрузки для Azure, которые содержатся в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79c95-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="79c95-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79c95-109">EXAMPLES</span></span>

### <span data-ttu-id="79c95-110">Пример 1: получение подсистемы балансировки нагрузки</span><span class="sxs-lookup"><span data-stu-id="79c95-110">Example 1: Get a load balancer</span></span>
```
PS C:\>Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="79c95-111">Эта команда получает подсистему балансировки нагрузки с именем MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="79c95-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="79c95-112">Для выполнения этого командлета должна существовать подсистема балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="79c95-112">A load balancer must exist before you can run this cmdlet.</span></span>

## <span data-ttu-id="79c95-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79c95-113">PARAMETERS</span></span>

### <span data-ttu-id="79c95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c95-114">-DefaultProfile</span></span>
<span data-ttu-id="79c95-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79c95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79c95-116">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="79c95-116">-ExpandResource</span></span>
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

### <span data-ttu-id="79c95-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79c95-117">-Name</span></span>
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

### <span data-ttu-id="79c95-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c95-118">-ResourceGroupName</span></span>
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

### <span data-ttu-id="79c95-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c95-119">CommonParameters</span></span>
<span data-ttu-id="79c95-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79c95-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c95-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c95-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c95-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79c95-122">INPUTS</span></span>

## <span data-ttu-id="79c95-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c95-123">OUTPUTS</span></span>

### <span data-ttu-id="79c95-124">Microsoft. Azure. Commands. Network. Models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79c95-124">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="79c95-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="79c95-125">NOTES</span></span>

## <span data-ttu-id="79c95-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79c95-126">RELATED LINKS</span></span>

[<span data-ttu-id="79c95-127">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79c95-127">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="79c95-128">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79c95-128">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="79c95-129">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="79c95-129">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


