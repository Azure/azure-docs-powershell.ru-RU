---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 9eb2b145f6a5968f460ba9a9506a4e0956793d01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560208"
---
# <span data-ttu-id="96059-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="96059-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="96059-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96059-102">SYNOPSIS</span></span>
<span data-ttu-id="96059-103">Обновляет аналитическое представление хранилища.</span><span class="sxs-lookup"><span data-stu-id="96059-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96059-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96059-104">SYNTAX</span></span>

### <span data-ttu-id="96059-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96059-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96059-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="96059-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96059-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96059-107">DESCRIPTION</span></span>
<span data-ttu-id="96059-108">Командлет **Set-AzureRmOperationalInsightsStorageInsight** изменяет конфигурацию аналитического анализа данных.</span><span class="sxs-lookup"><span data-stu-id="96059-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="96059-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96059-109">EXAMPLES</span></span>

### <span data-ttu-id="96059-110">Пример 1: изменение аналитического элемента хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="96059-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="96059-111">Эта команда изменяет таблицы, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="96059-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="96059-112">Пример 2: изменение аналитического элемента хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="96059-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="96059-113">Первая команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="96059-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="96059-114">Вторая команда изменяет контейнеры, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="96059-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="96059-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96059-115">PARAMETERS</span></span>

### <span data-ttu-id="96059-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="96059-116">-Containers</span></span>
<span data-ttu-id="96059-117">Указывает список контейнеров, предоставляющих данные.</span><span class="sxs-lookup"><span data-stu-id="96059-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96059-118">-DefaultProfile</span></span>
<span data-ttu-id="96059-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96059-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96059-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96059-120">-Name</span></span>
<span data-ttu-id="96059-121">Указывает имя аналитического элемента хранилища.</span><span class="sxs-lookup"><span data-stu-id="96059-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96059-122">-ResourceGroupName</span></span>
<span data-ttu-id="96059-123">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="96059-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="96059-124">-StorageAccountKey</span></span>
<span data-ttu-id="96059-125">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="96059-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-126">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="96059-126">-Tables</span></span>
<span data-ttu-id="96059-127">Указывает список таблиц, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="96059-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-128">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="96059-128">-Workspace</span></span>
<span data-ttu-id="96059-129">Указывает рабочую область, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="96059-129">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="96059-130">-WorkspaceName</span></span>
<span data-ttu-id="96059-131">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="96059-131">Specifies the name of a workspace.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96059-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96059-132">CommonParameters</span></span>
<span data-ttu-id="96059-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96059-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96059-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96059-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96059-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96059-135">INPUTS</span></span>

### <span data-ttu-id="96059-136">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="96059-136">PSWorkspace</span></span>
<span data-ttu-id="96059-137">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="96059-137">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="96059-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96059-138">OUTPUTS</span></span>

### <span data-ttu-id="96059-139">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="96059-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="96059-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="96059-140">NOTES</span></span>

## <span data-ttu-id="96059-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96059-141">RELATED LINKS</span></span>

[<span data-ttu-id="96059-142">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="96059-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="96059-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="96059-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


