---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391959"
---
# <span data-ttu-id="a0cc7-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="a0cc7-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="a0cc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0cc7-102">SYNOPSIS</span></span>
<span data-ttu-id="a0cc7-103">Создает или обновляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a0cc7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0cc7-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0cc7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0cc7-105">DESCRIPTION</span></span>
<span data-ttu-id="a0cc7-106">Создает или обновляет информационную панель.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="a0cc7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0cc7-107">EXAMPLES</span></span>

### <span data-ttu-id="a0cc7-108">Пример 1. Обновление определения панели мониторинга с помощью шаблона панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="a0cc7-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="a0cc7-109">Обновив определение панели мониторинга, можно использовать файл шаблона тире.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="a0cc7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0cc7-110">PARAMETERS</span></span>

### <span data-ttu-id="a0cc7-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="a0cc7-111">-DashboardPath</span></span>
<span data-ttu-id="a0cc7-112">Путь к существующему шаблону панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="a0cc7-113">Шаблоны панелей мониторинга можно скачать с портала.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="a0cc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0cc7-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="a0cc7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a0cc7-115">-Name</span></span>


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

### <span data-ttu-id="a0cc7-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0cc7-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="a0cc7-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a0cc7-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="a0cc7-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0cc7-118">-Confirm</span></span>
<span data-ttu-id="a0cc7-119">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0cc7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0cc7-120">-WhatIf</span></span>
<span data-ttu-id="a0cc7-121">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0cc7-122">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0cc7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0cc7-123">CommonParameters</span></span>
<span data-ttu-id="a0cc7-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0cc7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0cc7-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0cc7-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0cc7-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0cc7-126">INPUTS</span></span>

## <span data-ttu-id="a0cc7-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0cc7-127">OUTPUTS</span></span>

### <span data-ttu-id="a0cc7-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span><span class="sxs-lookup"><span data-stu-id="a0cc7-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="a0cc7-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0cc7-129">NOTES</span></span>

<span data-ttu-id="a0cc7-130">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a0cc7-130">ALIASES</span></span>

## <span data-ttu-id="a0cc7-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0cc7-131">RELATED LINKS</span></span>

