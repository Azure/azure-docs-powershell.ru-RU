---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsLinkedStorageAccount.md
ms.openlocfilehash: 7e879cd4e513ebdad297933269e373c625f2e407
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229353"
---
# <span data-ttu-id="e02ef-101">Get-AzApplicationInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e02ef-101">Get-AzApplicationInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="e02ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e02ef-102">SYNOPSIS</span></span>
<span data-ttu-id="e02ef-103">Связанная учетная запись хранилища для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="e02ef-103">Get application insights linked storage account</span></span>

## <span data-ttu-id="e02ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e02ef-104">SYNTAX</span></span>

### <span data-ttu-id="e02ef-105">ByResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e02ef-105">ByResourceNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName <String> -ComponentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02ef-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e02ef-106">ByInputObjectParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -InputObject <PSApplicationInsightsComponent>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e02ef-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e02ef-107">ByResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsLinkedStorageAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e02ef-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e02ef-108">DESCRIPTION</span></span>
<span data-ttu-id="e02ef-109">Связанная учетная запись хранилища для анализа приложений</span><span class="sxs-lookup"><span data-stu-id="e02ef-109">Get application insights linked storage account</span></span>

## <span data-ttu-id="e02ef-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e02ef-110">EXAMPLES</span></span>

### <span data-ttu-id="e02ef-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e02ef-111">Example 1</span></span>
```powershell
Get-AzApplicationInsightsLinkedStorageAccount -ResourceGroupName "rgName" -Name "componentName"
```

<span data-ttu-id="e02ef-112">Получить связанную учетную запись хранения, связанную с компонентом ComponentName</span><span class="sxs-lookup"><span data-stu-id="e02ef-112">Get linked storage account associated with component "componentName"</span></span>

## <span data-ttu-id="e02ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e02ef-113">PARAMETERS</span></span>

### <span data-ttu-id="e02ef-114">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="e02ef-114">-ComponentName</span></span>
<span data-ttu-id="e02ef-115">Имя компонента</span><span class="sxs-lookup"><span data-stu-id="e02ef-115">Component Name</span></span>

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

### <span data-ttu-id="e02ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02ef-116">-DefaultProfile</span></span>
<span data-ttu-id="e02ef-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e02ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e02ef-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e02ef-118">-InputObject</span></span>
<span data-ttu-id="e02ef-119">PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e02ef-119">PSApplicationInsightsComponent</span></span>

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

### <span data-ttu-id="e02ef-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e02ef-120">-ResourceGroupName</span></span>
<span data-ttu-id="e02ef-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e02ef-121">Resource Group Name</span></span>

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

### <span data-ttu-id="e02ef-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e02ef-122">-ResourceId</span></span>
<span data-ttu-id="e02ef-123">Component ResourceId</span><span class="sxs-lookup"><span data-stu-id="e02ef-123">Component ResourceId</span></span>

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

### <span data-ttu-id="e02ef-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02ef-124">CommonParameters</span></span>
<span data-ttu-id="e02ef-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02ef-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02ef-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e02ef-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02ef-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e02ef-127">INPUTS</span></span>

### <span data-ttu-id="e02ef-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e02ef-128">System.String</span></span>

### <span data-ttu-id="e02ef-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="e02ef-129">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="e02ef-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e02ef-130">OUTPUTS</span></span>

### <span data-ttu-id="e02ef-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e02ef-131">Microsoft.Azure.Commands.ApplicationInsights.Models.PSComponentLinkedStorageAccounts</span></span>

## <span data-ttu-id="e02ef-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e02ef-132">NOTES</span></span>

## <span data-ttu-id="e02ef-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e02ef-133">RELATED LINKS</span></span>
