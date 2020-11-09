---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317603"
---
# <span data-ttu-id="2537e-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="2537e-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="2537e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2537e-102">SYNOPSIS</span></span>
<span data-ttu-id="2537e-103">Получает список групп виртуальных машин и серверов для подписки на элементы управления приложением.</span><span class="sxs-lookup"><span data-stu-id="2537e-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2537e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2537e-104">SYNTAX</span></span>

### <span data-ttu-id="2537e-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2537e-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2537e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2537e-106">DESCRIPTION</span></span>
<span data-ttu-id="2537e-107">Адаптивные элементы управления приложениями автоматически рассчитываются центром безопасности Azure, используют этот командлет для получения списка ресурсов адаптивных элементов управления приложениями в области подписки.</span><span class="sxs-lookup"><span data-stu-id="2537e-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="2537e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2537e-108">EXAMPLES</span></span>

### <span data-ttu-id="2537e-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2537e-109">Example 1</span></span>
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
<span data-ttu-id="2537e-110">Получает список групп виртуальных машин и серверов для подписки на элементы управления приложением.</span><span class="sxs-lookup"><span data-stu-id="2537e-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="2537e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2537e-111">PARAMETERS</span></span>

### <span data-ttu-id="2537e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2537e-112">-DefaultProfile</span></span>
<span data-ttu-id="2537e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2537e-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2537e-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2537e-114">-SubscriptionId</span></span>
<span data-ttu-id="2537e-115">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="2537e-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="2537e-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="2537e-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="2537e-117">Включите правила политики.</span><span class="sxs-lookup"><span data-stu-id="2537e-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="2537e-118">-Сводка</span><span class="sxs-lookup"><span data-stu-id="2537e-118">-Summary</span></span>
<span data-ttu-id="2537e-119">Возвращение выходных данных в обобщенной форме.</span><span class="sxs-lookup"><span data-stu-id="2537e-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="2537e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2537e-120">CommonParameters</span></span>
<span data-ttu-id="2537e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2537e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2537e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2537e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2537e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2537e-123">INPUTS</span></span>

### <span data-ttu-id="2537e-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2537e-124">System.String</span></span>

### <span data-ttu-id="2537e-125">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2537e-125">System.Boolean</span></span>

## <span data-ttu-id="2537e-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2537e-126">OUTPUTS</span></span>

### <span data-ttu-id="2537e-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="2537e-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="2537e-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2537e-128">NOTES</span></span>

## <span data-ttu-id="2537e-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2537e-129">RELATED LINKS</span></span>
