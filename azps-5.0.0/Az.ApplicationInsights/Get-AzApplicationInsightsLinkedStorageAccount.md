---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316255"
---
# <span data-ttu-id="e565c-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e565c-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="e565c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e565c-102">SYNOPSIS</span></span>
<span data-ttu-id="e565c-103">Получение учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="e565c-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="e565c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e565c-104">SYNTAX</span></span>

### <span data-ttu-id="e565c-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e565c-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e565c-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e565c-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e565c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e565c-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e565c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e565c-108">DESCRIPTION</span></span>
<span data-ttu-id="e565c-109">Получение учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="e565c-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="e565c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e565c-110">EXAMPLES</span></span>

### <span data-ttu-id="e565c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e565c-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="e565c-112">Получение связанной учетной записи хранилища, связанной с компонентом "componentName"</span><span class="sxs-lookup"><span data-stu-id="e565c-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="e565c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e565c-113">PARAMETERS</span></span>

### <span data-ttu-id="e565c-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="e565c-114">-ComponentName</span></span>
<span data-ttu-id="e565c-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="e565c-115">Component Name</span></span>

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

### <span data-ttu-id="e565c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e565c-116">-DefaultProfile</span></span>
<span data-ttu-id="e565c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e565c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e565c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e565c-118">-InputObject</span></span>
<span data-ttu-id="e565c-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e565c-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="e565c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e565c-120">-ResourceGroupName</span></span>
<span data-ttu-id="e565c-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e565c-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e565c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e565c-122">-ResourceId</span></span>
<span data-ttu-id="e565c-123">ResourceId (ИД) компонента</span><span class="sxs-lookup"><span data-stu-id="e565c-123">Component ResourceId</span></span>

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

### <span data-ttu-id="e565c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e565c-124">CommonParameters</span></span>
<span data-ttu-id="e565c-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e565c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e565c-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e565c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e565c-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e565c-127">INPUTS</span></span>

### <span data-ttu-id="e565c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e565c-128">System.String</span></span>

### <span data-ttu-id="e565c-129">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e565c-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="e565c-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e565c-130">OUTPUTS</span></span>

### <span data-ttu-id="e565c-131">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e565c-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="e565c-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e565c-132">NOTES</span></span>

## <span data-ttu-id="e565c-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e565c-133">RELATED LINKS</span></span>
