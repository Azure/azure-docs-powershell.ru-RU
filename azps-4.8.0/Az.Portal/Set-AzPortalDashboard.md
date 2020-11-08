---
external help file: ''
Module Name: Az.Portal
online version: https://docs.microsoft.com/en-us/powershell/module/az.portal/set-azportaldashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Portal/help/Set-AzPortalDashboard.md
ms.openlocfilehash: 60569a05fc3770119844b05e65ec3dc7989a85ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244291"
---
# <span data-ttu-id="503d6-101">Set-AzPortalDashboard</span><span class="sxs-lookup"><span data-stu-id="503d6-101">Set-AzPortalDashboard</span></span>

## <span data-ttu-id="503d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="503d6-102">SYNOPSIS</span></span>
<span data-ttu-id="503d6-103">Создание или обновление информационной панели.</span><span class="sxs-lookup"><span data-stu-id="503d6-103">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="503d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="503d6-104">SYNTAX</span></span>

```
Set-AzPortalDashboard -Name <String> -ResourceGroupName <String> -DashboardPath <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="503d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="503d6-105">DESCRIPTION</span></span>
<span data-ttu-id="503d6-106">Создание или обновление информационной панели.</span><span class="sxs-lookup"><span data-stu-id="503d6-106">Creates or updates a Dashboard.</span></span>

## <span data-ttu-id="503d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="503d6-107">EXAMPLES</span></span>

### <span data-ttu-id="503d6-108">Пример 1: обновление определения панели мониторинга с помощью шаблона панели мониторинга</span><span class="sxs-lookup"><span data-stu-id="503d6-108">Example 1: Update the dashboard definition using a dashboard template</span></span>
```powershell
PS C:\> Set-AzPortalDashboard -DashboardPath .\resources\dash1-update.json -ResourceGroupName my-rg -DashboardName dashbase03

Location Name       Type
-------- ----       ----
eastasia dashbase03 Microsoft.Portal/dashboards
```

<span data-ttu-id="503d6-109">Обновите определение панели мониторинга с помощью файла шаблона dashbaord.</span><span class="sxs-lookup"><span data-stu-id="503d6-109">Update a dashboard definition using a dashbaord template file.</span></span>

## <span data-ttu-id="503d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="503d6-110">PARAMETERS</span></span>

### <span data-ttu-id="503d6-111">-DashboardPath</span><span class="sxs-lookup"><span data-stu-id="503d6-111">-DashboardPath</span></span>
<span data-ttu-id="503d6-112">Путь к существующему шаблону панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="503d6-112">The Path to an existing dashboard template.</span></span>
<span data-ttu-id="503d6-113">Шаблоны панели мониторинга можно загрузить с портала.</span><span class="sxs-lookup"><span data-stu-id="503d6-113">Dashboard templates may be downloaded from the portal.</span></span>

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

### <span data-ttu-id="503d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="503d6-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="503d6-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="503d6-115">-Name</span></span>


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

### <span data-ttu-id="503d6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="503d6-116">-ResourceGroupName</span></span>


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

### <span data-ttu-id="503d6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="503d6-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="503d6-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="503d6-118">-Confirm</span></span>
<span data-ttu-id="503d6-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="503d6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="503d6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="503d6-120">-WhatIf</span></span>
<span data-ttu-id="503d6-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="503d6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="503d6-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="503d6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="503d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="503d6-123">CommonParameters</span></span>
<span data-ttu-id="503d6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="503d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="503d6-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="503d6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="503d6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="503d6-126">INPUTS</span></span>

## <span data-ttu-id="503d6-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="503d6-127">OUTPUTS</span></span>

### <span data-ttu-id="503d6-128">Microsoft. Azure. PowerShell. командлеты. Portal. Models. Api201901Preview. IDashboard</span><span class="sxs-lookup"><span data-stu-id="503d6-128">Microsoft.Azure.PowerShell.Cmdlets.Portal.Models.Api201901Preview.IDashboard</span></span>

## <span data-ttu-id="503d6-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="503d6-129">NOTES</span></span>

<span data-ttu-id="503d6-130">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="503d6-130">ALIASES</span></span>

## <span data-ttu-id="503d6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="503d6-131">RELATED LINKS</span></span>

