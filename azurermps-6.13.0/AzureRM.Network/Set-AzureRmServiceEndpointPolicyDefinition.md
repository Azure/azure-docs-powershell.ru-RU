---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 1348eff2e4a2ac755ac0f425ddb29816438199b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732914"
---
# <span data-ttu-id="14ef2-101">Set-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="14ef2-101">Set-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="14ef2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14ef2-102">SYNOPSIS</span></span>
<span data-ttu-id="14ef2-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="14ef2-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14ef2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14ef2-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <System.Collections.Generic.List`1[System.String]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ef2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14ef2-105">DESCRIPTION</span></span>
<span data-ttu-id="14ef2-106">Командлет **Set-AzureRmServiceEndpointPolicyDefinition** создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="14ef2-106">The **Set-AzureRmServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="14ef2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14ef2-107">EXAMPLES</span></span>

### <span data-ttu-id="14ef2-108">Пример 1: обновление определения политики конечной точки службы в политике конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="14ef2-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="14ef2-109">Эта команда обновляет определение политики конечной точки службы с именем Policydef1 в политике конечной точки службы, определенной объектом $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="14ef2-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="14ef2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14ef2-110">PARAMETERS</span></span>

### <span data-ttu-id="14ef2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ef2-111">-DefaultProfile</span></span>
<span data-ttu-id="14ef2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14ef2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14ef2-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="14ef2-113">-Description</span></span>
<span data-ttu-id="14ef2-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="14ef2-114">The description of the definition</span></span>

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

### <span data-ttu-id="14ef2-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14ef2-115">-Name</span></span>
<span data-ttu-id="14ef2-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="14ef2-116">The name of the rule</span></span>

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

### <span data-ttu-id="14ef2-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="14ef2-117">-Service</span></span>
<span data-ttu-id="14ef2-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="14ef2-118">Name of the service</span></span>

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

### <span data-ttu-id="14ef2-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="14ef2-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="14ef2-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="14ef2-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="14ef2-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="14ef2-121">-ServiceResource</span></span>
<span data-ttu-id="14ef2-122">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="14ef2-122">List of service resources</span></span>

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

### <span data-ttu-id="14ef2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ef2-123">CommonParameters</span></span>
<span data-ttu-id="14ef2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14ef2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14ef2-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14ef2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ef2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14ef2-126">INPUTS</span></span>

### <span data-ttu-id="14ef2-127">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="14ef2-127">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="14ef2-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14ef2-128">OUTPUTS</span></span>

### <span data-ttu-id="14ef2-129">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="14ef2-129">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="14ef2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="14ef2-130">NOTES</span></span>

## <span data-ttu-id="14ef2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14ef2-131">RELATED LINKS</span></span>
