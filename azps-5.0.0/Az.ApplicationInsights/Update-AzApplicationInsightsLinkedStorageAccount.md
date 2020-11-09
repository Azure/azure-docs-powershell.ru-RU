---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ef27923fbffc92a0190419cc5949c0b841b95dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316236"
---
# <span data-ttu-id="a3da6-101">Update-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a3da6-101">Update-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="a3da6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3da6-102">SYNOPSIS</span></span>
<span data-ttu-id="a3da6-103">Обновление учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="a3da6-103">Update application insights linked storage account</span></span>

## <span data-ttu-id="a3da6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3da6-104">SYNTAX</span></span>

### <span data-ttu-id="a3da6-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3da6-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3da6-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3da6-106">ByInputObjectParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3da6-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3da6-107">ByResourceIdParameterSet</span></span>
```
Update-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3da6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3da6-108">DESCRIPTION</span></span>
<span data-ttu-id="a3da6-109">Обновление учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="a3da6-109">Update application insights linked storage account</span></span>

## <span data-ttu-id="a3da6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3da6-110">EXAMPLES</span></span>

### <span data-ttu-id="a3da6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3da6-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | Update-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="a3da6-112">Обновление связанной учетной записи хранилища в компоненте "componentName" для связи с $account</span><span class="sxs-lookup"><span data-stu-id="a3da6-112">Update linked storage account under component "componentName" to associate with $account</span></span>

## <span data-ttu-id="a3da6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3da6-113">PARAMETERS</span></span>

### <span data-ttu-id="a3da6-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="a3da6-114">-ComponentName</span></span>
<span data-ttu-id="a3da6-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="a3da6-115">Component Name</span></span>

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

### <span data-ttu-id="a3da6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3da6-116">-DefaultProfile</span></span>
<span data-ttu-id="a3da6-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3da6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3da6-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3da6-118">-InputObject</span></span>
<span data-ttu-id="a3da6-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a3da6-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="a3da6-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a3da6-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="a3da6-121">ResourceId (ИД) учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a3da6-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="a3da6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3da6-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3da6-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a3da6-123">Resource Group Name</span></span>

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

### <span data-ttu-id="a3da6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3da6-124">-ResourceId</span></span>
<span data-ttu-id="a3da6-125">ResourceId (ИД) компонента</span><span class="sxs-lookup"><span data-stu-id="a3da6-125">Component ResourceId</span></span>

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

### <span data-ttu-id="a3da6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3da6-126">-Confirm</span></span>
<span data-ttu-id="a3da6-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3da6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3da6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3da6-128">-WhatIf</span></span>
<span data-ttu-id="a3da6-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3da6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3da6-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3da6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3da6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3da6-131">CommonParameters</span></span>
<span data-ttu-id="a3da6-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3da6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3da6-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3da6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3da6-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3da6-134">INPUTS</span></span>

### <span data-ttu-id="a3da6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a3da6-135">System.String</span></span>

### <span data-ttu-id="a3da6-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="a3da6-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a3da6-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3da6-137">OUTPUTS</span></span>

### <span data-ttu-id="a3da6-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="a3da6-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="a3da6-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3da6-139">NOTES</span></span>

## <span data-ttu-id="a3da6-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3da6-140">RELATED LINKS</span></span>
