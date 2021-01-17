---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422924"
---
# <span data-ttu-id="2a4ea-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2a4ea-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2a4ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a4ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4ea-103">Удаление учетной записи хранилища, связанной с анализом приложений</span><span class="sxs-lookup"><span data-stu-id="2a4ea-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="2a4ea-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a4ea-104">SYNTAX</span></span>

### <span data-ttu-id="2a4ea-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a4ea-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a4ea-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a4ea-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a4ea-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a4ea-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a4ea-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a4ea-108">DESCRIPTION</span></span>
<span data-ttu-id="2a4ea-109">Удаление учетной записи хранилища, связанной с анализом приложений</span><span class="sxs-lookup"><span data-stu-id="2a4ea-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="2a4ea-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a4ea-110">EXAMPLES</span></span>

### <span data-ttu-id="2a4ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2a4ea-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="2a4ea-112">Удаление связанной учетной записи хранения, связанной с компонентом "имя компонента" для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="2a4ea-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="2a4ea-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a4ea-113">PARAMETERS</span></span>

### <span data-ttu-id="2a4ea-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="2a4ea-114">-ComponentName</span></span>
<span data-ttu-id="2a4ea-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="2a4ea-115">Component Name</span></span>

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

### <span data-ttu-id="2a4ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4ea-116">-DefaultProfile</span></span>
<span data-ttu-id="2a4ea-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4ea-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a4ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a4ea-118">-InputObject</span></span>
<span data-ttu-id="2a4ea-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2a4ea-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="2a4ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a4ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="2a4ea-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2a4ea-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2a4ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a4ea-122">-ResourceId</span></span>
<span data-ttu-id="2a4ea-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a4ea-123">Component ResourceId</span></span>

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

### <span data-ttu-id="2a4ea-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a4ea-124">-Confirm</span></span>
<span data-ttu-id="2a4ea-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a4ea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a4ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a4ea-126">-WhatIf</span></span>
<span data-ttu-id="2a4ea-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a4ea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a4ea-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a4ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a4ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4ea-129">CommonParameters</span></span>
<span data-ttu-id="2a4ea-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a4ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4ea-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a4ea-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4ea-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a4ea-132">INPUTS</span></span>

### <span data-ttu-id="2a4ea-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2a4ea-133">System.String</span></span>

### <span data-ttu-id="2a4ea-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="2a4ea-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="2a4ea-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a4ea-135">OUTPUTS</span></span>

### <span data-ttu-id="2a4ea-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a4ea-136">System.Boolean</span></span>

## <span data-ttu-id="2a4ea-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a4ea-137">NOTES</span></span>

## <span data-ttu-id="2a4ea-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a4ea-138">RELATED LINKS</span></span>
