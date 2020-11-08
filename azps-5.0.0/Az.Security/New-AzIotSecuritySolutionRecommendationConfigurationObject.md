---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246194"
---
# <span data-ttu-id="eacc4-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="eacc4-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="eacc4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eacc4-102">SYNOPSIS</span></span>
<span data-ttu-id="eacc4-103">Создание новой конфигурации рекомендации для решения для обеспечения безопасности IOT</span><span class="sxs-lookup"><span data-stu-id="eacc4-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="eacc4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eacc4-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eacc4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eacc4-105">DESCRIPTION</span></span>
<span data-ttu-id="eacc4-106">AzIotSecuritySolutionRecommendationConfigurationObject создает новый объект конфигурации рекомендации для решения для обеспечения безопасности IOT.</span><span class="sxs-lookup"><span data-stu-id="eacc4-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="eacc4-107">Таким образом, состояние рекомендации настраивается независимо от того, включена или отключена рекомендация.</span><span class="sxs-lookup"><span data-stu-id="eacc4-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="eacc4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eacc4-108">EXAMPLES</span></span>

### <span data-ttu-id="eacc4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eacc4-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="eacc4-110">Создание новой конфигурации рекомендации для типа рекомендации "IoT_ACRAuthentication" с состоянием "отключено"</span><span class="sxs-lookup"><span data-stu-id="eacc4-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="eacc4-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eacc4-111">PARAMETERS</span></span>

### <span data-ttu-id="eacc4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eacc4-112">-DefaultProfile</span></span>
<span data-ttu-id="eacc4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eacc4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacc4-114">-Включено</span><span class="sxs-lookup"><span data-stu-id="eacc4-114">-Enabled</span></span>
<span data-ttu-id="eacc4-115">Состояни.</span><span class="sxs-lookup"><span data-stu-id="eacc4-115">Status .</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacc4-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="eacc4-116">-RecommendationType</span></span>
<span data-ttu-id="eacc4-117">Тип рекомендации.</span><span class="sxs-lookup"><span data-stu-id="eacc4-117">Recommendation type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eacc4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eacc4-118">CommonParameters</span></span>
<span data-ttu-id="eacc4-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eacc4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eacc4-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eacc4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eacc4-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eacc4-121">INPUTS</span></span>

### <span data-ttu-id="eacc4-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="eacc4-122">None</span></span>

## <span data-ttu-id="eacc4-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eacc4-123">OUTPUTS</span></span>

### <span data-ttu-id="eacc4-124">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutions. PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="eacc4-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="eacc4-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="eacc4-125">NOTES</span></span>

## <span data-ttu-id="eacc4-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eacc4-126">RELATED LINKS</span></span>
