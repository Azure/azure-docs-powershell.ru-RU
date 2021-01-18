---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517741"
---
# <span data-ttu-id="5d2a5-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="5d2a5-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="5d2a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d2a5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2a5-103">Возвращает список групп VM-серверов и управления приложениями для подписки.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="5d2a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d2a5-104">SYNTAX</span></span>

### <span data-ttu-id="5d2a5-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d2a5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d2a5-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d2a5-106">DESCRIPTION</span></span>
<span data-ttu-id="5d2a5-107">Адаптивные элементы управления приложениями автоматически вычисляются Центром безопасности Azure. Используйте этот cmdlet, чтобы получить список ресурсов, адаптивных элементов управления приложениями, которые находятся в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="5d2a5-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d2a5-108">EXAMPLES</span></span>

### <span data-ttu-id="5d2a5-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d2a5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="5d2a5-110">Возвращает список групп VM-серверов и управления приложениями для подписки.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="5d2a5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d2a5-111">PARAMETERS</span></span>

### <span data-ttu-id="5d2a5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2a5-112">-DefaultProfile</span></span>
<span data-ttu-id="5d2a5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d2a5-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d2a5-114">-SubscriptionId</span></span>
<span data-ttu-id="5d2a5-115">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2a5-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="5d2a5-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="5d2a5-117">Включив правила политики.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2a5-118">-Summary (Сводка)</span><span class="sxs-lookup"><span data-stu-id="5d2a5-118">-Summary</span></span>
<span data-ttu-id="5d2a5-119">Возвращает выходные данные в обобщенной форме.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2a5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2a5-120">CommonParameters</span></span>
<span data-ttu-id="5d2a5-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d2a5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2a5-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2a5-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2a5-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d2a5-123">INPUTS</span></span>

### <span data-ttu-id="5d2a5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="5d2a5-124">System.String</span></span>

### <span data-ttu-id="5d2a5-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d2a5-125">System.Boolean</span></span>

## <span data-ttu-id="5d2a5-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d2a5-126">OUTPUTS</span></span>

### <span data-ttu-id="5d2a5-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="5d2a5-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="5d2a5-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d2a5-128">NOTES</span></span>

## <span data-ttu-id="5d2a5-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d2a5-129">RELATED LINKS</span></span>
