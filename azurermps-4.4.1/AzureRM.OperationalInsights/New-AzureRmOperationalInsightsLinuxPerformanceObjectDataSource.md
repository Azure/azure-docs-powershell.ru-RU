---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94F3FA8-08FD-4B25-B634-8E2EEBDDE36E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource.md
ms.openlocfilehash: 1e9114b9f6b62f6900c975b39e5f8c67b4d9051a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562323"
---
# <span data-ttu-id="5a928-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span><span class="sxs-lookup"><span data-stu-id="5a928-101">New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource</span></span>

## <span data-ttu-id="5a928-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a928-102">SYNOPSIS</span></span>
<span data-ttu-id="5a928-103">Добавляет счетчики производительности на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5a928-103">Adds performance counters to all Linux computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a928-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a928-104">SYNTAX</span></span>

### <span data-ttu-id="5a928-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a928-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-Name] <String> [-ObjectName] <String> [-CounterNames] <String[]>
 [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a928-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5a928-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-ObjectName] <String> [-CounterNames] <String[]> [-InstanceName <String>] [-IntervalSeconds <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a928-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a928-107">DESCRIPTION</span></span>
<span data-ttu-id="5a928-108">Командлет **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** добавляет счетчики производительности, с помощью которых оперативная аналитика Azure собирает данные на все компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5a928-108">The **New-AzureRmOperationalInsightsLinuxPerformanceObjectDataSource** cmdlet adds performance counters from which Azure Operational Insights collects data to all Linux computers in a workspace.</span></span>

## <span data-ttu-id="5a928-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a928-109">EXAMPLES</span></span>

## <span data-ttu-id="5a928-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a928-110">PARAMETERS</span></span>

### <span data-ttu-id="5a928-111">-CounterNames</span><span class="sxs-lookup"><span data-stu-id="5a928-111">-CounterNames</span></span>
<span data-ttu-id="5a928-112">Указывает массив имен счетчиков.</span><span class="sxs-lookup"><span data-stu-id="5a928-112">Specifies an array of names of counters.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5a928-113">-Force</span></span>
<span data-ttu-id="5a928-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5a928-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-115">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="5a928-115">-InstanceName</span></span>
<span data-ttu-id="5a928-116">Указывает имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5a928-116">Specifies an instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-117">-IntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="5a928-117">-IntervalSeconds</span></span>
<span data-ttu-id="5a928-118">Указывает интервал сбора.</span><span class="sxs-lookup"><span data-stu-id="5a928-118">Specifies the interval of collection.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5a928-119">-Name</span></span>
<span data-ttu-id="5a928-120">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="5a928-120">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="5a928-121">-ObjectName</span><span class="sxs-lookup"><span data-stu-id="5a928-121">-ObjectName</span></span>
<span data-ttu-id="5a928-122">Указывает имя объекта.</span><span class="sxs-lookup"><span data-stu-id="5a928-122">Specifies the name of an object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a928-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a928-124">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="5a928-124">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="5a928-125">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="5a928-125">-Workspace</span></span>
<span data-ttu-id="5a928-126">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a928-126">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5a928-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5a928-127">-WorkspaceName</span></span>
<span data-ttu-id="5a928-128">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5a928-128">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5a928-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a928-129">-Confirm</span></span>
<span data-ttu-id="5a928-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a928-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a928-131">-WhatIf</span></span>
<span data-ttu-id="5a928-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a928-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a928-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a928-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a928-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a928-134">-DefaultProfile</span></span>
<span data-ttu-id="5a928-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a928-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a928-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a928-136">CommonParameters</span></span>
<span data-ttu-id="5a928-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a928-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a928-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a928-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a928-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a928-139">INPUTS</span></span>

### <span data-ttu-id="5a928-140">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a928-140">PSWorkspace</span></span>
<span data-ttu-id="5a928-141">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5a928-141">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="5a928-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a928-142">OUTPUTS</span></span>

### <span data-ttu-id="5a928-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="5a928-143">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="5a928-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a928-144">NOTES</span></span>

## <span data-ttu-id="5a928-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a928-145">RELATED LINKS</span></span>

[<span data-ttu-id="5a928-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="5a928-146">Disable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="5a928-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="5a928-147">Enable-AzureRmOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxPerformanceCollection.md)


