---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsDataSource.md
ms.openlocfilehash: f291eedade1a1a243f22dc618ffcc538a9158de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729862"
---
# <span data-ttu-id="28650-101">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="28650-101">Get-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="28650-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28650-102">SYNOPSIS</span></span>
<span data-ttu-id="28650-103">Получение источников данных в области "анализ журналов Azure".</span><span class="sxs-lookup"><span data-stu-id="28650-103">Get datasources under Azure Log Analytics workspace.</span></span>

## <span data-ttu-id="28650-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28650-104">SYNTAX</span></span>

### <span data-ttu-id="28650-105">ByWorkspaceNameByKind (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28650-105">ByWorkspaceNameByKind (Default)</span></span>
```
Get-AzOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28650-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="28650-106">ByWorkspaceObjectByName</span></span>
```
Get-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28650-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="28650-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28650-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="28650-108">ByWorkspaceNameByName</span></span>
```
Get-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28650-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28650-109">DESCRIPTION</span></span>
<span data-ttu-id="28650-110">Командлет **Get-AzOperationalInsightsDataSource** получает источники данных.</span><span class="sxs-lookup"><span data-stu-id="28650-110">The **Get-AzOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="28650-111">Вы можете указать источник данных для получения.</span><span class="sxs-lookup"><span data-stu-id="28650-111">You can specify a data source to get.</span></span>
<span data-ttu-id="28650-112">Вы можете отфильтровать результаты в зависимости от типа источника данных.</span><span class="sxs-lookup"><span data-stu-id="28650-112">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="28650-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28650-113">EXAMPLES</span></span>

## <span data-ttu-id="28650-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28650-114">PARAMETERS</span></span>

### <span data-ttu-id="28650-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28650-115">-DefaultProfile</span></span>
<span data-ttu-id="28650-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="28650-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28650-117">-Видах</span><span class="sxs-lookup"><span data-stu-id="28650-117">-Kind</span></span>
<span data-ttu-id="28650-118">Указывает, какие источники данных нужно получить.</span><span class="sxs-lookup"><span data-stu-id="28650-118">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="28650-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28650-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28650-120">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="28650-120">AzureActivityLog</span></span> 
- <span data-ttu-id="28650-121">CustomLog</span><span class="sxs-lookup"><span data-stu-id="28650-121">CustomLog</span></span> 
- <span data-ttu-id="28650-122">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="28650-122">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="28650-123">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="28650-123">LinuxSyslog</span></span> 
- <span data-ttu-id="28650-124">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="28650-124">WindowsEvent</span></span> 
- <span data-ttu-id="28650-125">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="28650-125">WindowsPerformanceCounter</span></span>

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

### <span data-ttu-id="28650-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="28650-126">-Name</span></span>
<span data-ttu-id="28650-127">Указывает имя источника данных, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="28650-127">Specifies the name of a data source to get.</span></span>

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

### <span data-ttu-id="28650-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28650-128">-ResourceGroupName</span></span>
<span data-ttu-id="28650-129">Указывает имя группы ресурсов, которая содержит источники данных, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="28650-129">Specifies the name of a resource group that contains data sources to get.</span></span>

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

### <span data-ttu-id="28650-130">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="28650-130">-Workspace</span></span>
<span data-ttu-id="28650-131">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="28650-131">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="28650-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="28650-132">-WorkspaceName</span></span>
<span data-ttu-id="28650-133">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="28650-133">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="28650-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28650-134">CommonParameters</span></span>
<span data-ttu-id="28650-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28650-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28650-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28650-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28650-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28650-137">INPUTS</span></span>

### <span data-ttu-id="28650-138">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="28650-138">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="28650-139">System. String</span><span class="sxs-lookup"><span data-stu-id="28650-139">System.String</span></span>

## <span data-ttu-id="28650-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28650-140">OUTPUTS</span></span>

### <span data-ttu-id="28650-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="28650-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="28650-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="28650-142">NOTES</span></span>
* <span data-ttu-id="28650-143">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="28650-143">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="28650-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28650-144">RELATED LINKS</span></span>

[<span data-ttu-id="28650-145">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="28650-145">Remove-AzOperationalInsightsDataSource</span></span>](./Remove-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="28650-146">Set-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="28650-146">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


