---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 85c85be195df2dfa393cbd4d91ae62d8731dbf93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734254"
---
# <span data-ttu-id="0e30d-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0e30d-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="0e30d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e30d-102">SYNOPSIS</span></span>
<span data-ttu-id="0e30d-103">Обновляет аналитическое представление хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e30d-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e30d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e30d-104">SYNTAX</span></span>

### <span data-ttu-id="0e30d-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e30d-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e30d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="0e30d-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e30d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e30d-107">DESCRIPTION</span></span>
<span data-ttu-id="0e30d-108">Командлет **Set-AzureRmOperationalInsightsStorageInsight** изменяет конфигурацию аналитического анализа данных.</span><span class="sxs-lookup"><span data-stu-id="0e30d-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="0e30d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e30d-109">EXAMPLES</span></span>

### <span data-ttu-id="0e30d-110">Пример 1: изменение аналитического элемента хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="0e30d-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="0e30d-111">Эта команда изменяет таблицы, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e30d-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="0e30d-112">Пример 2: изменение аналитического элемента хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="0e30d-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="0e30d-113">Первая команда использует командлет Get-AzureRmOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="0e30d-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="0e30d-114">Вторая команда изменяет контейнеры, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e30d-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="0e30d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e30d-115">PARAMETERS</span></span>

### <span data-ttu-id="0e30d-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="0e30d-116">-Containers</span></span>
<span data-ttu-id="0e30d-117">Указывает список контейнеров, предоставляющих данные.</span><span class="sxs-lookup"><span data-stu-id="0e30d-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="0e30d-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0e30d-118">-Name</span></span>
<span data-ttu-id="0e30d-119">Указывает имя аналитического элемента хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e30d-119">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="0e30d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e30d-120">-ResourceGroupName</span></span>
<span data-ttu-id="0e30d-121">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="0e30d-121">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="0e30d-122">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0e30d-122">-StorageAccountKey</span></span>
<span data-ttu-id="0e30d-123">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0e30d-123">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="0e30d-124">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="0e30d-124">-Tables</span></span>
<span data-ttu-id="0e30d-125">Указывает список таблиц, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="0e30d-125">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="0e30d-126">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="0e30d-126">-Workspace</span></span>
<span data-ttu-id="0e30d-127">Указывает рабочую область, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="0e30d-127">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="0e30d-128">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0e30d-128">-WorkspaceName</span></span>
<span data-ttu-id="0e30d-129">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0e30d-129">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="0e30d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e30d-130">-DefaultProfile</span></span>
<span data-ttu-id="0e30d-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e30d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e30d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e30d-132">CommonParameters</span></span>
<span data-ttu-id="0e30d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e30d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e30d-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e30d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e30d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e30d-135">INPUTS</span></span>

### <span data-ttu-id="0e30d-136">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e30d-136">PSWorkspace</span></span>
<span data-ttu-id="0e30d-137">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0e30d-137">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="0e30d-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e30d-138">OUTPUTS</span></span>

### <span data-ttu-id="0e30d-139">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="0e30d-139">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="0e30d-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e30d-140">NOTES</span></span>

## <span data-ttu-id="0e30d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e30d-141">RELATED LINKS</span></span>

[<span data-ttu-id="0e30d-142">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="0e30d-142">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="0e30d-143">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0e30d-143">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


