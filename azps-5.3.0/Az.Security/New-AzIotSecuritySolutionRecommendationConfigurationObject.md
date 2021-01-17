---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionRecommendationConfigurationObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionRecommendationConfigurationObject.md
ms.openlocfilehash: 448b72ce068c29e357db69abb45420157c3c1bf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98420919"
---
# <span data-ttu-id="c2fe4-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="c2fe4-101">New-AzIotSecuritySolutionRecommendationConfigurationObject</span></span>

## <span data-ttu-id="c2fe4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fe4-103">Создание новой конфигурации рекомендации для решения для безопасности iOT</span><span class="sxs-lookup"><span data-stu-id="c2fe4-103">Create new recommendation configuration for iot security solution</span></span>

## <span data-ttu-id="c2fe4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2fe4-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType <String> -Enabled <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2fe4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="c2fe4-106">AzIotSecuritySolutionRecommendationConfigurationObject создает новый объект конфигурации рекомендации для решения безопасности iot.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-106">The AzIotSecuritySolutionRecommendationConfigurationObject creates a new recommendation configuration object for iot security solution.</span></span>
<span data-ttu-id="c2fe4-107">В этом случае состояние рекомендации будет настроено независимо от того, включена ли она.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-107">This way the status of a recommendation is configured, whether it is enabled or disabled.</span></span>

## <span data-ttu-id="c2fe4-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2fe4-108">EXAMPLES</span></span>

### <span data-ttu-id="c2fe4-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c2fe4-109">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionRecommendationConfigurationObject -RecommendationType "IoT_ACRAuthentication" -Enabled $false

RecommendationType: "IoT_ACRAuthentication"
Name: "Service prinicpal not used with ACR repository"
Status: "Disabled"
```

<span data-ttu-id="c2fe4-110">Создайте новую конфигурацию рекомендации для типа "IoT_ACRAuthentication" с состоянием, отключенным</span><span class="sxs-lookup"><span data-stu-id="c2fe4-110">Create new recommendation configuration for recommendation type "IoT_ACRAuthentication" with status set to disable</span></span>

## <span data-ttu-id="c2fe4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2fe4-111">PARAMETERS</span></span>

### <span data-ttu-id="c2fe4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fe4-112">-DefaultProfile</span></span>
<span data-ttu-id="c2fe4-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fe4-114">-Enabled</span><span class="sxs-lookup"><span data-stu-id="c2fe4-114">-Enabled</span></span>
<span data-ttu-id="c2fe4-115">Состояние.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-115">Status .</span></span>

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

### <span data-ttu-id="c2fe4-116">-RecommendationType</span><span class="sxs-lookup"><span data-stu-id="c2fe4-116">-RecommendationType</span></span>
<span data-ttu-id="c2fe4-117">Тип рекомендации.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-117">Recommendation type.</span></span>

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

### <span data-ttu-id="c2fe4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fe4-118">CommonParameters</span></span>
<span data-ttu-id="c2fe4-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2fe4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fe4-120">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2fe4-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fe4-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fe4-121">INPUTS</span></span>

### <span data-ttu-id="c2fe4-122">Нет</span><span class="sxs-lookup"><span data-stu-id="c2fe4-122">None</span></span>

## <span data-ttu-id="c2fe4-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2fe4-123">OUTPUTS</span></span>

### <span data-ttu-id="c2fe4-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span><span class="sxs-lookup"><span data-stu-id="c2fe4-124">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSRecommendationConfiguration</span></span>

## <span data-ttu-id="c2fe4-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2fe4-125">NOTES</span></span>

## <span data-ttu-id="c2fe4-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2fe4-126">RELATED LINKS</span></span>
