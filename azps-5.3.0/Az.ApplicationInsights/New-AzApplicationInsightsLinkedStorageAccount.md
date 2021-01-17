---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422967"
---
# <span data-ttu-id="46cf0-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46cf0-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="46cf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46cf0-102">SYNOPSIS</span></span>
<span data-ttu-id="46cf0-103">Создание связанной учетной записи хранилища для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="46cf0-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="46cf0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46cf0-104">SYNTAX</span></span>

### <span data-ttu-id="46cf0-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46cf0-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46cf0-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="46cf0-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46cf0-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="46cf0-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46cf0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46cf0-108">DESCRIPTION</span></span>
<span data-ttu-id="46cf0-109">Создание связанной учетной записи хранилища для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="46cf0-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="46cf0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46cf0-110">EXAMPLES</span></span>

### <span data-ttu-id="46cf0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46cf0-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="46cf0-112">Создание связанной учетной записи $account в компоненте ComponentName</span><span class="sxs-lookup"><span data-stu-id="46cf0-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="46cf0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46cf0-113">PARAMETERS</span></span>

### <span data-ttu-id="46cf0-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="46cf0-114">-ComponentName</span></span>
<span data-ttu-id="46cf0-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="46cf0-115">Component Name</span></span>

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

### <span data-ttu-id="46cf0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46cf0-116">-DefaultProfile</span></span>
<span data-ttu-id="46cf0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46cf0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46cf0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46cf0-118">-InputObject</span></span>
<span data-ttu-id="46cf0-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="46cf0-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="46cf0-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="46cf0-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="46cf0-121">ResourceId учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="46cf0-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="46cf0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46cf0-122">-ResourceGroupName</span></span>
<span data-ttu-id="46cf0-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="46cf0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="46cf0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46cf0-124">-ResourceId</span></span>
<span data-ttu-id="46cf0-125">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="46cf0-125">Component ResourceId</span></span>

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

### <span data-ttu-id="46cf0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46cf0-126">-Confirm</span></span>
<span data-ttu-id="46cf0-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="46cf0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46cf0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46cf0-128">-WhatIf</span></span>
<span data-ttu-id="46cf0-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46cf0-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46cf0-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46cf0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46cf0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46cf0-131">CommonParameters</span></span>
<span data-ttu-id="46cf0-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46cf0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46cf0-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46cf0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46cf0-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46cf0-134">INPUTS</span></span>

### <span data-ttu-id="46cf0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="46cf0-135">System.String</span></span>

### <span data-ttu-id="46cf0-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="46cf0-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="46cf0-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46cf0-137">OUTPUTS</span></span>

### <span data-ttu-id="46cf0-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="46cf0-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="46cf0-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46cf0-139">NOTES</span></span>

## <span data-ttu-id="46cf0-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46cf0-140">RELATED LINKS</span></span>
