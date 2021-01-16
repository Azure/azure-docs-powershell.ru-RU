---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396247"
---
# <span data-ttu-id="8b77a-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="8b77a-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="8b77a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b77a-102">SYNOPSIS</span></span>
<span data-ttu-id="8b77a-103">Создание или обновление политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="8b77a-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="8b77a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b77a-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8b77a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b77a-105">DESCRIPTION</span></span>
<span data-ttu-id="8b77a-106">Создание или обновление политики доступа в указанной среде.</span><span class="sxs-lookup"><span data-stu-id="8b77a-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="8b77a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b77a-107">EXAMPLES</span></span>

### <span data-ttu-id="8b77a-108">Пример 1. Создание политики доступа для указанной среды</span><span class="sxs-lookup"><span data-stu-id="8b77a-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="8b77a-109">Эта команда создает политику доступа для указанной среды.</span><span class="sxs-lookup"><span data-stu-id="8b77a-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="8b77a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b77a-110">PARAMETERS</span></span>

### <span data-ttu-id="8b77a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b77a-111">-DefaultProfile</span></span>
<span data-ttu-id="8b77a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b77a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b77a-113">-Description</span><span class="sxs-lookup"><span data-stu-id="8b77a-113">-Description</span></span>
<span data-ttu-id="8b77a-114">Описание политики доступа.</span><span class="sxs-lookup"><span data-stu-id="8b77a-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="8b77a-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="8b77a-115">-EnvironmentName</span></span>
<span data-ttu-id="8b77a-116">Имя среды Time Series Insights, связанной с указанной группой ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b77a-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="8b77a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8b77a-117">-Name</span></span>
<span data-ttu-id="8b77a-118">Имя политики доступа.</span><span class="sxs-lookup"><span data-stu-id="8b77a-118">Name of the access policy.</span></span>

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

### <span data-ttu-id="8b77a-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="8b77a-119">-PrincipalObjectId</span></span>
<span data-ttu-id="8b77a-120">ObjectId основного объекта в Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8b77a-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="8b77a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b77a-121">-ResourceGroupName</span></span>
<span data-ttu-id="8b77a-122">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8b77a-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="8b77a-123">-Роль</span><span class="sxs-lookup"><span data-stu-id="8b77a-123">-Role</span></span>
<span data-ttu-id="8b77a-124">Список ролей, которые назначены основной в среде.</span><span class="sxs-lookup"><span data-stu-id="8b77a-124">The list of roles the principal is assigned on the environment.</span></span>

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

### <span data-ttu-id="8b77a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b77a-125">-SubscriptionId</span></span>
<span data-ttu-id="8b77a-126">ИД подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="8b77a-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="8b77a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b77a-127">-Confirm</span></span>
<span data-ttu-id="8b77a-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b77a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b77a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b77a-129">-WhatIf</span></span>
<span data-ttu-id="8b77a-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b77a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b77a-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8b77a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b77a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b77a-132">CommonParameters</span></span>
<span data-ttu-id="8b77a-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b77a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b77a-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b77a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b77a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b77a-135">INPUTS</span></span>

## <span data-ttu-id="8b77a-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b77a-136">OUTPUTS</span></span>

### <span data-ttu-id="8b77a-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="8b77a-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="8b77a-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b77a-138">NOTES</span></span>

<span data-ttu-id="8b77a-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b77a-139">ALIASES</span></span>

## <span data-ttu-id="8b77a-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b77a-140">RELATED LINKS</span></span>
