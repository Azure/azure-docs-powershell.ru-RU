---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: b0d3baaa1e41e6f0df74e1b6bf39bdc858777a92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556572"
---
# <span data-ttu-id="5d738-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="5d738-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="5d738-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d738-102">SYNOPSIS</span></span>
<span data-ttu-id="5d738-103">Получение сведений об аналитическом элементе хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d738-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d738-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d738-104">SYNTAX</span></span>

### <span data-ttu-id="5d738-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d738-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d738-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5d738-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d738-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d738-107">DESCRIPTION</span></span>
<span data-ttu-id="5d738-108">Командлет **Get-AzureRmOperationalInsightsStorageInsight** получает сведения о существующем аналитическом хранилище.</span><span class="sxs-lookup"><span data-stu-id="5d738-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="5d738-109">Если указано имя для аналитики хранилища, этот командлет получает сведения об этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="5d738-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="5d738-110">Если имя не задано, этот командлет получает сведения обо всех аналитиках хранилища в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5d738-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="5d738-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d738-111">EXAMPLES</span></span>

### <span data-ttu-id="5d738-112">Пример 1: получение сведений о хранении по имени</span><span class="sxs-lookup"><span data-stu-id="5d738-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="5d738-113">Эта команда получает аналитическое представление хранилища с именем MyStorageInsight из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="5d738-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="5d738-114">Пример 2: получение сведений об объеме хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="5d738-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="5d738-115">Первая команда использует командлет **Get-AzureRmOperationalInsightsWorkspace** для получения рабочей области оперативной аналитики и сохраняет ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="5d738-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="5d738-116">Вторая команда получает аналитическое представление хранилища с именем MyStorageInsight для рабочей области в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="5d738-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="5d738-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d738-117">PARAMETERS</span></span>

### <span data-ttu-id="5d738-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d738-118">-DefaultProfile</span></span>
<span data-ttu-id="5d738-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5d738-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d738-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d738-120">-Name</span></span>
<span data-ttu-id="5d738-121">Указывает имя аналитического анализа хранилища.</span><span class="sxs-lookup"><span data-stu-id="5d738-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="5d738-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d738-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d738-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="5d738-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="5d738-124">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="5d738-124">-Workspace</span></span>
<span data-ttu-id="5d738-125">Указывает рабочую область, содержащую аналитическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="5d738-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="5d738-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d738-126">-WorkspaceName</span></span>
<span data-ttu-id="5d738-127">Указывает имя рабочей области, содержащей аналитическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="5d738-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="5d738-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d738-128">CommonParameters</span></span>
<span data-ttu-id="5d738-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d738-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d738-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d738-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d738-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d738-131">INPUTS</span></span>

### <span data-ttu-id="5d738-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5d738-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="5d738-133">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5d738-133">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="5d738-134">System. String</span><span class="sxs-lookup"><span data-stu-id="5d738-134">System.String</span></span>

## <span data-ttu-id="5d738-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d738-135">OUTPUTS</span></span>

### <span data-ttu-id="5d738-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="5d738-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="5d738-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d738-137">NOTES</span></span>

## <span data-ttu-id="5d738-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d738-138">RELATED LINKS</span></span>

[<span data-ttu-id="5d738-139">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="5d738-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


