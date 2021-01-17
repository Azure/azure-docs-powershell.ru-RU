---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401903"
---
# <span data-ttu-id="433d2-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="433d2-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="433d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433d2-102">SYNOPSIS</span></span>
<span data-ttu-id="433d2-103">Обновляет сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="433d2-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="433d2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="433d2-104">SYNTAX</span></span>

### <span data-ttu-id="433d2-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="433d2-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433d2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="433d2-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433d2-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="433d2-107">DESCRIPTION</span></span>
<span data-ttu-id="433d2-108">Cmdlet **Set-AzOperationalInsightsStorageInsight** изменяет конфигурацию аналитики хранилища.</span><span class="sxs-lookup"><span data-stu-id="433d2-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="433d2-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="433d2-109">EXAMPLES</span></span>

### <span data-ttu-id="433d2-110">Пример 1. Изменение данных хранилища по имени</span><span class="sxs-lookup"><span data-stu-id="433d2-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="433d2-111">Эта команда изменяет таблицы, из которых будет прочитана информация о хранилище MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="433d2-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="433d2-112">Пример 2. Изменение статистики хранилища с помощью объекта рабочей области</span><span class="sxs-lookup"><span data-stu-id="433d2-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="433d2-113">Первая команда использует Get-AzOperationalInsightsWorkspace для получения рабочей области MyWorkspace, а затем сохраняет ее в $Workspace переменной.</span><span class="sxs-lookup"><span data-stu-id="433d2-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="433d2-114">Вторая команда изменяет контейнеры, из которых вы читаете "Сведения о хранилище" с именем MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="433d2-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="433d2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433d2-115">PARAMETERS</span></span>

### <span data-ttu-id="433d2-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="433d2-116">-Containers</span></span>
<span data-ttu-id="433d2-117">Определяет список контейнеров, которые предоставляют данные.</span><span class="sxs-lookup"><span data-stu-id="433d2-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="433d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433d2-118">-DefaultProfile</span></span>
<span data-ttu-id="433d2-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="433d2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="433d2-120">-Name</span><span class="sxs-lookup"><span data-stu-id="433d2-120">-Name</span></span>
<span data-ttu-id="433d2-121">Указывает имя статистики хранилища.</span><span class="sxs-lookup"><span data-stu-id="433d2-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="433d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="433d2-123">Указывает имя группы ресурсов Azure, которая содержит рабочее пространство.</span><span class="sxs-lookup"><span data-stu-id="433d2-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="433d2-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="433d2-124">-StorageAccountKey</span></span>
<span data-ttu-id="433d2-125">Указывает ключ доступа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="433d2-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="433d2-126">-Таблицы</span><span class="sxs-lookup"><span data-stu-id="433d2-126">-Tables</span></span>
<span data-ttu-id="433d2-127">Определяет список таблиц, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="433d2-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="433d2-128">-Workspace</span><span class="sxs-lookup"><span data-stu-id="433d2-128">-Workspace</span></span>
<span data-ttu-id="433d2-129">Определяет рабочее пространство, содержательное сведения о хранилище.</span><span class="sxs-lookup"><span data-stu-id="433d2-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="433d2-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="433d2-130">-WorkspaceName</span></span>
<span data-ttu-id="433d2-131">Указывает имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="433d2-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="433d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433d2-132">CommonParameters</span></span>
<span data-ttu-id="433d2-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433d2-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="433d2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433d2-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="433d2-135">INPUTS</span></span>

### <span data-ttu-id="433d2-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="433d2-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="433d2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="433d2-137">System.String</span></span>

### <span data-ttu-id="433d2-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="433d2-138">System.String[]</span></span>

## <span data-ttu-id="433d2-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="433d2-139">OUTPUTS</span></span>

### <span data-ttu-id="433d2-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="433d2-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="433d2-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="433d2-141">NOTES</span></span>

## <span data-ttu-id="433d2-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="433d2-142">RELATED LINKS</span></span>

[<span data-ttu-id="433d2-143">Azure Operational Insights Cmdlets</span><span class="sxs-lookup"><span data-stu-id="433d2-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="433d2-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="433d2-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


