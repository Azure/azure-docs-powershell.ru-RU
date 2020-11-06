---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 12d809ad4c1df021891ab5acf384415d64aa08a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567703"
---
# <span data-ttu-id="5b10c-101">New-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b10c-101">New-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="5b10c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b10c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b10c-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="5b10c-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5b10c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b10c-104">SYNTAX</span></span>

```
New-AzureRmServiceEndpointPolicyDefinition -Name <String> [-Description <String>]
 [-ServiceResource <System.Collections.Generic.List`1[System.String]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b10c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b10c-105">DESCRIPTION</span></span>
<span data-ttu-id="5b10c-106">Командлет **New-AzureRmServiceEndpointPolicyDefinition** создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="5b10c-106">The **New-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="5b10c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b10c-107">EXAMPLES</span></span>

### <span data-ttu-id="5b10c-108">Пример 1: Создание политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="5b10c-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="5b10c-109">Эта команда создает определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1, обслуживанием Microsoft. Storage, подписками на ресурсы служб/Sub1 и описанием "новое определение", которое принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="5b10c-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="5b10c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b10c-110">PARAMETERS</span></span>

### <span data-ttu-id="5b10c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b10c-111">-DefaultProfile</span></span>
<span data-ttu-id="5b10c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b10c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b10c-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="5b10c-113">-Description</span></span>
<span data-ttu-id="5b10c-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="5b10c-114">The description of the definition</span></span>

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

### <span data-ttu-id="5b10c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b10c-115">-Name</span></span>
<span data-ttu-id="5b10c-116">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="5b10c-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="5b10c-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="5b10c-117">-Service</span></span>
<span data-ttu-id="5b10c-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="5b10c-118">Name of the service</span></span>

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

### <span data-ttu-id="5b10c-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="5b10c-119">-ServiceResource</span></span>
<span data-ttu-id="5b10c-120">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="5b10c-120">List of service resources</span></span>

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

### <span data-ttu-id="5b10c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b10c-121">CommonParameters</span></span>
<span data-ttu-id="5b10c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b10c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5b10c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b10c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b10c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b10c-124">INPUTS</span></span>

### <span data-ttu-id="5b10c-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="5b10c-125">None</span></span>


## <span data-ttu-id="5b10c-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b10c-126">OUTPUTS</span></span>

### <span data-ttu-id="5b10c-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="5b10c-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>


## <span data-ttu-id="5b10c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b10c-128">NOTES</span></span>

## <span data-ttu-id="5b10c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b10c-129">RELATED LINKS</span></span>
