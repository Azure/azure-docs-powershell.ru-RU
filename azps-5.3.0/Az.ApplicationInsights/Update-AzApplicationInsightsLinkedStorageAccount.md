---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422916"
---
# <span data-ttu-id="5923b-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5923b-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5923b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5923b-102">SYNOPSIS</span></span>
<span data-ttu-id="5923b-103">Обновление связанной учетной записи хранилища для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="5923b-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="5923b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5923b-104">SYNTAX</span></span>

### <span data-ttu-id="5923b-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5923b-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5923b-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5923b-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5923b-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5923b-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5923b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5923b-108">DESCRIPTION</span></span>
<span data-ttu-id="5923b-109">Обновление связанной учетной записи хранилища для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="5923b-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="5923b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5923b-110">EXAMPLES</span></span>

### <span data-ttu-id="5923b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5923b-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="5923b-112">Обновление связанной учетной записи хранения в компоненте ComponentName, чтобы связать ее с $account</span><span class="sxs-lookup"><span data-stu-id="5923b-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="5923b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5923b-113">PARAMETERS</span></span>

### <span data-ttu-id="5923b-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="5923b-114">-ComponentName</span></span>
<span data-ttu-id="5923b-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="5923b-115">Component Name</span></span>

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

### <span data-ttu-id="5923b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5923b-116">-DefaultProfile</span></span>
<span data-ttu-id="5923b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5923b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5923b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5923b-118">-InputObject</span></span>
<span data-ttu-id="5923b-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5923b-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="5923b-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5923b-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="5923b-121">ResourceId учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="5923b-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="5923b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5923b-122">-ResourceGroupName</span></span>
<span data-ttu-id="5923b-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5923b-123">Resource Group Name</span></span>

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

### <span data-ttu-id="5923b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5923b-124">-ResourceId</span></span>
<span data-ttu-id="5923b-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="5923b-125">Component ResourceId</span></span>

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

### <span data-ttu-id="5923b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5923b-126">-Confirm</span></span>
<span data-ttu-id="5923b-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5923b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5923b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5923b-128">-WhatIf</span></span>
<span data-ttu-id="5923b-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5923b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5923b-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5923b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5923b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5923b-131">CommonParameters</span></span>
<span data-ttu-id="5923b-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5923b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5923b-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5923b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5923b-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5923b-134">INPUTS</span></span>

### <span data-ttu-id="5923b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5923b-135">System.String</span></span>

### <span data-ttu-id="5923b-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="5923b-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="5923b-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5923b-137">OUTPUTS</span></span>

### <span data-ttu-id="5923b-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="5923b-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="5923b-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5923b-139">NOTES</span></span>

## <span data-ttu-id="5923b-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5923b-140">RELATED LINKS</span></span>
