---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 05bcd77a732be66c426f456f6058e74107b6eb8d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731934"
---
# <span data-ttu-id="d2ada-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2ada-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="d2ada-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2ada-102">SYNOPSIS</span></span>
<span data-ttu-id="d2ada-103">Получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d2ada-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="d2ada-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2ada-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2ada-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ada-105">DESCRIPTION</span></span>
<span data-ttu-id="d2ada-106">Командлет **Get-AzOperationalInsightsWorkspace** получает сведения о существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d2ada-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="d2ada-107">При указании имени рабочей области этот командлет получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d2ada-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="d2ada-108">Если имя не задано, этот командлет получает сведения обо всех рабочих областях в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d2ada-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="d2ada-109">Если не указать имя и группу ресурсов, этот командлет получает сведения обо всех рабочих областях в подписке.</span><span class="sxs-lookup"><span data-stu-id="d2ada-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="d2ada-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2ada-110">EXAMPLES</span></span>

### <span data-ttu-id="d2ada-111">Пример 1: получение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="d2ada-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="d2ada-112">Эта команда получает рабочую область с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d2ada-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="d2ada-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2ada-113">PARAMETERS</span></span>

### <span data-ttu-id="d2ada-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2ada-114">-DefaultProfile</span></span>
<span data-ttu-id="d2ada-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d2ada-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2ada-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2ada-116">-Name</span></span>
<span data-ttu-id="d2ada-117">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d2ada-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ada-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2ada-118">-ResourceGroupName</span></span>
<span data-ttu-id="d2ada-119">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="d2ada-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2ada-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2ada-120">CommonParameters</span></span>
<span data-ttu-id="d2ada-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2ada-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2ada-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2ada-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2ada-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2ada-123">INPUTS</span></span>

### <span data-ttu-id="d2ada-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d2ada-124">System.String</span></span>

## <span data-ttu-id="d2ada-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2ada-125">OUTPUTS</span></span>

### <span data-ttu-id="d2ada-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d2ada-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="d2ada-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2ada-127">NOTES</span></span>

## <span data-ttu-id="d2ada-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2ada-128">RELATED LINKS</span></span>

[<span data-ttu-id="d2ada-129">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="d2ada-129">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


