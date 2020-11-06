---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: a88806ddd934c2c7ee4eb8bb6f463da24ecefde7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560811"
---
# <span data-ttu-id="9ea78-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ea78-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="9ea78-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ea78-102">SYNOPSIS</span></span>
<span data-ttu-id="9ea78-103">Получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9ea78-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ea78-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ea78-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ea78-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ea78-105">DESCRIPTION</span></span>
<span data-ttu-id="9ea78-106">Командлет **Get-AzureRmOperationalInsightsWorkspace** получает сведения о существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9ea78-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="9ea78-107">При указании имени рабочей области этот командлет получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9ea78-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="9ea78-108">Если имя не задано, этот командлет получает сведения обо всех рабочих областях в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ea78-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="9ea78-109">Если не указать имя и группу ресурсов, этот командлет получает сведения обо всех рабочих областях в подписке.</span><span class="sxs-lookup"><span data-stu-id="9ea78-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="9ea78-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ea78-110">EXAMPLES</span></span>

### <span data-ttu-id="9ea78-111">Пример 1: получение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="9ea78-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="9ea78-112">Эта команда получает рабочую область с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9ea78-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="9ea78-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ea78-113">PARAMETERS</span></span>

### <span data-ttu-id="9ea78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ea78-114">-DefaultProfile</span></span>
<span data-ttu-id="9ea78-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ea78-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ea78-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ea78-116">-Name</span></span>
<span data-ttu-id="9ea78-117">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="9ea78-117">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="9ea78-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ea78-118">-ResourceGroupName</span></span>
<span data-ttu-id="9ea78-119">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="9ea78-119">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="9ea78-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ea78-120">CommonParameters</span></span>
<span data-ttu-id="9ea78-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ea78-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ea78-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ea78-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ea78-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ea78-123">INPUTS</span></span>

### <span data-ttu-id="9ea78-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9ea78-124">System.String</span></span>

## <span data-ttu-id="9ea78-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ea78-125">OUTPUTS</span></span>

### <span data-ttu-id="9ea78-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="9ea78-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="9ea78-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ea78-127">NOTES</span></span>

## <span data-ttu-id="9ea78-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ea78-128">RELATED LINKS</span></span>

[<span data-ttu-id="9ea78-129">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="9ea78-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


