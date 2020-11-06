---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacemanagementgroups
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceManagementGroups.md
ms.openlocfilehash: 215e3007de3b3760d974512cdffdd669f32447ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560039"
---
# <span data-ttu-id="901fb-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span><span class="sxs-lookup"><span data-stu-id="901fb-101">Get-AzureRmOperationalInsightsWorkspaceManagementGroups</span></span>

## <span data-ttu-id="901fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="901fb-102">SYNOPSIS</span></span>
<span data-ttu-id="901fb-103">Получение сведений о группах управления, подключенных к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="901fb-103">Gets details of management groups connected to a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="901fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="901fb-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceManagementGroups [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="901fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="901fb-105">DESCRIPTION</span></span>
<span data-ttu-id="901fb-106">Командлет **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** содержит список групп управления, подключенных к рабочей области.</span><span class="sxs-lookup"><span data-stu-id="901fb-106">The **Get-AzureRmOperationalInsightsWorkspaceManagementGroups** cmdlet lists the management groups that are connected to a workspace.</span></span>

## <span data-ttu-id="901fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="901fb-107">EXAMPLES</span></span>

### <span data-ttu-id="901fb-108">Пример 1: получение групп управления по имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="901fb-108">Example 1: Get management groups by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceManagementGroups -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="901fb-109">Эта команда получает группы управления для рабочей области с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="901fb-109">This command gets the management groups for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="901fb-110">Пример 2: получение групп управления с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="901fb-110">Example 2: Get management groups by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceManagementGroups
```

<span data-ttu-id="901fb-111">Эта команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем передает рабочую область текущему командлету, который получает группы управления для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="901fb-111">This command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes the workspace to the current cmdlet, which gets the management groups for that workspace.</span></span>

## <span data-ttu-id="901fb-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="901fb-112">PARAMETERS</span></span>

### <span data-ttu-id="901fb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901fb-113">-DefaultProfile</span></span>
<span data-ttu-id="901fb-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="901fb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="901fb-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="901fb-115">-Name</span></span>
<span data-ttu-id="901fb-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="901fb-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="901fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="901fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="901fb-118">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="901fb-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="901fb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901fb-119">CommonParameters</span></span>
<span data-ttu-id="901fb-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="901fb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901fb-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="901fb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901fb-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="901fb-122">INPUTS</span></span>

### <span data-ttu-id="901fb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="901fb-123">System.String</span></span>

## <span data-ttu-id="901fb-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="901fb-124">OUTPUTS</span></span>

### <span data-ttu-id="901fb-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="901fb-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSManagementGroup</span></span>

## <span data-ttu-id="901fb-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="901fb-126">NOTES</span></span>

## <span data-ttu-id="901fb-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="901fb-127">RELATED LINKS</span></span>

[<span data-ttu-id="901fb-128">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="901fb-128">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="901fb-129">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="901fb-129">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


