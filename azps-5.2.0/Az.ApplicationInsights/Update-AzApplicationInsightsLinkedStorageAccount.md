---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406716"
---
# <span data-ttu-id="025c5-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="025c5-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="025c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025c5-102">SYNOPSIS</span></span>
<span data-ttu-id="025c5-103">Обновление связанной учетной записи хранения для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="025c5-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="025c5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="025c5-104">SYNTAX</span></span>

### <span data-ttu-id="025c5-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="025c5-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="025c5-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="025c5-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="025c5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="025c5-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025c5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="025c5-108">DESCRIPTION</span></span>
<span data-ttu-id="025c5-109">Обновление связанной учетной записи хранения для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="025c5-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="025c5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="025c5-110">EXAMPLES</span></span>

### <span data-ttu-id="025c5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="025c5-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="025c5-112">Обновление связанной учетной записи хранения в компоненте ComponentName, чтобы связать ее с $account</span><span class="sxs-lookup"><span data-stu-id="025c5-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="025c5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025c5-113">PARAMETERS</span></span>

### <span data-ttu-id="025c5-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="025c5-114">-ComponentName</span></span>
<span data-ttu-id="025c5-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="025c5-115">Component Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025c5-116">-DefaultProfile</span></span>
<span data-ttu-id="025c5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="025c5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="025c5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="025c5-118">-InputObject</span></span>
<span data-ttu-id="025c5-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="025c5-119">PSApplicationInsightsComponent</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="025c5-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="025c5-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="025c5-121">ResourceId учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="025c5-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="025c5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="025c5-122">-ResourceGroupName</span></span>
<span data-ttu-id="025c5-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="025c5-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025c5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="025c5-124">-ResourceId</span></span>
<span data-ttu-id="025c5-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="025c5-125">Component ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="025c5-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="025c5-126">-Confirm</span></span>
<span data-ttu-id="025c5-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025c5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025c5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025c5-128">-WhatIf</span></span>
<span data-ttu-id="025c5-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025c5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="025c5-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="025c5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025c5-131">CommonParameters</span></span>
<span data-ttu-id="025c5-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025c5-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="025c5-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025c5-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="025c5-134">INPUTS</span></span>

### <span data-ttu-id="025c5-135">System.String</span><span class="sxs-lookup"><span data-stu-id="025c5-135">System.String</span></span>

### <span data-ttu-id="025c5-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="025c5-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="025c5-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="025c5-137">OUTPUTS</span></span>

### <span data-ttu-id="025c5-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="025c5-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="025c5-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="025c5-139">NOTES</span></span>

## <span data-ttu-id="025c5-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="025c5-140">RELATED LINKS</span></span>
