---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccountapiproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccountApiProperty.md
ms.openlocfilehash: 97cf393d0d95dbc9ecfec06f53795713f59aecbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98390879"
---
# <span data-ttu-id="4b417-101">New-AzCognitiveServicesAccountApiProperty</span><span class="sxs-lookup"><span data-stu-id="4b417-101">New-AzCognitiveServicesAccountApiProperty</span></span>

## <span data-ttu-id="4b417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b417-102">SYNOPSIS</span></span>
<span data-ttu-id="4b417-103">Создание нового экземпляра API-свойств учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="4b417-103">Generate a new instance of Cognitive Services Account ApiProperties</span></span>

## <span data-ttu-id="4b417-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b417-104">SYNTAX</span></span>

```
New-AzCognitiveServicesAccountApiProperty [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b417-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b417-105">DESCRIPTION</span></span>
<span data-ttu-id="4b417-106">Создание нового экземпляра API-свойств учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="4b417-106">Generate a new instance of Cognitive Services Account ApiProperties.</span></span>
<span data-ttu-id="4b417-107">Свойства API можно использовать при создании или обновлении существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="4b417-107">ApiProperties can be used when creating a new account or updating an existing account.</span></span>
<span data-ttu-id="4b417-108">Свойства API требуются для определенных типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4b417-108">ApiProperties is required by certain account types.</span></span>

## <span data-ttu-id="4b417-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b417-109">EXAMPLES</span></span>

### <span data-ttu-id="4b417-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b417-110">Example 1</span></span>
```powershell
PS C:\> $apiProperties = New-AzCognitiveServicesAccountApiProperty
PS C:\> $apiProperties.QnaRuntimeEndpoint = "https://qnamaker.azurewebsites.net"
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name qnamaker -Type QnAMaker -SkuName S0 -Locatio WestUS -ApiProperty $apiProperties
```

<span data-ttu-id="4b417-111">В примере выше будет создаваться учетная запись QnAMaker со свойством API "QnaRuntimeEndpoint".</span><span class="sxs-lookup"><span data-stu-id="4b417-111">Above example will create an QnAMaker account, with API property "QnaRuntimeEndpoint".</span></span>


## <span data-ttu-id="4b417-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b417-112">PARAMETERS</span></span>

### <span data-ttu-id="4b417-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b417-113">-DefaultProfile</span></span>
<span data-ttu-id="4b417-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b417-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b417-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b417-115">-Confirm</span></span>
<span data-ttu-id="4b417-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b417-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b417-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b417-117">-WhatIf</span></span>
<span data-ttu-id="4b417-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b417-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b417-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4b417-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b417-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b417-120">CommonParameters</span></span>
<span data-ttu-id="4b417-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b417-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b417-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b417-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b417-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b417-123">INPUTS</span></span>

### <span data-ttu-id="4b417-124">Нет</span><span class="sxs-lookup"><span data-stu-id="4b417-124">None</span></span>

## <span data-ttu-id="4b417-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b417-125">OUTPUTS</span></span>

### <span data-ttu-id="4b417-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span><span class="sxs-lookup"><span data-stu-id="4b417-126">Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties</span></span>

## <span data-ttu-id="4b417-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b417-127">NOTES</span></span>

## <span data-ttu-id="4b417-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b417-128">RELATED LINKS</span></span>
