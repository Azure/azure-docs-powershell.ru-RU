---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406759"
---
# <span data-ttu-id="44459-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="44459-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="44459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44459-102">SYNOPSIS</span></span>
<span data-ttu-id="44459-103">Удаление связанной учетной записи хранения в статистике приложения</span><span class="sxs-lookup"><span data-stu-id="44459-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="44459-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="44459-104">SYNTAX</span></span>

### <span data-ttu-id="44459-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44459-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44459-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44459-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44459-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44459-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44459-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44459-108">DESCRIPTION</span></span>
<span data-ttu-id="44459-109">Удаление связанной учетной записи хранения в статистике приложения</span><span class="sxs-lookup"><span data-stu-id="44459-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="44459-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="44459-110">EXAMPLES</span></span>

### <span data-ttu-id="44459-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44459-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="44459-112">Удаление связанной учетной записи хранения, связанной с компонентом "имя компонента" для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="44459-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="44459-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44459-113">PARAMETERS</span></span>

### <span data-ttu-id="44459-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="44459-114">-ComponentName</span></span>
<span data-ttu-id="44459-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="44459-115">Component Name</span></span>

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

### <span data-ttu-id="44459-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44459-116">-DefaultProfile</span></span>
<span data-ttu-id="44459-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44459-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44459-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44459-118">-InputObject</span></span>
<span data-ttu-id="44459-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="44459-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="44459-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44459-120">-ResourceGroupName</span></span>
<span data-ttu-id="44459-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="44459-121">Resource Group Name</span></span>

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

### <span data-ttu-id="44459-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44459-122">-ResourceId</span></span>
<span data-ttu-id="44459-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="44459-123">Component ResourceId</span></span>

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

### <span data-ttu-id="44459-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44459-124">-Confirm</span></span>
<span data-ttu-id="44459-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44459-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44459-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44459-126">-WhatIf</span></span>
<span data-ttu-id="44459-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44459-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44459-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="44459-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44459-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44459-129">CommonParameters</span></span>
<span data-ttu-id="44459-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44459-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44459-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44459-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44459-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="44459-132">INPUTS</span></span>

### <span data-ttu-id="44459-133">System.String</span><span class="sxs-lookup"><span data-stu-id="44459-133">System.String</span></span>

### <span data-ttu-id="44459-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="44459-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="44459-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="44459-135">OUTPUTS</span></span>

### <span data-ttu-id="44459-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44459-136">System.Boolean</span></span>

## <span data-ttu-id="44459-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="44459-137">NOTES</span></span>

## <span data-ttu-id="44459-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44459-138">RELATED LINKS</span></span>
