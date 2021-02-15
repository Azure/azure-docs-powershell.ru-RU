---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: fd91ea79cbad51d03c0986ed5f55601af240de16
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230521"
---
# <span data-ttu-id="e62a3-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="e62a3-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="e62a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e62a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e62a3-103">Элементы меню "Пуск" списка в заданной группе приложений.</span><span class="sxs-lookup"><span data-stu-id="e62a3-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="e62a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e62a3-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e62a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e62a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e62a3-106">Элементы меню "Пуск" списка в заданной группе приложений.</span><span class="sxs-lookup"><span data-stu-id="e62a3-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="e62a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e62a3-107">EXAMPLES</span></span>

### <span data-ttu-id="e62a3-108">Пример 2. Список элементов меню "Пуск" виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="e62a3-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="e62a3-109">Эта команда содержит список элементов меню "Пуск" виртуального рабочего стола Windows в соответствующей группе.</span><span class="sxs-lookup"><span data-stu-id="e62a3-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="e62a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e62a3-110">PARAMETERS</span></span>

### <span data-ttu-id="e62a3-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="e62a3-111">-ApplicationGroupName</span></span>
<span data-ttu-id="e62a3-112">Имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="e62a3-112">The name of the application group</span></span>

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

### <span data-ttu-id="e62a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62a3-113">-DefaultProfile</span></span>
<span data-ttu-id="e62a3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e62a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e62a3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e62a3-115">-ResourceGroupName</span></span>
<span data-ttu-id="e62a3-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e62a3-116">The name of the resource group.</span></span>
<span data-ttu-id="e62a3-117">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="e62a3-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="e62a3-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e62a3-118">-SubscriptionId</span></span>
<span data-ttu-id="e62a3-119">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="e62a3-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="e62a3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62a3-120">CommonParameters</span></span>
<span data-ttu-id="e62a3-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62a3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62a3-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e62a3-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62a3-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e62a3-123">INPUTS</span></span>

## <span data-ttu-id="e62a3-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e62a3-124">OUTPUTS</span></span>

### <span data-ttu-id="e62a3-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="e62a3-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IStartMenuItem</span></span>

## <span data-ttu-id="e62a3-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e62a3-126">NOTES</span></span>

<span data-ttu-id="e62a3-127">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e62a3-127">ALIASES</span></span>

## <span data-ttu-id="e62a3-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e62a3-128">RELATED LINKS</span></span>

