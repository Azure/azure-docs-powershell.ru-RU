---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: cd7dad03d8542685339778d0b0cdac967f83ea21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733669"
---
# <span data-ttu-id="e79d0-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e79d0-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="e79d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e79d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e79d0-103">Получение сведений об аналитическом элементе хранилища.</span><span class="sxs-lookup"><span data-stu-id="e79d0-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e79d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e79d0-104">SYNTAX</span></span>

### <span data-ttu-id="e79d0-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e79d0-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e79d0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e79d0-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e79d0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e79d0-107">DESCRIPTION</span></span>
<span data-ttu-id="e79d0-108">Командлет **Get-AzureRmOperationalInsightsStorageInsight** получает сведения о существующем аналитическом хранилище.</span><span class="sxs-lookup"><span data-stu-id="e79d0-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="e79d0-109">Если указано имя для аналитики хранилища, этот командлет получает сведения об этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="e79d0-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="e79d0-110">Если имя не задано, этот командлет получает сведения обо всех аналитиках хранилища в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e79d0-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="e79d0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e79d0-111">EXAMPLES</span></span>

### <span data-ttu-id="e79d0-112">Пример 1: получение сведений о хранении по имени</span><span class="sxs-lookup"><span data-stu-id="e79d0-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="e79d0-113">Эта команда получает аналитическое представление хранилища с именем MyStorageInsight из рабочей области с именем ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="e79d0-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="e79d0-114">Пример 2: получение сведений об объеме хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="e79d0-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="e79d0-115">Первая команда использует командлет **Get-AzureRmOperationalInsightsWorkspace** для получения рабочей области оперативной аналитики и сохраняет ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="e79d0-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="e79d0-116">Вторая команда получает аналитическое представление хранилища с именем MyStorageInsight для рабочей области в $Workspace.</span><span class="sxs-lookup"><span data-stu-id="e79d0-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="e79d0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e79d0-117">PARAMETERS</span></span>

### <span data-ttu-id="e79d0-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e79d0-118">-Name</span></span>
<span data-ttu-id="e79d0-119">Указывает имя аналитического анализа хранилища.</span><span class="sxs-lookup"><span data-stu-id="e79d0-119">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="e79d0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e79d0-120">-ResourceGroupName</span></span>
<span data-ttu-id="e79d0-121">Указывает имя группы ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="e79d0-121">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="e79d0-122">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="e79d0-122">-Workspace</span></span>
<span data-ttu-id="e79d0-123">Указывает рабочую область, содержащую аналитическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e79d0-123">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="e79d0-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e79d0-124">-WorkspaceName</span></span>
<span data-ttu-id="e79d0-125">Указывает имя рабочей области, содержащей аналитическое хранилище.</span><span class="sxs-lookup"><span data-stu-id="e79d0-125">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="e79d0-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e79d0-126">-DefaultProfile</span></span>
<span data-ttu-id="e79d0-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e79d0-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e79d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e79d0-128">CommonParameters</span></span>
<span data-ttu-id="e79d0-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e79d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e79d0-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e79d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e79d0-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e79d0-131">INPUTS</span></span>

### <span data-ttu-id="e79d0-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e79d0-132">PSWorkspace</span></span>
<span data-ttu-id="e79d0-133">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e79d0-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e79d0-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e79d0-134">OUTPUTS</span></span>

### <span data-ttu-id="e79d0-135">System. Collections. Generic. List ' 1 [Microsoft. Azure. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="e79d0-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="e79d0-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="e79d0-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="e79d0-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e79d0-137">NOTES</span></span>

## <span data-ttu-id="e79d0-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e79d0-138">RELATED LINKS</span></span>

[<span data-ttu-id="e79d0-139">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="e79d0-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


