---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: dfbf5833bd045c40315cb06d2e954688229ac557
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565205"
---
# <span data-ttu-id="0a211-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="0a211-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="0a211-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a211-102">SYNOPSIS</span></span>
<span data-ttu-id="0a211-103">Возвращает данные об использовании рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a211-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a211-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a211-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a211-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a211-105">DESCRIPTION</span></span>
<span data-ttu-id="0a211-106">Командлет **Get-AzureRmOperationalInsightsWorkspaceUsage** извлекает данные об использовании рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a211-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="0a211-107">Это показывает объем данных, проанализированных рабочей областью за определенный период.</span><span class="sxs-lookup"><span data-stu-id="0a211-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="0a211-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a211-108">EXAMPLES</span></span>

### <span data-ttu-id="0a211-109">Пример 1: получение данных об использовании по имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="0a211-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0a211-110">Эта команда получает сведения об использовании рабочей области с именем MyWorkspace в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0a211-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="0a211-111">Пример 2: получение данных об использовании с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="0a211-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="0a211-112">Эта команда получает рабочую область с именем MyWorkSpace с помощью командлета Get-AzureRmOperationalInsightsWorkspace, а затем передает рабочую область текущему командлету.</span><span class="sxs-lookup"><span data-stu-id="0a211-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="0a211-113">Команда получает сведения об использовании для этой рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a211-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="0a211-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a211-114">PARAMETERS</span></span>

### <span data-ttu-id="0a211-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a211-115">-Name</span></span>
<span data-ttu-id="0a211-116">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0a211-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0a211-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a211-117">-ResourceGroupName</span></span>
<span data-ttu-id="0a211-118">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0a211-118">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0a211-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a211-119">-DefaultProfile</span></span>
<span data-ttu-id="0a211-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a211-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a211-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a211-121">CommonParameters</span></span>
<span data-ttu-id="0a211-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a211-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a211-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a211-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a211-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a211-124">INPUTS</span></span>

## <span data-ttu-id="0a211-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a211-125">OUTPUTS</span></span>

### <span data-ttu-id="0a211-126">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSUsageMetric]</span><span class="sxs-lookup"><span data-stu-id="0a211-126">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric]</span></span>

## <span data-ttu-id="0a211-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a211-127">NOTES</span></span>

## <span data-ttu-id="0a211-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a211-128">RELATED LINKS</span></span>

[<span data-ttu-id="0a211-129">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="0a211-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0a211-130">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a211-130">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


