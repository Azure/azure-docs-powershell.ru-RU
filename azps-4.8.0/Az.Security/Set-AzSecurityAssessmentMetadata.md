---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessmentMetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessmentMetadata.md
ms.openlocfilehash: d65cd0a5f29f15d2d82227aad6520df34fd4357f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235354"
---
# <span data-ttu-id="63afe-101">Set-AzSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="63afe-101">Set-AzSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="63afe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63afe-102">SYNOPSIS</span></span>
<span data-ttu-id="63afe-103">Создание или обновление типа оценки безопасности.</span><span class="sxs-lookup"><span data-stu-id="63afe-103">Creates or updates a security assessment type.</span></span>

## <span data-ttu-id="63afe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63afe-104">SYNTAX</span></span>

```
Set-AzSecurityAssessmentMetadata -Name <String> -DisplayName <String> [-Description <String>]
 [-RemediationDescription <String>] [-Severity <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63afe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63afe-105">DESCRIPTION</span></span>
<span data-ttu-id="63afe-106">Создание или обновление метаданных оценки безопасности, которое можно использовать для создания различных свойств оценки и управления ими.</span><span class="sxs-lookup"><span data-stu-id="63afe-106">Creates or updates a security assessment metadata, can be used to create and manage various assessment properties.</span></span>
<span data-ttu-id="63afe-107">После этого вы сможете получать отчеты о результатах оценки по любому ресурсу в этой подписке.</span><span class="sxs-lookup"><span data-stu-id="63afe-107">After this action you will be able to report assessment results on any resource in this subscription.</span></span>

## <span data-ttu-id="63afe-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63afe-108">EXAMPLES</span></span>

### <span data-ttu-id="63afe-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63afe-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessmentMetadata -Name $assessmentGuid -DisplayName "Resource should be secured" -Severity "High" -Description "The resource should be secured according to my company's security policy"
```

<span data-ttu-id="63afe-110">Создание нового типа оценки в подписке.</span><span class="sxs-lookup"><span data-stu-id="63afe-110">Create a new assessment type in a subscription.</span></span>

## <span data-ttu-id="63afe-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63afe-111">PARAMETERS</span></span>

### <span data-ttu-id="63afe-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63afe-112">-DefaultProfile</span></span>
<span data-ttu-id="63afe-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63afe-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63afe-114">-Описание</span><span class="sxs-lookup"><span data-stu-id="63afe-114">-Description</span></span>
<span data-ttu-id="63afe-115">Подробное описание строки, которая поможет пользователям понять смысл этой оценки и способ ее вычисления.</span><span class="sxs-lookup"><span data-stu-id="63afe-115">Detailed string that will help users to understand the meaning of this assessment and how it was calculated.</span></span>

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

### <span data-ttu-id="63afe-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="63afe-116">-DisplayName</span></span>
<span data-ttu-id="63afe-117">Удобное для чтения название объекта.</span><span class="sxs-lookup"><span data-stu-id="63afe-117">Human readable title for this object.</span></span>

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

### <span data-ttu-id="63afe-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63afe-118">-Name</span></span>
<span data-ttu-id="63afe-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="63afe-119">Resource name.</span></span>

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

### <span data-ttu-id="63afe-120">-RemediationDescription</span><span class="sxs-lookup"><span data-stu-id="63afe-120">-RemediationDescription</span></span>
<span data-ttu-id="63afe-121">Подробное описание строки, которая поможет пользователям понять различные способы устранения и устранения проблем с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="63afe-121">Detailed string that will help users to understand the different ways to mitigate or fix the security issue.</span></span>

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

### <span data-ttu-id="63afe-122">-Серьезность</span><span class="sxs-lookup"><span data-stu-id="63afe-122">-Severity</span></span>
<span data-ttu-id="63afe-123">Указывает важность риска нарушения безопасности в случае неработоспособности оценки.</span><span class="sxs-lookup"><span data-stu-id="63afe-123">Indicates the importance of the security risk if the assessment is unhealthy.</span></span>

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

### <span data-ttu-id="63afe-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63afe-124">-Confirm</span></span>
<span data-ttu-id="63afe-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63afe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63afe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63afe-126">-WhatIf</span></span>
<span data-ttu-id="63afe-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63afe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63afe-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63afe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63afe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63afe-129">CommonParameters</span></span>
<span data-ttu-id="63afe-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63afe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63afe-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63afe-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63afe-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63afe-132">INPUTS</span></span>

### <span data-ttu-id="63afe-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="63afe-133">None</span></span>

## <span data-ttu-id="63afe-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63afe-134">OUTPUTS</span></span>

### <span data-ttu-id="63afe-135">Microsoft. Azure. Commands. Security. Models. AssessmentMetadata. PSSecurityAssessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="63afe-135">Microsoft.Azure.Commands.Security.Models.AssessmentMetadata.PSSecurityAssessmentMetadata</span></span>

## <span data-ttu-id="63afe-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="63afe-136">NOTES</span></span>

## <span data-ttu-id="63afe-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63afe-137">RELATED LINKS</span></span>