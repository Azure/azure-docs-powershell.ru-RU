---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 1F094EBA-E4AE-4B3E-BA20-858818C6FD12
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 057437e55fd7877154343bdbfc5f25d216412b8e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564692"
---
# <span data-ttu-id="b90e9-101">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b90e9-101">Get-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="b90e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b90e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b90e9-103">Получение источников данных в области "анализ журналов Azure".</span><span class="sxs-lookup"><span data-stu-id="b90e9-103">Get datasources under Azure Log Analytics workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b90e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b90e9-104">SYNTAX</span></span>

### <span data-ttu-id="b90e9-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b90e9-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-106">ByWorkspaceObjectByName</span><span class="sxs-lookup"><span data-stu-id="b90e9-106">ByWorkspaceObjectByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-107">ByWorkspaceObjectByKind</span><span class="sxs-lookup"><span data-stu-id="b90e9-107">ByWorkspaceObjectByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-Workspace] <PSWorkspace>] [[-Kind] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-108">ByWorkspaceNameByName</span><span class="sxs-lookup"><span data-stu-id="b90e9-108">ByWorkspaceNameByName</span></span>
```
Get-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b90e9-109">ByWorkspaceNameByKind</span><span class="sxs-lookup"><span data-stu-id="b90e9-109">ByWorkspaceNameByKind</span></span>
```
Get-AzureRmOperationalInsightsDataSource [[-ResourceGroupName] <String>] [[-WorkspaceName] <String>]
 [-Kind] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b90e9-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b90e9-110">DESCRIPTION</span></span>
<span data-ttu-id="b90e9-111">Командлет **Get-AzureRmOperationalInsightsDataSource** получает источники данных.</span><span class="sxs-lookup"><span data-stu-id="b90e9-111">The **Get-AzureRmOperationalInsightsDataSource** cmdlet gets data sources.</span></span>
<span data-ttu-id="b90e9-112">Вы можете указать источник данных для получения.</span><span class="sxs-lookup"><span data-stu-id="b90e9-112">You can specify a data source to get.</span></span>
<span data-ttu-id="b90e9-113">Вы можете отфильтровать результаты в зависимости от типа источника данных.</span><span class="sxs-lookup"><span data-stu-id="b90e9-113">You can filter the results based on the kind of data source.</span></span>

## <span data-ttu-id="b90e9-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b90e9-114">EXAMPLES</span></span>

## <span data-ttu-id="b90e9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b90e9-115">PARAMETERS</span></span>

### <span data-ttu-id="b90e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b90e9-116">-DefaultProfile</span></span>
<span data-ttu-id="b90e9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b90e9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b90e9-118">-Видах</span><span class="sxs-lookup"><span data-stu-id="b90e9-118">-Kind</span></span>
<span data-ttu-id="b90e9-119">Указывает, какие источники данных нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b90e9-119">Specifies the kind of data sources to get.</span></span>
<span data-ttu-id="b90e9-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b90e9-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b90e9-121">AzureActivityLog</span><span class="sxs-lookup"><span data-stu-id="b90e9-121">AzureActivityLog</span></span> 
- <span data-ttu-id="b90e9-122">CustomLog</span><span class="sxs-lookup"><span data-stu-id="b90e9-122">CustomLog</span></span> 
- <span data-ttu-id="b90e9-123">LinuxPerformanceObject</span><span class="sxs-lookup"><span data-stu-id="b90e9-123">LinuxPerformanceObject</span></span> 
- <span data-ttu-id="b90e9-124">LinuxSyslog</span><span class="sxs-lookup"><span data-stu-id="b90e9-124">LinuxSyslog</span></span> 
- <span data-ttu-id="b90e9-125">WindowsEvent</span><span class="sxs-lookup"><span data-stu-id="b90e9-125">WindowsEvent</span></span> 
- <span data-ttu-id="b90e9-126">WindowsPerformanceCounter</span><span class="sxs-lookup"><span data-stu-id="b90e9-126">WindowsPerformanceCounter</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 
Accepted values: AzureAuditLog, AzureActivityLog, CustomLog, LinuxPerformanceObject, LinuxSyslog, WindowsEvent, WindowsPerformanceCounter

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b90e9-127">-Name</span></span>
<span data-ttu-id="b90e9-128">Указывает имя источника данных, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b90e9-128">Specifies the name of a data source to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b90e9-129">-ResourceGroupName</span></span>
<span data-ttu-id="b90e9-130">Указывает имя группы ресурсов, которая содержит источники данных, которые требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b90e9-130">Specifies the name of a resource group that contains data sources to get.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-131">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="b90e9-131">-Workspace</span></span>
<span data-ttu-id="b90e9-132">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b90e9-132">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObjectByKind
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b90e9-133">-WorkspaceName</span></span>
<span data-ttu-id="b90e9-134">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b90e9-134">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByWorkspaceNameByKind
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b90e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b90e9-135">CommonParameters</span></span>
<span data-ttu-id="b90e9-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b90e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b90e9-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b90e9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b90e9-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b90e9-138">INPUTS</span></span>

### <span data-ttu-id="b90e9-139">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b90e9-139">PSWorkspace</span></span>
<span data-ttu-id="b90e9-140">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b90e9-140">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

### <span data-ttu-id="b90e9-141">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b90e9-141">PSWorkspace</span></span>
<span data-ttu-id="b90e9-142">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b90e9-142">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="b90e9-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b90e9-143">OUTPUTS</span></span>

### <span data-ttu-id="b90e9-144">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span><span class="sxs-lookup"><span data-stu-id="b90e9-144">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource]</span></span>

### <span data-ttu-id="b90e9-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="b90e9-145">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="b90e9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b90e9-146">NOTES</span></span>
* <span data-ttu-id="b90e9-147">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="b90e9-147">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="b90e9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b90e9-148">RELATED LINKS</span></span>

[<span data-ttu-id="b90e9-149">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b90e9-149">Remove-AzureRmOperationalInsightsDataSource</span></span>](./Remove-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="b90e9-150">Set-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="b90e9-150">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


