---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913243"
---
# <span data-ttu-id="56736-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="56736-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="56736-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56736-102">SYNOPSIS</span></span>
<span data-ttu-id="56736-103">Возвращает данные об использовании рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56736-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="56736-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56736-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56736-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56736-105">DESCRIPTION</span></span>
<span data-ttu-id="56736-106">Командлет **Get-AzOperationalInsightsWorkspaceUsage** извлекает данные об использовании рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56736-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="56736-107">Это показывает объем данных, проанализированных рабочей областью за определенный период.</span><span class="sxs-lookup"><span data-stu-id="56736-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="56736-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56736-108">EXAMPLES</span></span>

### <span data-ttu-id="56736-109">Пример 1: получение данных об использовании по имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="56736-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="56736-110">Эта команда получает сведения об использовании рабочей области с именем MyWorkspace в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56736-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="56736-111">Пример 2: получение данных об использовании с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="56736-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="56736-112">Эта команда получает рабочую область с именем MyWorkSpace с помощью командлета Get-AzOperationalInsightsWorkspace, а затем передает рабочую область текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="56736-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="56736-113">Команда получает сведения об использовании для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56736-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="56736-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56736-114">PARAMETERS</span></span>

### <span data-ttu-id="56736-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56736-115">-DefaultProfile</span></span>
<span data-ttu-id="56736-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="56736-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56736-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56736-117">-Name</span></span>
<span data-ttu-id="56736-118">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="56736-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="56736-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56736-119">-ResourceGroupName</span></span>
<span data-ttu-id="56736-120">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="56736-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="56736-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56736-121">CommonParameters</span></span>
<span data-ttu-id="56736-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56736-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56736-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56736-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56736-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56736-124">INPUTS</span></span>

### <span data-ttu-id="56736-125">System. String</span><span class="sxs-lookup"><span data-stu-id="56736-125">System.String</span></span>

## <span data-ttu-id="56736-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56736-126">OUTPUTS</span></span>

### <span data-ttu-id="56736-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="56736-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="56736-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="56736-128">NOTES</span></span>

## <span data-ttu-id="56736-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56736-129">RELATED LINKS</span></span>

[<span data-ttu-id="56736-130">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="56736-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="56736-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="56736-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


