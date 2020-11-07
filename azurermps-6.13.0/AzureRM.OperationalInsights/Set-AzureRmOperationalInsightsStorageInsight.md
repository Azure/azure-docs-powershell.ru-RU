---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 460a1585c8c6c556f0044b9cd0673a3be750ffe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732462"
---
# <span data-ttu-id="82c49-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="82c49-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="82c49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82c49-102">SYNOPSIS</span></span>
<span data-ttu-id="82c49-103">Обновляет аналитическое представление хранилища.</span><span class="sxs-lookup"><span data-stu-id="82c49-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82c49-104">SYNTAX</span></span>

### <span data-ttu-id="82c49-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="82c49-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82c49-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="82c49-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c49-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c49-107">DESCRIPTION</span></span>
<span data-ttu-id="82c49-108">Командлет **Set-AzureRmOperationalInsightsStorageInsight** изменяет конфигурацию аналитического анализа данных.</span><span class="sxs-lookup"><span data-stu-id="82c49-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="82c49-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82c49-109">EXAMPLES</span></span>

### <span data-ttu-id="82c49-110">Пример 1: изменение аналитического элемента хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="82c49-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="82c49-111">Эта команда изменяет таблицы, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="82c49-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="82c49-112">Пример 2: изменение аналитического элемента хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="82c49-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="82c49-113">Первая команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="82c49-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="82c49-114">Вторая команда изменяет контейнеры, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="82c49-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="82c49-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82c49-115">PARAMETERS</span></span>

### <span data-ttu-id="82c49-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="82c49-116">-Containers</span></span>
<span data-ttu-id="82c49-117">Указывает список контейнеров, предоставляющих данные.</span><span class="sxs-lookup"><span data-stu-id="82c49-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c49-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c49-118">-DefaultProfile</span></span>
<span data-ttu-id="82c49-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82c49-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82c49-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="82c49-120">-Name</span></span>
<span data-ttu-id="82c49-121">Указывает имя аналитического элемента хранилища.</span><span class="sxs-lookup"><span data-stu-id="82c49-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c49-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c49-122">-ResourceGroupName</span></span>
<span data-ttu-id="82c49-123">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="82c49-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="82c49-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="82c49-124">-StorageAccountKey</span></span>
<span data-ttu-id="82c49-125">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="82c49-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c49-126">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="82c49-126">-Tables</span></span>
<span data-ttu-id="82c49-127">Указывает список таблиц, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="82c49-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c49-128">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="82c49-128">-Workspace</span></span>
<span data-ttu-id="82c49-129">Указывает рабочую область, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="82c49-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="82c49-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="82c49-130">-WorkspaceName</span></span>
<span data-ttu-id="82c49-131">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="82c49-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="82c49-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c49-132">CommonParameters</span></span>
<span data-ttu-id="82c49-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82c49-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c49-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c49-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c49-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82c49-135">INPUTS</span></span>

### <span data-ttu-id="82c49-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="82c49-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="82c49-137">Параметры: Workspace (ByValue)</span><span class="sxs-lookup"><span data-stu-id="82c49-137">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="82c49-138">System. String</span><span class="sxs-lookup"><span data-stu-id="82c49-138">System.String</span></span>

### <span data-ttu-id="82c49-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="82c49-139">System.String[]</span></span>

## <span data-ttu-id="82c49-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c49-140">OUTPUTS</span></span>

### <span data-ttu-id="82c49-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="82c49-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="82c49-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="82c49-142">NOTES</span></span>

## <span data-ttu-id="82c49-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82c49-143">RELATED LINKS</span></span>

[<span data-ttu-id="82c49-144">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="82c49-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="82c49-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="82c49-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


