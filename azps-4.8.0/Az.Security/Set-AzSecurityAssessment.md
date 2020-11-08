---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAssessment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAssessment.md
ms.openlocfilehash: 9a227c742892d94417d42be7137f903e17b8b928
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235351"
---
# <span data-ttu-id="fe255-101">Set-AzSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="fe255-101">Set-AzSecurityAssessment</span></span>

## <span data-ttu-id="fe255-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe255-102">SYNOPSIS</span></span>
<span data-ttu-id="fe255-103">Создание или обновление результатов оценки системы безопасности для ресурса</span><span class="sxs-lookup"><span data-stu-id="fe255-103">Create or update a security assessment result on a resource</span></span>

## <span data-ttu-id="fe255-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe255-104">SYNTAX</span></span>

### <span data-ttu-id="fe255-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe255-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAssessment -Name <String> [-StatusCode <String>] [-StatusCause <String>]
 [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe255-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="fe255-106">ResourceIdLevelResource</span></span>
```
Set-AzSecurityAssessment -Name <String> -AssessedResourceId <String> -StatusCode <String>
 [-StatusCause <String>] [-StatusDescription <String>]
 [-AdditionalData <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe255-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe255-107">DESCRIPTION</span></span>
<span data-ttu-id="fe255-108">Создание или обновление результатов оценки системы безопасности для ресурса можно использовать для изменения состояния существующего результата или добавления дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="fe255-108">Create or update a security assessment result on a resource, can be used to change the status of an existing result or add additional data.</span></span>
<span data-ttu-id="fe255-109">можно использовать только для типов оценки "CustomerManaged" и только после создания сопоставленных метаданных оценки.</span><span class="sxs-lookup"><span data-stu-id="fe255-109">can only be used for "CustomerManaged" assessment types and only after the matched assessment metadata is created.</span></span>

## <span data-ttu-id="fe255-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe255-110">EXAMPLES</span></span>

### <span data-ttu-id="fe255-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe255-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAssessment -Name 4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D -StatusCode "Unhealthy"
```

<span data-ttu-id="fe255-112">Помечает результат подписки как "неработоспособный" для оценки типа "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" — Дополнительные сведения о типе оценки будут обнаружены в типе assessmentMetadata</span><span class="sxs-lookup"><span data-stu-id="fe255-112">Marks the subscription result as "Unhealthy" for assessment of type "4FB6C0A0-1137-42C7-A1C7-4BD37C91DE8D" - more details about the assessment type will be found under the assessmentMetadata type</span></span>

## <span data-ttu-id="fe255-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe255-113">PARAMETERS</span></span>

### <span data-ttu-id="fe255-114">-AdditionalData</span><span class="sxs-lookup"><span data-stu-id="fe255-114">-AdditionalData</span></span>
<span data-ttu-id="fe255-115">Данные, вложенные в результат оценки для более качественного исследования или ясности состояния.</span><span class="sxs-lookup"><span data-stu-id="fe255-115">Data that is attached to the assessment result for better investigations or status clarity.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe255-116">-AssessedResourceId</span><span class="sxs-lookup"><span data-stu-id="fe255-116">-AssessedResourceId</span></span>
<span data-ttu-id="fe255-117">Полный идентификатор ресурса, для которого рассчитывается оценка.</span><span class="sxs-lookup"><span data-stu-id="fe255-117">Full resource ID of the resource that the assessment is calculated on.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe255-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe255-118">-DefaultProfile</span></span>
<span data-ttu-id="fe255-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe255-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe255-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe255-120">-Name</span></span>
<span data-ttu-id="fe255-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe255-121">Resource name.</span></span>

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

### <span data-ttu-id="fe255-122">-StatusCause</span><span class="sxs-lookup"><span data-stu-id="fe255-122">-StatusCause</span></span>
<span data-ttu-id="fe255-123">Progremmatic код причины, по которой выводятся результаты оценки.</span><span class="sxs-lookup"><span data-stu-id="fe255-123">Progremmatic code for the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="fe255-124">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="fe255-124">-StatusCode</span></span>
<span data-ttu-id="fe255-125">Progremmatic код для результата оценки.</span><span class="sxs-lookup"><span data-stu-id="fe255-125">Progremmatic code for the result of the assessment.</span></span>
<span data-ttu-id="fe255-126">может быть "Исправен", "неисправен" или "NotApplicable"</span><span class="sxs-lookup"><span data-stu-id="fe255-126">can be "Healthy", "Unhealthy" or "NotApplicable"</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe255-127">-StatusDescription</span><span class="sxs-lookup"><span data-stu-id="fe255-127">-StatusDescription</span></span>
<span data-ttu-id="fe255-128">Понятное описание причины результата оценки.</span><span class="sxs-lookup"><span data-stu-id="fe255-128">Human readable description of the cause of the assessment's result.</span></span>

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

### <span data-ttu-id="fe255-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe255-129">-Confirm</span></span>
<span data-ttu-id="fe255-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe255-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe255-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe255-131">-WhatIf</span></span>
<span data-ttu-id="fe255-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe255-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe255-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe255-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe255-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe255-134">CommonParameters</span></span>
<span data-ttu-id="fe255-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe255-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe255-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe255-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe255-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe255-137">INPUTS</span></span>

### <span data-ttu-id="fe255-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="fe255-138">None</span></span>

## <span data-ttu-id="fe255-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe255-139">OUTPUTS</span></span>

### <span data-ttu-id="fe255-140">Microsoft. Azure. Commands. Security. Models. оценивающие. PSSecurityAssessment</span><span class="sxs-lookup"><span data-stu-id="fe255-140">Microsoft.Azure.Commands.Security.Models.Assessments.PSSecurityAssessment</span></span>

## <span data-ttu-id="fe255-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe255-141">NOTES</span></span>

## <span data-ttu-id="fe255-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe255-142">RELATED LINKS</span></span>
