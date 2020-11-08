---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243444"
---
# <span data-ttu-id="6c0e6-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="6c0e6-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="6c0e6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6c0e6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c0e6-103">Создание или обновление политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="6c0e6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6c0e6-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6c0e6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c0e6-105">DESCRIPTION</span></span>
<span data-ttu-id="6c0e6-106">Создание или обновление политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="6c0e6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6c0e6-107">EXAMPLES</span></span>

### <span data-ttu-id="6c0e6-108">Пример 1: Создание политики доступа для указанной среды</span><span class="sxs-lookup"><span data-stu-id="6c0e6-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="6c0e6-109">Эта команда создает политику доступа для указанной среды.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="6c0e6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6c0e6-110">PARAMETERS</span></span>

### <span data-ttu-id="6c0e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c0e6-111">-DefaultProfile</span></span>
<span data-ttu-id="6c0e6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c0e6-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="6c0e6-113">-Description</span></span>
<span data-ttu-id="6c0e6-114">Описание политики доступа.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-114">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e6-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="6c0e6-115">-EnvironmentName</span></span>
<span data-ttu-id="6c0e6-116">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="6c0e6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6c0e6-117">-Name</span></span>
<span data-ttu-id="6c0e6-118">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e6-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="6c0e6-119">-PrincipalObjectId</span></span>
<span data-ttu-id="6c0e6-120">ObjectId участника в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-120">The objectId of the principal in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c0e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="6c0e6-122">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="6c0e6-123">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="6c0e6-123">-Role</span></span>
<span data-ttu-id="6c0e6-124">Список ролей, назначаемых участником в среде.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c0e6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6c0e6-125">-SubscriptionId</span></span>
<span data-ttu-id="6c0e6-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="6c0e6-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6c0e6-127">-Confirm</span></span>
<span data-ttu-id="6c0e6-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c0e6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c0e6-129">-WhatIf</span></span>
<span data-ttu-id="6c0e6-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c0e6-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c0e6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c0e6-132">CommonParameters</span></span>
<span data-ttu-id="6c0e6-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6c0e6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c0e6-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c0e6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c0e6-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6c0e6-135">INPUTS</span></span>

## <span data-ttu-id="6c0e6-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6c0e6-136">OUTPUTS</span></span>

### <span data-ttu-id="6c0e6-137">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="6c0e6-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="6c0e6-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="6c0e6-138">NOTES</span></span>

<span data-ttu-id="6c0e6-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6c0e6-139">ALIASES</span></span>

## <span data-ttu-id="6c0e6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6c0e6-140">RELATED LINKS</span></span>

