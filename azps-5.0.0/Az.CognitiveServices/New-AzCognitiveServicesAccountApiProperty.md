---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315173"
---
# <span data-ttu-id="a5b57-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="a5b57-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="a5b57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5b57-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b57-103">Создание нового экземпляра учетной записи самообслуживания ApiProperties</span><span class="sxs-lookup"><span data-stu-id="a5b57-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="a5b57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5b57-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5b57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b57-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b57-106">Создайте новый экземпляр учетной записи службы ApiProperties.</span><span class="sxs-lookup"><span data-stu-id="a5b57-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="a5b57-107">ApiProperties можно использовать при создании новой или обновлении существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="a5b57-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="a5b57-108">ApiProperties является обязательным для некоторых типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="a5b57-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="a5b57-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5b57-109">EXAMPLES</span></span>

### <span data-ttu-id="a5b57-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a5b57-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="a5b57-111">В приведенном выше примере создается учетная запись QnAMaker с свойством API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="a5b57-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="a5b57-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5b57-112">PARAMETERS</span></span>

### <span data-ttu-id="a5b57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b57-113">-DefaultProfile</span></span>
<span data-ttu-id="a5b57-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5b57-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5b57-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5b57-115">-Confirm</span></span>
<span data-ttu-id="a5b57-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5b57-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b57-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b57-117">-WhatIf</span></span>
<span data-ttu-id="a5b57-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5b57-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b57-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5b57-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b57-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b57-120">CommonParameters</span></span>
<span data-ttu-id="a5b57-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5b57-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b57-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5b57-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b57-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5b57-123">INPUTS</span></span>

### <span data-ttu-id="a5b57-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="a5b57-124">None</span></span>

## <span data-ttu-id="a5b57-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5b57-125">OUTPUTS</span></span>

### <span data-ttu-id="a5b57-126">Microsoft. Azure. Management. CognitiveServices. Models. CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="a5b57-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="a5b57-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5b57-127">NOTES</span></span>

## <span data-ttu-id="a5b57-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5b57-128">RELATED LINKS</span></span>
