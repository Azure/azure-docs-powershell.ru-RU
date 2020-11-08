---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 652a5668bd641ae1b68093f431e0aa0963aca50b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248145"
---
# <span data-ttu-id="1660c-101">New-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1660c-101">New-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="1660c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1660c-102">SYNOPSIS</span></span>
<span data-ttu-id="1660c-103">Создание учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="1660c-103">Create an application insights linked storage account</span></span>

## <span data-ttu-id="1660c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1660c-104">SYNTAX</span></span>

### <span data-ttu-id="1660c-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1660c-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1660c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1660c-106">ByInputObjectParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 -LinkedStorageAccountResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1660c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1660c-107">ByResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> -LinkedStorageAccountResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1660c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1660c-108">DESCRIPTION</span></span>
<span data-ttu-id="1660c-109">Создание учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="1660c-109">Create an application insights linked storage account</span></span>

## <span data-ttu-id="1660c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1660c-110">EXAMPLES</span></span>

### <span data-ttu-id="1660c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1660c-111">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName "rgName" -Name "accountName"

Get-AzApplicationInsights -ResourceGroupName "rgName" -Name "componentName" | New-AzApplicationInsightsLinkedStorageAccount -LinkedStorageAccountResourceId $account.Id
```

<span data-ttu-id="1660c-112">Создание связанной учетной записи хранения $account в разделе Component "componentName"</span><span class="sxs-lookup"><span data-stu-id="1660c-112">Create linked storage account $account under component "componentName"</span></span>

## <span data-ttu-id="1660c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1660c-113">PARAMETERS</span></span>

### <span data-ttu-id="1660c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="1660c-114">-ComponentName</span></span>
<span data-ttu-id="1660c-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="1660c-115">Component Name</span></span>

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

### <span data-ttu-id="1660c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1660c-116">-DefaultProfile</span></span>
<span data-ttu-id="1660c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1660c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1660c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1660c-118">-InputObject</span></span>
<span data-ttu-id="1660c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1660c-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="1660c-120">-LinkedStorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1660c-120">-LinkedStorageAccountResourceId</span></span>
<span data-ttu-id="1660c-121">ResourceId (ИД) учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1660c-121">Storage Account ResourceId</span></span>

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

### <span data-ttu-id="1660c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1660c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1660c-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1660c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1660c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1660c-124">-ResourceId</span></span>
<span data-ttu-id="1660c-125">ResourceId (ИД) компонента</span><span class="sxs-lookup"><span data-stu-id="1660c-125">Component ResourceId</span></span>

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

### <span data-ttu-id="1660c-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1660c-126">-Confirm</span></span>
<span data-ttu-id="1660c-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1660c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1660c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1660c-128">-WhatIf</span></span>
<span data-ttu-id="1660c-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1660c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1660c-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1660c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1660c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1660c-131">CommonParameters</span></span>
<span data-ttu-id="1660c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1660c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1660c-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1660c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1660c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1660c-134">INPUTS</span></span>

### <span data-ttu-id="1660c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1660c-135">System.String</span></span>

### <span data-ttu-id="1660c-136">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="1660c-136">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="1660c-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1660c-137">OUTPUTS</span></span>

### <span data-ttu-id="1660c-138">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1660c-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="1660c-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1660c-139">NOTES</span></span>

## <span data-ttu-id="1660c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1660c-140">RELATED LINKS</span></span>
