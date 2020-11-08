---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 6bb6a422af88c0d7cd911e575e9d49bcdafcd3d8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243727"
---
# <span data-ttu-id="3aa87-101">Remove-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3aa87-101">Remove-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="3aa87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3aa87-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa87-103">Удаление учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="3aa87-103">Delete application insights linked storage account</span></span>

## <span data-ttu-id="3aa87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3aa87-104">SYNTAX</span></span>

### <span data-ttu-id="3aa87-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3aa87-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa87-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aa87-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aa87-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aa87-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsLinkedStorageAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aa87-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa87-108">DESCRIPTION</span></span>
<span data-ttu-id="3aa87-109">Удаление учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="3aa87-109">Delete application insights linked storage account</span></span>

## <span data-ttu-id="3aa87-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3aa87-110">EXAMPLES</span></span>

### <span data-ttu-id="3aa87-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3aa87-111">Example 1</span></span>
```powershell
Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Remove-AzApplicationInsightsLinkedStorageAccount
```

<span data-ttu-id="3aa87-112">Удаление связанной учетной записи хранилища, связанной с компонентом Application Insights "componentName"</span><span class="sxs-lookup"><span data-stu-id="3aa87-112">Delete linked storage account associated with application insights component "componentName"</span></span>

## <span data-ttu-id="3aa87-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3aa87-113">PARAMETERS</span></span>

### <span data-ttu-id="3aa87-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="3aa87-114">-ComponentName</span></span>
<span data-ttu-id="3aa87-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="3aa87-115">Component Name</span></span>

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

### <span data-ttu-id="3aa87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa87-116">-DefaultProfile</span></span>
<span data-ttu-id="3aa87-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa87-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aa87-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aa87-118">-InputObject</span></span>
<span data-ttu-id="3aa87-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3aa87-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="3aa87-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa87-120">-ResourceGroupName</span></span>
<span data-ttu-id="3aa87-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3aa87-121">Resource Group Name</span></span>

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

### <span data-ttu-id="3aa87-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aa87-122">-ResourceId</span></span>
<span data-ttu-id="3aa87-123">ResourceId (ИД) компонента</span><span class="sxs-lookup"><span data-stu-id="3aa87-123">Component ResourceId</span></span>

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

### <span data-ttu-id="3aa87-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3aa87-124">-Confirm</span></span>
<span data-ttu-id="3aa87-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3aa87-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aa87-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aa87-126">-WhatIf</span></span>
<span data-ttu-id="3aa87-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3aa87-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3aa87-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3aa87-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aa87-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa87-129">CommonParameters</span></span>
<span data-ttu-id="3aa87-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3aa87-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa87-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3aa87-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa87-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3aa87-132">INPUTS</span></span>

### <span data-ttu-id="3aa87-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3aa87-133">System.String</span></span>

### <span data-ttu-id="3aa87-134">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3aa87-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="3aa87-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa87-135">OUTPUTS</span></span>

### <span data-ttu-id="3aa87-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3aa87-136">System.Boolean</span></span>

## <span data-ttu-id="3aa87-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="3aa87-137">NOTES</span></span>

## <span data-ttu-id="3aa87-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aa87-138">RELATED LINKS</span></span>
