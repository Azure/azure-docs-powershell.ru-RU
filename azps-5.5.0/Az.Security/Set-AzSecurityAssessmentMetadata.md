---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242293"
---
# <span data-ttu-id="53144-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="53144-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="53144-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53144-102">SYNOPSIS</span></span>
<span data-ttu-id="53144-103">Создание или обновление типа оценки безопасности.</span><span class="sxs-lookup"><span data-stu-id="53144-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="53144-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="53144-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53144-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53144-105">DESCRIPTION</span></span>
<span data-ttu-id="53144-106">Создание или обновление метаданных оценки безопасности, которые можно использовать для создания различных свойств оценки и управления ими.</span><span class="sxs-lookup"><span data-stu-id="53144-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="53144-107">После этого действия вы сможете сообщать о результатах оценки по любому ресурсу в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="53144-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="53144-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="53144-108">EXAMPLES</span></span>

### <span data-ttu-id="53144-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="53144-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="53144-110">Создайте новый тип оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="53144-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="53144-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53144-111">PARAMETERS</span></span>

### <span data-ttu-id="53144-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53144-112">-DefaultProfile</span></span>
<span data-ttu-id="53144-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53144-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53144-114">-Description</span><span class="sxs-lookup"><span data-stu-id="53144-114">-Description</span></span>
<span data-ttu-id="53144-115">Подробная строка, которая поможет пользователям понять значение этой оценки и ее расчет.</span><span class="sxs-lookup"><span data-stu-id="53144-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="53144-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="53144-116">-DisplayName</span></span>
<span data-ttu-id="53144-117">Понятное название объекта.</span><span class="sxs-lookup"><span data-stu-id="53144-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="53144-118">-Name</span><span class="sxs-lookup"><span data-stu-id="53144-118">-Name</span></span>
<span data-ttu-id="53144-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="53144-119">Resource name.</span></span>

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

### <span data-ttu-id="53144-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="53144-120">-RemediationDescription</span></span>
<span data-ttu-id="53144-121">Подробная строка, которая поможет пользователям понять, как устранять и устранять проблемы с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="53144-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="53144-122">-Severity</span><span class="sxs-lookup"><span data-stu-id="53144-122">-Severity</span></span>
<span data-ttu-id="53144-123">Указывает на важность риска безопасности, если оценка неработоспособна.</span><span class="sxs-lookup"><span data-stu-id="53144-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="53144-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53144-124">-Confirm</span></span>
<span data-ttu-id="53144-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53144-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53144-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53144-126">-WhatIf</span></span>
<span data-ttu-id="53144-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53144-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53144-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="53144-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53144-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53144-129">CommonParameters</span></span>
<span data-ttu-id="53144-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53144-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53144-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53144-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53144-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="53144-132">INPUTS</span></span>

### <span data-ttu-id="53144-133">Нет</span><span class="sxs-lookup"><span data-stu-id="53144-133">None</span></span>

## <span data-ttu-id="53144-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="53144-134">OUTPUTS</span></span>

### <span data-ttu-id="53144-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="53144-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="53144-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="53144-136">NOTES</span></span>

## <span data-ttu-id="53144-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53144-137">RELATED LINKS</span></span>
