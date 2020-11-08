---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 901d1b20856014ab66addb6b2b0c8cff94f364fc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077225"
---
# <span data-ttu-id="23348-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="23348-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="23348-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23348-102">SYNOPSIS</span></span>
<span data-ttu-id="23348-103">Обновляет аналитическое представление хранилища.</span><span class="sxs-lookup"><span data-stu-id="23348-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="23348-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23348-104">SYNTAX</span></span>

### <span data-ttu-id="23348-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23348-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23348-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="23348-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23348-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23348-107">DESCRIPTION</span></span>
<span data-ttu-id="23348-108">Командлет **Set-AzOperationalInsightsStorageInsight** изменяет конфигурацию аналитического анализа данных.</span><span class="sxs-lookup"><span data-stu-id="23348-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="23348-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23348-109">EXAMPLES</span></span>

### <span data-ttu-id="23348-110">Пример 1: изменение аналитического элемента хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="23348-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="23348-111">Эта команда изменяет таблицы, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="23348-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="23348-112">Пример 2: изменение аналитического элемента хранилища с помощью объекта Workspace</span><span class="sxs-lookup"><span data-stu-id="23348-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="23348-113">Первая команда использует командлет Get-AzOperationalInsightsWorkspace, чтобы получить рабочую область с именем MyWorkspace, а затем сохранит ее в переменной $Workspace.</span><span class="sxs-lookup"><span data-stu-id="23348-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="23348-114">Вторая команда изменяет контейнеры, из которых аналитический элемент MyStorageInsight считывает данные из хранилища.</span><span class="sxs-lookup"><span data-stu-id="23348-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="23348-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23348-115">PARAMETERS</span></span>

### <span data-ttu-id="23348-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="23348-116">-Containers</span></span>
<span data-ttu-id="23348-117">Указывает список контейнеров, предоставляющих данные.</span><span class="sxs-lookup"><span data-stu-id="23348-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="23348-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23348-118">-DefaultProfile</span></span>
<span data-ttu-id="23348-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23348-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23348-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23348-120">-Name</span></span>
<span data-ttu-id="23348-121">Указывает имя аналитического элемента хранилища.</span><span class="sxs-lookup"><span data-stu-id="23348-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="23348-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23348-122">-ResourceGroupName</span></span>
<span data-ttu-id="23348-123">Указывает имя группы ресурсов Azure, содержащей рабочую область.</span><span class="sxs-lookup"><span data-stu-id="23348-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="23348-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="23348-124">-StorageAccountKey</span></span>
<span data-ttu-id="23348-125">Задает клавишу доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="23348-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="23348-126">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="23348-126">-Tables</span></span>
<span data-ttu-id="23348-127">Указывает список таблиц, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="23348-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="23348-128">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="23348-128">-Workspace</span></span>
<span data-ttu-id="23348-129">Указывает рабочую область, в которой находится аналитика хранилища.</span><span class="sxs-lookup"><span data-stu-id="23348-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="23348-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23348-130">-WorkspaceName</span></span>
<span data-ttu-id="23348-131">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="23348-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="23348-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23348-132">CommonParameters</span></span>
<span data-ttu-id="23348-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23348-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23348-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23348-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23348-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23348-135">INPUTS</span></span>

### <span data-ttu-id="23348-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="23348-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="23348-137">System. String</span><span class="sxs-lookup"><span data-stu-id="23348-137">System.String</span></span>

### <span data-ttu-id="23348-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="23348-138">System.String[]</span></span>

## <span data-ttu-id="23348-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23348-139">OUTPUTS</span></span>

### <span data-ttu-id="23348-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="23348-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="23348-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="23348-141">NOTES</span></span>

## <span data-ttu-id="23348-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23348-142">RELATED LINKS</span></span>

[<span data-ttu-id="23348-143">Командлеты оперативной аналитики Azure</span><span class="sxs-lookup"><span data-stu-id="23348-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="23348-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="23348-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


