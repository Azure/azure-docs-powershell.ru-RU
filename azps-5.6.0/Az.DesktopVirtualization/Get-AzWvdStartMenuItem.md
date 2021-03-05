---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: a2db8d344628d8a421623cd5e6348db31a7321ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980563"
---
# <span data-ttu-id="c5e5c-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="c5e5c-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="c5e5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5e5c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5e5c-103">Элементы меню "Пуск" списка в заданной группе приложений.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="c5e5c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c5e5c-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c5e5c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5e5c-105">DESCRIPTION</span></span>
<span data-ttu-id="c5e5c-106">Элементы меню "Пуск" списка в заданной группе приложений.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="c5e5c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c5e5c-107">EXAMPLES</span></span>

### <span data-ttu-id="c5e5c-108">Пример 2. Список элементов меню "Пуск" виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="c5e5c-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="c5e5c-109">Эта команда содержит список элементов меню "Пуск" виртуального рабочего стола Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="c5e5c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5e5c-110">PARAMETERS</span></span>

### <span data-ttu-id="c5e5c-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e5c-111">-ApplicationGroupName</span></span>
<span data-ttu-id="c5e5c-112">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="c5e5c-112">The name of the application group</span></span>

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

### <span data-ttu-id="c5e5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5e5c-113">-DefaultProfile</span></span>
<span data-ttu-id="c5e5c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e5c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5e5c-115">-ResourceGroupName</span></span>
<span data-ttu-id="c5e5c-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-116">The name of the resource group.</span></span>
<span data-ttu-id="c5e5c-117">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c5e5c-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c5e5c-118">-SubscriptionId</span></span>
<span data-ttu-id="c5e5c-119">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5e5c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5e5c-120">CommonParameters</span></span>
<span data-ttu-id="c5e5c-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5e5c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5e5c-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c5e5c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5e5c-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e5c-123">INPUTS</span></span>

## <span data-ttu-id="c5e5c-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c5e5c-124">OUTPUTS</span></span>

### <span data-ttu-id="c5e5c-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="c5e5c-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="c5e5c-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c5e5c-126">NOTES</span></span>

<span data-ttu-id="c5e5c-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c5e5c-127">ALIASES</span></span>

## <span data-ttu-id="c5e5c-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5e5c-128">RELATED LINKS</span></span>

