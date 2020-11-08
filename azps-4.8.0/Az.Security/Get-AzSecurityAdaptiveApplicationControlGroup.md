---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077641"
---
# <span data-ttu-id="3c344-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="3c344-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="3c344-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c344-102">SYNOPSIS</span></span>
<span data-ttu-id="3c344-103">Возвращает группу ВМ или сервера управления приложением.</span><span class="sxs-lookup"><span data-stu-id="3c344-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="3c344-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c344-104">SYNTAX</span></span>

### <span data-ttu-id="3c344-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c344-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c344-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c344-106">DESCRIPTION</span></span>
<span data-ttu-id="3c344-107">Адаптивные элементы управления приложениями автоматически рассчитываются центром безопасности Azure, используют этот командлет, чтобы получить группу "виртуальная машина/сервер" для управления приложением.</span><span class="sxs-lookup"><span data-stu-id="3c344-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="3c344-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c344-108">EXAMPLES</span></span>

### <span data-ttu-id="3c344-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3c344-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="3c344-110">Возвращает группу ВМ или сервера управления приложением.</span><span class="sxs-lookup"><span data-stu-id="3c344-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="3c344-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c344-111">PARAMETERS</span></span>

### <span data-ttu-id="3c344-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c344-112">-DefaultProfile</span></span>
<span data-ttu-id="3c344-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c344-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c344-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="3c344-114">-AscLocation</span></span>
<span data-ttu-id="3c344-115">Расположение, в котором ASC хранит данные о подписке.</span><span class="sxs-lookup"><span data-stu-id="3c344-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="3c344-116">может извлекаться из папки Get.</span><span class="sxs-lookup"><span data-stu-id="3c344-116">can be retrieved from Get locations.</span></span>

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

### <span data-ttu-id="3c344-117">-Имя_группы</span><span class="sxs-lookup"><span data-stu-id="3c344-117">-GroupName</span></span>
<span data-ttu-id="3c344-118">Имя группы "VM" или "сервер" для управления приложением.</span><span class="sxs-lookup"><span data-stu-id="3c344-118">Name of an application control VM/server group.</span></span>

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

### <span data-ttu-id="3c344-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c344-119">-SubscriptionId</span></span>
<span data-ttu-id="3c344-120">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="3c344-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="3c344-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c344-121">CommonParameters</span></span>
<span data-ttu-id="3c344-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c344-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c344-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c344-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c344-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c344-124">INPUTS</span></span>

### <span data-ttu-id="3c344-125">System. String</span><span class="sxs-lookup"><span data-stu-id="3c344-125">System.String</span></span>

## <span data-ttu-id="3c344-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c344-126">OUTPUTS</span></span>

### <span data-ttu-id="3c344-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="3c344-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="3c344-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c344-128">NOTES</span></span>

## <span data-ttu-id="3c344-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c344-129">RELATED LINKS</span></span>