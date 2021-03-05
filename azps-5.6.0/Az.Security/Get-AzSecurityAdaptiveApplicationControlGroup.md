---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: c23c04a5a9df3464bd84a2261435c744374cfb3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011731"
---
# <span data-ttu-id="5cf49-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="5cf49-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="5cf49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cf49-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf49-103">Получает управление приложением VM/server group.</span><span class="sxs-lookup"><span data-stu-id="5cf49-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="5cf49-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cf49-104">SYNTAX</span></span>

### <span data-ttu-id="5cf49-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5cf49-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cf49-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cf49-106">DESCRIPTION</span></span>
<span data-ttu-id="5cf49-107">Адаптивные элементы управления приложениями автоматически вычисляются Центром безопасности Azure. Используйте этот cmdlet для получения управления приложениями VM/server group.</span><span class="sxs-lookup"><span data-stu-id="5cf49-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="5cf49-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cf49-108">EXAMPLES</span></span>

### <span data-ttu-id="5cf49-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cf49-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="5cf49-110">Получает управление приложением VM/server group.</span><span class="sxs-lookup"><span data-stu-id="5cf49-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="5cf49-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cf49-111">PARAMETERS</span></span>

### <span data-ttu-id="5cf49-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf49-112">-DefaultProfile</span></span>
<span data-ttu-id="5cf49-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf49-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf49-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="5cf49-114">-AscLocation</span></span>
<span data-ttu-id="5cf49-115">Расположение, в котором ASC хранит данные подписки.</span><span class="sxs-lookup"><span data-stu-id="5cf49-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="5cf49-116">можно получить из расположения "Получить".</span><span class="sxs-lookup"><span data-stu-id="5cf49-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf49-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="5cf49-117">-GroupName</span></span>
<span data-ttu-id="5cf49-118">Имя группы VM-сервера или управления приложениями.</span><span class="sxs-lookup"><span data-stu-id="5cf49-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf49-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cf49-119">-SubscriptionId</span></span>
<span data-ttu-id="5cf49-120">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="5cf49-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="5cf49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf49-121">CommonParameters</span></span>
<span data-ttu-id="5cf49-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf49-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf49-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf49-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cf49-124">INPUTS</span></span>

### <span data-ttu-id="5cf49-125">System.String</span><span class="sxs-lookup"><span data-stu-id="5cf49-125">System.String</span></span>

## <span data-ttu-id="5cf49-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cf49-126">OUTPUTS</span></span>

### <span data-ttu-id="5cf49-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="5cf49-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="5cf49-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cf49-128">NOTES</span></span>

## <span data-ttu-id="5cf49-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cf49-129">RELATED LINKS</span></span>