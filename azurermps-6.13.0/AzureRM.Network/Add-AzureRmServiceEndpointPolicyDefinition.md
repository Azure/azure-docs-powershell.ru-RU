---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: ac58450295e0e2d988c12c308c0210b38ad71b4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733829"
---
# <span data-ttu-id="d67ea-101">Add-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d67ea-101">Add-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="d67ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d67ea-102">SYNOPSIS</span></span>
<span data-ttu-id="d67ea-103">Добавляет определение политики конечной точки службы к указанной политике.</span><span class="sxs-lookup"><span data-stu-id="d67ea-103">Adds a service endpoint policy definition to a specified policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d67ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d67ea-104">SYNTAX</span></span>

```
Add-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d67ea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67ea-105">DESCRIPTION</span></span>
<span data-ttu-id="d67ea-106">Командлет **Add-AzureRmServiceEndpointPolicyDefinition** добавляет определение политики конечной точки службы в политику.</span><span class="sxs-lookup"><span data-stu-id="d67ea-106">The **Add-AzureRmServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="d67ea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d67ea-107">EXAMPLES</span></span>

### <span data-ttu-id="d67ea-108">Пример 1: обновление определения политики конечной точки службы в политике конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="d67ea-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="d67ea-109">Эта команда обновила определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1, обслуживанием Microsoft. Storage, подписками на ресурсы служб/Sub1 и описанием "новое определение", которое принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="d67ea-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="d67ea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d67ea-110">PARAMETERS</span></span>

### <span data-ttu-id="d67ea-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d67ea-111">-DefaultProfile</span></span>
<span data-ttu-id="d67ea-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d67ea-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d67ea-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="d67ea-113">-Description</span></span>
<span data-ttu-id="d67ea-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="d67ea-114">The description of the definition</span></span>

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

### <span data-ttu-id="d67ea-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d67ea-115">-Name</span></span>
<span data-ttu-id="d67ea-116">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="d67ea-116">The name of the service endpoint policy definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67ea-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="d67ea-117">-Service</span></span>
<span data-ttu-id="d67ea-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="d67ea-118">Name of the service</span></span>

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

### <span data-ttu-id="d67ea-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d67ea-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d67ea-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d67ea-120">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d67ea-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="d67ea-121">-ServiceResource</span></span>
<span data-ttu-id="d67ea-122">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="d67ea-122">List of service resources</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d67ea-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d67ea-123">CommonParameters</span></span>
<span data-ttu-id="d67ea-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d67ea-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d67ea-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d67ea-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d67ea-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d67ea-126">INPUTS</span></span>

### <span data-ttu-id="d67ea-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d67ea-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="d67ea-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d67ea-128">OUTPUTS</span></span>

### <span data-ttu-id="d67ea-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d67ea-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="d67ea-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d67ea-130">NOTES</span></span>

## <span data-ttu-id="d67ea-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d67ea-131">RELATED LINKS</span></span>
