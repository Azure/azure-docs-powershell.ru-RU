---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 5729daec656c7f99ac7f4c4c9440e090217c315d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565200"
---
# <span data-ttu-id="e6827-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="e6827-101">New-AzureRmOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="e6827-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6827-102">SYNOPSIS</span></span>
<span data-ttu-id="e6827-103">Добавляет источник данных на компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="e6827-103">Adds a data source to Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6827-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6827-104">SYNTAX</span></span>

### <span data-ttu-id="e6827-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6827-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6827-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e6827-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning]
 [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6827-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6827-107">DESCRIPTION</span></span>
<span data-ttu-id="e6827-108">Командлет **New-AzureRmOperationalInsightsLinuxSyslogDataSource** добавляет источник данных syslog на подключенные компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e6827-108">The **New-AzureRmOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="e6827-109">Azure Operational Insights может собирать данные syslog.</span><span class="sxs-lookup"><span data-stu-id="e6827-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="e6827-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6827-110">EXAMPLES</span></span>

## <span data-ttu-id="e6827-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6827-111">PARAMETERS</span></span>

### <span data-ttu-id="e6827-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="e6827-112">-CollectAlert</span></span>
<span data-ttu-id="e6827-113">Указывает, что оперативная аналитика собирает сообщения оповещений.</span><span class="sxs-lookup"><span data-stu-id="e6827-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="e6827-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="e6827-114">-CollectCritical</span></span>
<span data-ttu-id="e6827-115">Указывает, что оперативная аналитика собирает важные сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6827-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="e6827-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="e6827-116">-CollectDebug</span></span>
<span data-ttu-id="e6827-117">Указывает, что оперативная аналитика собирает сообщения об отладке.</span><span class="sxs-lookup"><span data-stu-id="e6827-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="e6827-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="e6827-118">-CollectEmergency</span></span>
<span data-ttu-id="e6827-119">Указывает на то, что оперативная аналитика собирает сообщения для экстренного реагирования.</span><span class="sxs-lookup"><span data-stu-id="e6827-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="e6827-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="e6827-120">-CollectError</span></span>
<span data-ttu-id="e6827-121">Указывает на то, что оперативная аналитика собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="e6827-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="e6827-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="e6827-122">-CollectInformational</span></span>
<span data-ttu-id="e6827-123">Указывает, что при работе с аналитической аналитикой собираются информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6827-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="e6827-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="e6827-124">-CollectNotice</span></span>
<span data-ttu-id="e6827-125">Указывает, что оперативная аналитика собирает сообщения с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="e6827-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="e6827-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="e6827-126">-CollectWarning</span></span>
<span data-ttu-id="e6827-127">Указывает на то, что в syslog есть предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="e6827-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="e6827-128">-Ссуда</span><span class="sxs-lookup"><span data-stu-id="e6827-128">-Facility</span></span>
<span data-ttu-id="e6827-129">Указывает код оборудования.</span><span class="sxs-lookup"><span data-stu-id="e6827-129">Specifies a facility code.</span></span>

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

### <span data-ttu-id="e6827-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e6827-130">-Force</span></span>
<span data-ttu-id="e6827-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6827-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e6827-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6827-132">-Name</span></span>
<span data-ttu-id="e6827-133">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="e6827-133">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="e6827-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6827-134">-ResourceGroupName</span></span>
<span data-ttu-id="e6827-135">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="e6827-135">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e6827-136">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="e6827-136">-Workspace</span></span>
<span data-ttu-id="e6827-137">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e6827-137">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e6827-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e6827-138">-WorkspaceName</span></span>
<span data-ttu-id="e6827-139">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e6827-139">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e6827-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6827-140">-Confirm</span></span>
<span data-ttu-id="e6827-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6827-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6827-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6827-142">-WhatIf</span></span>
<span data-ttu-id="e6827-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6827-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6827-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6827-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6827-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6827-145">-DefaultProfile</span></span>
<span data-ttu-id="e6827-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6827-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6827-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6827-147">CommonParameters</span></span>
<span data-ttu-id="e6827-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6827-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6827-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6827-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6827-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6827-150">INPUTS</span></span>

### <span data-ttu-id="e6827-151">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e6827-151">PSWorkspace</span></span>
<span data-ttu-id="e6827-152">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e6827-152">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="e6827-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6827-153">OUTPUTS</span></span>

### <span data-ttu-id="e6827-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e6827-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e6827-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6827-155">NOTES</span></span>

## <span data-ttu-id="e6827-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6827-156">RELATED LINKS</span></span>

[<span data-ttu-id="e6827-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="e6827-157">Disable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="e6827-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="e6827-158">Enable-AzureRmOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzureRmOperationalInsightsLinuxSyslogCollection.md)


