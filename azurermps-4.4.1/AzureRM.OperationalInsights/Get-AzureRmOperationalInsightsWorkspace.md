---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 042597d8d300f57600680282dadb16e8ec221e59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733666"
---
# <span data-ttu-id="8c89c-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c89c-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="8c89c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c89c-102">SYNOPSIS</span></span>
<span data-ttu-id="8c89c-103">Получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8c89c-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c89c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c89c-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c89c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c89c-105">DESCRIPTION</span></span>
<span data-ttu-id="8c89c-106">Командлет **Get-AzureRmOperationalInsightsWorkspace** получает сведения о существующей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8c89c-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="8c89c-107">При указании имени рабочей области этот командлет получает сведения о рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8c89c-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="8c89c-108">Если имя не задано, этот командлет получает сведения обо всех рабочих областях в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c89c-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="8c89c-109">Если не указать имя и группу ресурсов, этот командлет получает сведения обо всех рабочих областях в подписке.</span><span class="sxs-lookup"><span data-stu-id="8c89c-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="8c89c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c89c-110">EXAMPLES</span></span>

### <span data-ttu-id="8c89c-111">Пример 1: получение рабочей области по имени</span><span class="sxs-lookup"><span data-stu-id="8c89c-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="8c89c-112">Эта команда получает рабочую область с именем MyWorkspace в группе ресурсов с именем ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8c89c-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="8c89c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c89c-113">PARAMETERS</span></span>

### <span data-ttu-id="8c89c-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8c89c-114">-Name</span></span>
<span data-ttu-id="8c89c-115">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8c89c-115">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="8c89c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c89c-116">-ResourceGroupName</span></span>
<span data-ttu-id="8c89c-117">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8c89c-117">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="8c89c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c89c-118">-DefaultProfile</span></span>
<span data-ttu-id="8c89c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8c89c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c89c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c89c-120">CommonParameters</span></span>
<span data-ttu-id="8c89c-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c89c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c89c-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c89c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c89c-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c89c-123">INPUTS</span></span>

## <span data-ttu-id="8c89c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c89c-124">OUTPUTS</span></span>

### <span data-ttu-id="8c89c-125">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="8c89c-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="8c89c-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8c89c-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="8c89c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c89c-127">NOTES</span></span>

## <span data-ttu-id="8c89c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c89c-128">RELATED LINKS</span></span>

[<span data-ttu-id="8c89c-129">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="8c89c-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


