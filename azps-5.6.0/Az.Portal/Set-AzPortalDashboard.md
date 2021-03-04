---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 8002a0a38353022c273aa680ccae9cf354b3540d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988952"
---
# <span data-ttu-id="c05c0-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="c05c0-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="c05c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c05c0-102">SYNOPSIS</span></span>
<span data-ttu-id="c05c0-103">Создает или обновляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="c05c0-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="c05c0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c05c0-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c05c0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c05c0-105">DESCRIPTION</span></span>
<span data-ttu-id="c05c0-106">Создает или обновляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="c05c0-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="c05c0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c05c0-107">EXAMPLES</span></span>

### <span data-ttu-id="c05c0-108">Пример 1. Обновление определения панели мониторинга с помощью шаблона панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="c05c0-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="c05c0-109">Обновив определение панели мониторинга, можно использовать файл шаблона тире.</span><span class="sxs-lookup"><span data-stu-id="c05c0-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="c05c0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c05c0-110">PARAMETERS</span></span>

### <span data-ttu-id="c05c0-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="c05c0-111">-DashboardPath</span></span>
<span data-ttu-id="c05c0-112">Путь к существующему шаблону панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="c05c0-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="c05c0-113">Шаблоны панелей мониторинга можно скачать с портала.</span><span class="sxs-lookup"><span data-stu-id="c05c0-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="c05c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c05c0-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="c05c0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c05c0-115">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DashboardName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05c0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c05c0-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="c05c0-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c05c0-117">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05c0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c05c0-118">-Confirm</span></span>
<span data-ttu-id="c05c0-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c05c0-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05c0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c05c0-120">-WhatIf</span></span>
<span data-ttu-id="c05c0-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c05c0-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c05c0-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c05c0-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c05c0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c05c0-123">CommonParameters</span></span>
<span data-ttu-id="c05c0-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c05c0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c05c0-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c05c0-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c05c0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c05c0-126">INPUTS</span></span>

## <span data-ttu-id="c05c0-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c05c0-127">OUTPUTS</span></span>

### <span data-ttu-id="c05c0-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="c05c0-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="c05c0-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c05c0-129">NOTES</span></span>

<span data-ttu-id="c05c0-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c05c0-130">ALIASES</span></span>

## <span data-ttu-id="c05c0-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c05c0-131">RELATED LINKS</span></span>

