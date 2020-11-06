---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93570512"
---
# <span data-ttu-id="520bd-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="520bd-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="520bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="520bd-102">SYNOPSIS</span></span>
<span data-ttu-id="520bd-103">Получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="520bd-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="520bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="520bd-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="520bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="520bd-105">DESCRIPTION</span></span>
<span data-ttu-id="520bd-106">Командлет **Get-AzureRmOperationalInsightsWorkspace** получает сведения о существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="520bd-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="520bd-107">При указании имени рабочей области этот командлет получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="520bd-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="520bd-108">Если имя не задано, этот командлет получает сведения обо всех рабочих областях в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="520bd-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="520bd-109">Если не указать имя и группу ресурсов, этот командлет получает сведения обо всех рабочих областях в подписке.</span><span class="sxs-lookup"><span data-stu-id="520bd-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="520bd-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="520bd-110">EXAMPLES</span></span>

### <span data-ttu-id="520bd-111">Пример 1: получение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="520bd-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="520bd-112">Эта команда получает рабочую область с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="520bd-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="520bd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="520bd-113">PARAMETERS</span></span>

### <span data-ttu-id="520bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="520bd-114">-DefaultProfile</span></span>
<span data-ttu-id="520bd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="520bd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="520bd-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="520bd-116">-Name</span></span>
<span data-ttu-id="520bd-117">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="520bd-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="520bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="520bd-119">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="520bd-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="520bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="520bd-120">CommonParameters</span></span>
<span data-ttu-id="520bd-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="520bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="520bd-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="520bd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="520bd-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="520bd-123">INPUTS</span></span>

### <span data-ttu-id="520bd-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="520bd-124">None</span></span>
<span data-ttu-id="520bd-125">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="520bd-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="520bd-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="520bd-126">OUTPUTS</span></span>

### <span data-ttu-id="520bd-127">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="520bd-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="520bd-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="520bd-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="520bd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="520bd-129">NOTES</span></span>

## <span data-ttu-id="520bd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="520bd-130">RELATED LINKS</span></span>

[<span data-ttu-id="520bd-131">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="520bd-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


