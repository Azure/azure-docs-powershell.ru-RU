---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: c3ca23ae1cbe29c7c2867ec9ac48bea612dd4fc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976504"
---
# <span data-ttu-id="0a31d-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0a31d-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="0a31d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a31d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a31d-103">Получите данные в рабочей области Azure Log Analytics.</span><span class="sxs-lookup"><span data-stu-id="0a31d-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="0a31d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0a31d-104">SYNTAX</span></span>

### <span data-ttu-id="0a31d-105">ByWorkspaceNameByKind (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a31d-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a31d-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="0a31d-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a31d-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="0a31d-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a31d-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="0a31d-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a31d-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a31d-109">DESCRIPTION</span></span>
<span data-ttu-id="0a31d-110">Для получения источников данных возвращается **cmdlet Get-AzOperationalInsightsDataSource.**</span><span class="sxs-lookup"><span data-stu-id="0a31d-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="0a31d-111">Вы можете указать источник данных, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="0a31d-111">You can specify a data source to get.</span></span>
<span data-ttu-id="0a31d-112">Результаты можно фильтровать в зависимости от типа источника данных.</span><span class="sxs-lookup"><span data-stu-id="0a31d-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="0a31d-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0a31d-113">EXAMPLES</span></span>

## <span data-ttu-id="0a31d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a31d-114">PARAMETERS</span></span>

### <span data-ttu-id="0a31d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a31d-115">-DefaultProfile</span></span>
<span data-ttu-id="0a31d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0a31d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a31d-117">-Kind</span><span class="sxs-lookup"><span data-stu-id="0a31d-117">-Kind</span></span>
<span data-ttu-id="0a31d-118">Определяет тип источников данных, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="0a31d-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="0a31d-119">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="0a31d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a31d-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="0a31d-120">AzureActivityLog</span></span> 
- <span data-ttu-id="0a31d-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="0a31d-121">CustomLog</span></span> 
- <span data-ttu-id="0a31d-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="0a31d-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="0a31d-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="0a31d-123">LinuxSyslog</span></span> 
- <span data-ttu-id="0a31d-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="0a31d-124">WindowsEvent</span></span> 
- <span data-ttu-id="0a31d-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="0a31d-125">WindowsPerformanceCounter</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByKind
Aliases:
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter, ApplicationInsights

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a31d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0a31d-126">-Name</span></span>
<span data-ttu-id="0a31d-127">Указывает имя источника данных, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="0a31d-127">Specifies the name of a data source to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a31d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a31d-128">-ResourceGroupName</span></span>
<span data-ttu-id="0a31d-129">Имя группы ресурсов, которая содержит источники данных, которые нужно получить.</span><span class="sxs-lookup"><span data-stu-id="0a31d-129">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a31d-130">-Workspace</span><span class="sxs-lookup"><span data-stu-id="0a31d-130">-Workspace</span></span>
<span data-ttu-id="0a31d-131">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a31d-131">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a31d-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0a31d-132">-WorkspaceName</span></span>
<span data-ttu-id="0a31d-133">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a31d-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByKind
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByWorkspaceNameByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a31d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a31d-134">CommonParameters</span></span>
<span data-ttu-id="0a31d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a31d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a31d-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a31d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a31d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0a31d-137">INPUTS</span></span>

### <span data-ttu-id="0a31d-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="0a31d-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="0a31d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="0a31d-139">System.String</span></span>

## <span data-ttu-id="0a31d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0a31d-140">OUTPUTS</span></span>

### <span data-ttu-id="0a31d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="0a31d-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="0a31d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0a31d-142">NOTES</span></span>
* <span data-ttu-id="0a31d-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, operational, insights</span><span class="sxs-lookup"><span data-stu-id="0a31d-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="0a31d-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a31d-144">RELATED LINKS</span></span>

[<span data-ttu-id="0a31d-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0a31d-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="0a31d-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="0a31d-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


