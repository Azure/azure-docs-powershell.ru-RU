---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398652"
---
# <span data-ttu-id="1dcb6-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dcb6-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1dcb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dcb6-102">SYNOPSIS</span></span>
<span data-ttu-id="1dcb6-103">Получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="1dcb6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1dcb6-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dcb6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1dcb6-105">DESCRIPTION</span></span>
<span data-ttu-id="1dcb6-106">Командлет **Get-AzOperationalInsightsWorkspace** получает сведения о существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="1dcb6-107">Если указать имя рабочей области, этот cmdlet получит сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="1dcb6-108">Если имя не указано, этот cmdlet получает сведения обо всех рабочей области в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="1dcb6-109">Если имя и группа ресурсов не указаны, этот cmdlet получает сведения обо всех рабочей области в подписке.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="1dcb6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1dcb6-110">EXAMPLES</span></span>

### <span data-ttu-id="1dcb6-111">Пример 1. Получить рабочее пространство по имени</span><span class="sxs-lookup"><span data-stu-id="1dcb6-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="1dcb6-112">Эта команда получает рабочее пространство с именем MyWorkspace в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="1dcb6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dcb6-113">PARAMETERS</span></span>

### <span data-ttu-id="1dcb6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dcb6-114">-DefaultProfile</span></span>
<span data-ttu-id="1dcb6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1dcb6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dcb6-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1dcb6-116">-Name</span></span>
<span data-ttu-id="1dcb6-117">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="1dcb6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dcb6-118">-ResourceGroupName</span></span>
<span data-ttu-id="1dcb6-119">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="1dcb6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dcb6-120">CommonParameters</span></span>
<span data-ttu-id="1dcb6-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dcb6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dcb6-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dcb6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dcb6-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1dcb6-123">INPUTS</span></span>

### <span data-ttu-id="1dcb6-124">System.String</span><span class="sxs-lookup"><span data-stu-id="1dcb6-124">System.String</span></span>

## <span data-ttu-id="1dcb6-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1dcb6-125">OUTPUTS</span></span>

### <span data-ttu-id="1dcb6-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1dcb6-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1dcb6-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1dcb6-127">NOTES</span></span>

## <span data-ttu-id="1dcb6-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1dcb6-128">RELATED LINKS</span></span>

[<span data-ttu-id="1dcb6-129">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1dcb6-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


