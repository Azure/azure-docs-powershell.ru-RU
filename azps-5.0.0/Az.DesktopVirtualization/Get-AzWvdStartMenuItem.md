---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/get-azwvdstartmenuitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Get-AzWvdStartMenuItem.md
ms.openlocfilehash: d4390f7de7b9fb91cf998050f192a3ba282e9585
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312569"
---
# <span data-ttu-id="735eb-101">Get-AzWvdStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="735eb-101">Get-AzWvdStartMenuItem</span></span>

## <span data-ttu-id="735eb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="735eb-102">SYNOPSIS</span></span>
<span data-ttu-id="735eb-103">Список элементов меню "Пуск" в заданной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="735eb-103">List start menu items in the given application group.</span></span>

## <span data-ttu-id="735eb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="735eb-104">SYNTAX</span></span>

```
Get-AzWvdStartMenuItem -ApplicationGroupName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="735eb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="735eb-105">DESCRIPTION</span></span>
<span data-ttu-id="735eb-106">Список элементов меню "Пуск" в заданной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="735eb-106">List start menu items in the given application group.</span></span>

## <span data-ttu-id="735eb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="735eb-107">EXAMPLES</span></span>

### <span data-ttu-id="735eb-108">Пример 2: список элементов меню «Пуск» для виртуальных рабочих столов Windows</span><span class="sxs-lookup"><span data-stu-id="735eb-108">Example 2: List Windows Virtual Desktop Start Menu Items</span></span>
```powershell
PS C:\> Get-AzWvdStartMenuItem -ResourceGroupName ResourceGroupName -ApplicationGroupName ApplicationGroupName

Name                                                Type
----                                                ----
ApplicationGroupName/Character Map                  Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Defragment and Optimize Drives Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Disk Cleanup                   Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
ApplicationGroupName/Internet Explorer              Microsoft.DesktopVirtualization/applicationgroups/startmenuitems
```

<span data-ttu-id="735eb-109">Эта команда перечисляет элементы меню Пуск виртуальных рабочих столов Windows в группе applicaton.</span><span class="sxs-lookup"><span data-stu-id="735eb-109">This command Lists Windows Virtual Desktop Start Menu Items in an applicaton Group.</span></span>

## <span data-ttu-id="735eb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="735eb-110">PARAMETERS</span></span>

### <span data-ttu-id="735eb-111">-ApplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="735eb-111">-ApplicationGroupName</span></span>
<span data-ttu-id="735eb-112">Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="735eb-112">The name of the application group</span></span>

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

### <span data-ttu-id="735eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="735eb-113">-DefaultProfile</span></span>
<span data-ttu-id="735eb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="735eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="735eb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="735eb-115">-ResourceGroupName</span></span>
<span data-ttu-id="735eb-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="735eb-116">The name of the resource group.</span></span>
<span data-ttu-id="735eb-117">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="735eb-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="735eb-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="735eb-118">-SubscriptionId</span></span>
<span data-ttu-id="735eb-119">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="735eb-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="735eb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="735eb-120">CommonParameters</span></span>
<span data-ttu-id="735eb-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="735eb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="735eb-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="735eb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="735eb-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="735eb-123">INPUTS</span></span>

## <span data-ttu-id="735eb-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="735eb-124">OUTPUTS</span></span>

### <span data-ttu-id="735eb-125">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IStartMenuItem</span><span class="sxs-lookup"><span data-stu-id="735eb-125">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IStartMenuItem</span></span>

## <span data-ttu-id="735eb-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="735eb-126">NOTES</span></span>

<span data-ttu-id="735eb-127">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="735eb-127">ALIASES</span></span>

## <span data-ttu-id="735eb-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="735eb-128">RELATED LINKS</span></span>

