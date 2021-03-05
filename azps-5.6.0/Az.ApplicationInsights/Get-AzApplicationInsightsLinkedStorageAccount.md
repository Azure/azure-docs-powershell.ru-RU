---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: a059209e993f17ffb5eed1b29d1854f8387f3d8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965235"
---
# <span data-ttu-id="396a3-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="396a3-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="396a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="396a3-102">SYNOPSIS</span></span>
<span data-ttu-id="396a3-103">Связанная учетная запись хранения для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="396a3-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="396a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="396a3-104">SYNTAX</span></span>

### <span data-ttu-id="396a3-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="396a3-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="396a3-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="396a3-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="396a3-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="396a3-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="396a3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="396a3-108">DESCRIPTION</span></span>
<span data-ttu-id="396a3-109">Связанная учетная запись хранения для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="396a3-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="396a3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="396a3-110">EXAMPLES</span></span>

### <span data-ttu-id="396a3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="396a3-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="396a3-112">Получить связанную учетную запись хранения, связанную с компонентом ComponentName</span><span class="sxs-lookup"><span data-stu-id="396a3-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="396a3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="396a3-113">PARAMETERS</span></span>

### <span data-ttu-id="396a3-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="396a3-114">-ComponentName</span></span>
<span data-ttu-id="396a3-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="396a3-115">Component Name</span></span>

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

### <span data-ttu-id="396a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="396a3-116">-DefaultProfile</span></span>
<span data-ttu-id="396a3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="396a3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="396a3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="396a3-118">-InputObject</span></span>
<span data-ttu-id="396a3-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="396a3-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="396a3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="396a3-120">-ResourceGroupName</span></span>
<span data-ttu-id="396a3-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="396a3-121">Resource Group Name</span></span>

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

### <span data-ttu-id="396a3-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="396a3-122">-ResourceId</span></span>
<span data-ttu-id="396a3-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="396a3-123">Component ResourceId</span></span>

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

### <span data-ttu-id="396a3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396a3-124">CommonParameters</span></span>
<span data-ttu-id="396a3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396a3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396a3-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="396a3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396a3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="396a3-127">INPUTS</span></span>

### <span data-ttu-id="396a3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="396a3-128">System.String</span></span>

### <span data-ttu-id="396a3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="396a3-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="396a3-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="396a3-130">OUTPUTS</span></span>

### <span data-ttu-id="396a3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="396a3-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="396a3-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="396a3-132">NOTES</span></span>

## <span data-ttu-id="396a3-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="396a3-133">RELATED LINKS</span></span>
