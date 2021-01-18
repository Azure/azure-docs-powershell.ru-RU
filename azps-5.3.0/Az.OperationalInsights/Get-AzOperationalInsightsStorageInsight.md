---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505468"
---
# <span data-ttu-id="31e20-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="31e20-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="31e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31e20-102">SYNOPSIS</span></span>
<span data-ttu-id="31e20-103">Сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="31e20-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="31e20-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31e20-104">SYNTAX</span></span>

### <span data-ttu-id="31e20-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31e20-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31e20-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="31e20-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31e20-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31e20-107">DESCRIPTION</span></span>
<span data-ttu-id="31e20-108">Для получения сведений о существующей информации о хранилище можно использовать cmdlet **Get-AzOperationalInsightStorageInsight.**</span><span class="sxs-lookup"><span data-stu-id="31e20-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="31e20-109">Если задано имя "Сведения о хранилище", этот cmdlet получает сведения об этой информации.</span><span class="sxs-lookup"><span data-stu-id="31e20-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="31e20-110">Если имя не указано, этот cmdlet получает сведения обо всех данных о хранилище в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="31e20-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="31e20-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31e20-111">EXAMPLES</span></span>

### <span data-ttu-id="31e20-112">Пример 1. Просмотр данных хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="31e20-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="31e20-113">Эта команда получает сведения о хранилище MyStorageInsight из рабочей области ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="31e20-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="31e20-114">Пример 2. Анализ хранилища с помощью объекта рабочей области</span><span class="sxs-lookup"><span data-stu-id="31e20-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="31e20-115">Первая команда использует командлет **Get-AzOperationalInsightsWorkspace** для получения рабочей области Operational Insights, а затем сохраняет ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="31e20-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="31e20-116">Вторая команда получает сведения о хранилище MyStorageInsight для рабочей области в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="31e20-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="31e20-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31e20-117">PARAMETERS</span></span>

### <span data-ttu-id="31e20-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e20-118">-DefaultProfile</span></span>
<span data-ttu-id="31e20-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="31e20-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31e20-120">-Name</span><span class="sxs-lookup"><span data-stu-id="31e20-120">-Name</span></span>
<span data-ttu-id="31e20-121">Имя "Сведения о хранилище".</span><span class="sxs-lookup"><span data-stu-id="31e20-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="31e20-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e20-122">-ResourceGroupName</span></span>
<span data-ttu-id="31e20-123">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="31e20-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="31e20-124">-Workspace</span><span class="sxs-lookup"><span data-stu-id="31e20-124">-Workspace</span></span>
<span data-ttu-id="31e20-125">Определяет рабочее пространство, содержательное "Сведения о хранилище".</span><span class="sxs-lookup"><span data-stu-id="31e20-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="31e20-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="31e20-126">-WorkspaceName</span></span>
<span data-ttu-id="31e20-127">Указывает имя рабочей области, которая содержит сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="31e20-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="31e20-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e20-128">CommonParameters</span></span>
<span data-ttu-id="31e20-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e20-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e20-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e20-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e20-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31e20-131">INPUTS</span></span>

### <span data-ttu-id="31e20-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="31e20-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="31e20-133">System.String</span><span class="sxs-lookup"><span data-stu-id="31e20-133">System.String</span></span>

## <span data-ttu-id="31e20-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31e20-134">OUTPUTS</span></span>

### <span data-ttu-id="31e20-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="31e20-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="31e20-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31e20-136">NOTES</span></span>

## <span data-ttu-id="31e20-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31e20-137">RELATED LINKS</span></span>

[<span data-ttu-id="31e20-138">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="31e20-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


