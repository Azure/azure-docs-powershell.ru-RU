---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249280"
---
# <span data-ttu-id="bc3b2-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="bc3b2-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="bc3b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bc3b2-102">SYNOPSIS</span></span>
<span data-ttu-id="bc3b2-103">Создание или обновление политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="bc3b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bc3b2-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bc3b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc3b2-105">DESCRIPTION</span></span>
<span data-ttu-id="bc3b2-106">Создание или обновление политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="bc3b2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bc3b2-107">EXAMPLES</span></span>

### <span data-ttu-id="bc3b2-108">Пример 1: Создание политики доступа для указанной среды</span><span class="sxs-lookup"><span data-stu-id="bc3b2-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="bc3b2-109">Эта команда создает политику доступа для указанной среды.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="bc3b2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bc3b2-110">PARAMETERS</span></span>

### <span data-ttu-id="bc3b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc3b2-111">-DefaultProfile</span></span>
<span data-ttu-id="bc3b2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc3b2-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="bc3b2-113">-Description</span></span>
<span data-ttu-id="bc3b2-114">Описание политики доступа.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="bc3b2-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="bc3b2-115">-EnvironmentName</span></span>
<span data-ttu-id="bc3b2-116">Название среды "анализ временной последовательности", связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="bc3b2-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bc3b2-117">-Name</span></span>
<span data-ttu-id="bc3b2-118">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="bc3b2-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="bc3b2-119">-PrincipalObjectId</span></span>
<span data-ttu-id="bc3b2-120">ObjectId участника в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="bc3b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc3b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="bc3b2-122">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="bc3b2-123">-Role (роль)</span><span class="sxs-lookup"><span data-stu-id="bc3b2-123">-Role</span></span>
<span data-ttu-id="bc3b2-124">Список ролей, назначаемых участником в среде.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="bc3b2-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc3b2-125">-SubscriptionId</span></span>
<span data-ttu-id="bc3b2-126">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bc3b2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc3b2-127">-Confirm</span></span>
<span data-ttu-id="bc3b2-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc3b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc3b2-129">-WhatIf</span></span>
<span data-ttu-id="bc3b2-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc3b2-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc3b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc3b2-132">CommonParameters</span></span>
<span data-ttu-id="bc3b2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bc3b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc3b2-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bc3b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc3b2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bc3b2-135">INPUTS</span></span>

## <span data-ttu-id="bc3b2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc3b2-136">OUTPUTS</span></span>

### <span data-ttu-id="bc3b2-137">Microsoft. Azure. PowerShell. командлеты. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="bc3b2-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="bc3b2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="bc3b2-138">NOTES</span></span>

<span data-ttu-id="bc3b2-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="bc3b2-139">ALIASES</span></span>

## <span data-ttu-id="bc3b2-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc3b2-140">RELATED LINKS</span></span>

