---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 547b38fd30f09a305c63054b2f27d33db5ae6a86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567265"
---
# <span data-ttu-id="c7b62-101">Get-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7b62-101">Get-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c7b62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7b62-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b62-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="c7b62-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7b62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7b62-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7b62-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b62-105">DESCRIPTION</span></span>
<span data-ttu-id="c7b62-106">Командлет **Get-AzureRmServiceEndpointPolicyDefinition** получает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="c7b62-106">The **Get-AzureRmServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="c7b62-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7b62-107">EXAMPLES</span></span>

### <span data-ttu-id="c7b62-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7b62-108">Example 1</span></span>
```
$policydef= Get-AzureRmServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="c7b62-109">Эта команда получает определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1 в ServiceEndpointPolicy $Policy сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="c7b62-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="c7b62-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7b62-110">PARAMETERS</span></span>

### <span data-ttu-id="c7b62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b62-111">-DefaultProfile</span></span>
<span data-ttu-id="c7b62-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b62-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7b62-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c7b62-113">-Name</span></span>
<span data-ttu-id="c7b62-114">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="c7b62-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="c7b62-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7b62-115">-ResourceId</span></span>
<span data-ttu-id="c7b62-116">{Определение ИД ресурса заполнения}}</span><span class="sxs-lookup"><span data-stu-id="c7b62-116">{{Fill ResourceId Description}}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7b62-117">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c7b62-117">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="c7b62-118">Политика конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="c7b62-118">The Service endpoint policy</span></span>

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

### <span data-ttu-id="c7b62-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7b62-119">-Confirm</span></span>
<span data-ttu-id="c7b62-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7b62-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b62-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7b62-121">-WhatIf</span></span>
<span data-ttu-id="c7b62-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7b62-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c7b62-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7b62-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7b62-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b62-124">CommonParameters</span></span>
<span data-ttu-id="c7b62-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7b62-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b62-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7b62-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b62-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7b62-127">INPUTS</span></span>

### <span data-ttu-id="c7b62-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="c7b62-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="c7b62-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7b62-129">OUTPUTS</span></span>

### <span data-ttu-id="c7b62-130">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="c7b62-130">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="c7b62-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7b62-131">NOTES</span></span>

## <span data-ttu-id="c7b62-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7b62-132">RELATED LINKS</span></span>
