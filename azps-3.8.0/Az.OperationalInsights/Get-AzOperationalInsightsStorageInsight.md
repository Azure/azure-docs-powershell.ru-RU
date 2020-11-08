---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: e23192eec18f835fe2019f4de8cf3d2219967622
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077196"
---
# <span data-ttu-id="ddd76-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ddd76-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ddd76-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ddd76-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd76-103">Получение сведений об аналитическом элементе хранилища.</span><span class="sxs-lookup"><span data-stu-id="ddd76-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="ddd76-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ddd76-104">SYNTAX</span></span>

### <span data-ttu-id="ddd76-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ddd76-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ddd76-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ddd76-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddd76-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd76-107">DESCRIPTION</span></span>
<span data-ttu-id="ddd76-108">Командлет **Get-AzOperationalInsightsStorageInsight** получает сведения о существующем аналитическом хранилище.</span><span class="sxs-lookup"><span data-stu-id="ddd76-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="ddd76-109">Если указано имя для аналитики хранилища, этот командлет получает сведения об этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="ddd76-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="ddd76-110">Если имя не задано, этот командлет получает сведения обо всех аналитиках хранилища в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ddd76-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="ddd76-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ddd76-111">EXAMPLES</span></span>

### <span data-ttu-id="ddd76-112">Пример 1: получение сведений о хранении по имени</span><span class="sxs-lookup"><span data-stu-id="ddd76-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ddd76-113">Эта команда получает аналитическое представление хранилища с именем MyStorageInsight из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="ddd76-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ddd76-114">Пример 2: получение сведений об объеме хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="ddd76-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="ddd76-115">Первая команда использует командлет **Get-AzOperationalInsightsWorkspace** для получения рабочей области оперативной аналитики и сохраняет ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="ddd76-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="ddd76-116">Вторая команда получает аналитическое представление хранилища с именем MyStorageInsight для рабочей области в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="ddd76-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="ddd76-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ddd76-117">PARAMETERS</span></span>

### <span data-ttu-id="ddd76-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd76-118">-DefaultProfile</span></span>
<span data-ttu-id="ddd76-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ddd76-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddd76-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ddd76-120">-Name</span></span>
<span data-ttu-id="ddd76-121">Указывает имя аналитического анализа хранилища.</span><span class="sxs-lookup"><span data-stu-id="ddd76-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd76-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd76-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddd76-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd76-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd76-124">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="ddd76-124">-Workspace</span></span>
<span data-ttu-id="ddd76-125">Указывает рабочую область, содержащую аналитическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="ddd76-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd76-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ddd76-126">-WorkspaceName</span></span>
<span data-ttu-id="ddd76-127">Указывает имя рабочей области, содержащей аналитическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="ddd76-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddd76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd76-128">CommonParameters</span></span>
<span data-ttu-id="ddd76-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ddd76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd76-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddd76-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd76-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ddd76-131">INPUTS</span></span>

### <span data-ttu-id="ddd76-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ddd76-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ddd76-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd76-133">System.String</span></span>

## <span data-ttu-id="ddd76-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ddd76-134">OUTPUTS</span></span>

### <span data-ttu-id="ddd76-135">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ddd76-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="ddd76-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ddd76-136">NOTES</span></span>

## <span data-ttu-id="ddd76-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ddd76-137">RELATED LINKS</span></span>

[<span data-ttu-id="ddd76-138">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="ddd76-138">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


