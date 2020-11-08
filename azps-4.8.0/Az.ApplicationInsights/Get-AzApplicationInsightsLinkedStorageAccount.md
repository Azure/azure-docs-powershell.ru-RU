---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077977"
---
# <span data-ttu-id="3e74e-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3e74e-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="3e74e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e74e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e74e-103">Получение учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="3e74e-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="3e74e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e74e-104">SYNTAX</span></span>

### <span data-ttu-id="3e74e-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e74e-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e74e-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e74e-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e74e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3e74e-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e74e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e74e-108">DESCRIPTION</span></span>
<span data-ttu-id="3e74e-109">Получение учетной записи связанного хранилища Application Insights</span><span class="sxs-lookup"><span data-stu-id="3e74e-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="3e74e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e74e-110">EXAMPLES</span></span>

### <span data-ttu-id="3e74e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e74e-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="3e74e-112">Получение связанной учетной записи хранилища, связанной с компонентом "componentName"</span><span class="sxs-lookup"><span data-stu-id="3e74e-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="3e74e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e74e-113">PARAMETERS</span></span>

### <span data-ttu-id="3e74e-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="3e74e-114">-ComponentName</span></span>
<span data-ttu-id="3e74e-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="3e74e-115">Component Name</span></span>

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

### <span data-ttu-id="3e74e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e74e-116">-DefaultProfile</span></span>
<span data-ttu-id="3e74e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e74e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e74e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e74e-118">-InputObject</span></span>
<span data-ttu-id="3e74e-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3e74e-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="3e74e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e74e-120">-ResourceGroupName</span></span>
<span data-ttu-id="3e74e-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3e74e-121">Resource Group Name</span></span>

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

### <span data-ttu-id="3e74e-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e74e-122">-ResourceId</span></span>
<span data-ttu-id="3e74e-123">ResourceId (ИД) компонента</span><span class="sxs-lookup"><span data-stu-id="3e74e-123">Component ResourceId</span></span>

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

### <span data-ttu-id="3e74e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e74e-124">CommonParameters</span></span>
<span data-ttu-id="3e74e-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e74e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e74e-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e74e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e74e-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e74e-127">INPUTS</span></span>

### <span data-ttu-id="3e74e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="3e74e-128">System.String</span></span>

### <span data-ttu-id="3e74e-129">Microsoft. Azure. Commands. ApplicationInsights. Models. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3e74e-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="3e74e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e74e-130">OUTPUTS</span></span>

### <span data-ttu-id="3e74e-131">Microsoft. Azure. Commands. ApplicationInsights. Models. PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3e74e-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="3e74e-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e74e-132">NOTES</span></span>

## <span data-ttu-id="3e74e-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e74e-133">RELATED LINKS</span></span>
