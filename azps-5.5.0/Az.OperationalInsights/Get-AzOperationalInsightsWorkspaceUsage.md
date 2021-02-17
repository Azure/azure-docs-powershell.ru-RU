---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 88a416f48bc94756c24295f0db3cce1efdfc8ffe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240424"
---
# <span data-ttu-id="21da6-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="21da6-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="21da6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21da6-102">SYNOPSIS</span></span>
<span data-ttu-id="21da6-103">Возвращает данные об использовании рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21da6-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="21da6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="21da6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21da6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="21da6-105">DESCRIPTION</span></span>
<span data-ttu-id="21da6-106">Командлет **Get-AzOperationalInsightsWorkspaceUsage** извлекает данные об использовании рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21da6-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="21da6-107">В результате будет отсвечен объем данных, проанализирован в рабочей области за определенный период.</span><span class="sxs-lookup"><span data-stu-id="21da6-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="21da6-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="21da6-108">EXAMPLES</span></span>

### <span data-ttu-id="21da6-109">Пример 1. Получить данные об использовании по имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="21da6-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="21da6-110">Эта команда получает сведения об использовании рабочей области MyWorkspace в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="21da6-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="21da6-111">Пример 2. Использование данных с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="21da6-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="21da6-112">Эта команда получает рабочее пространство myWorkSpace с Get-AzOperationalInsightsWorkspace и передает ее текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="21da6-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="21da6-113">Команда получает сведения об использовании этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21da6-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="21da6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21da6-114">PARAMETERS</span></span>

### <span data-ttu-id="21da6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21da6-115">-DefaultProfile</span></span>
<span data-ttu-id="21da6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="21da6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21da6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="21da6-117">-Name</span></span>
<span data-ttu-id="21da6-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="21da6-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21da6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21da6-119">-ResourceGroupName</span></span>
<span data-ttu-id="21da6-120">Имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="21da6-120">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21da6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21da6-121">CommonParameters</span></span>
<span data-ttu-id="21da6-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21da6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21da6-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21da6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21da6-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="21da6-124">INPUTS</span></span>

### <span data-ttu-id="21da6-125">System.String</span><span class="sxs-lookup"><span data-stu-id="21da6-125">System.String</span></span>

## <span data-ttu-id="21da6-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="21da6-126">OUTPUTS</span></span>

### <span data-ttu-id="21da6-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="21da6-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="21da6-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="21da6-128">NOTES</span></span>

## <span data-ttu-id="21da6-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="21da6-129">RELATED LINKS</span></span>

[<span data-ttu-id="21da6-130">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="21da6-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="21da6-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="21da6-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


