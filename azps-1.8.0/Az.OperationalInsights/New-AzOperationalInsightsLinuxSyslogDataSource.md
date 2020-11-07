---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: a0268931d276c74560acd5cb04cac1d1e5778b81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729844"
---
# <span data-ttu-id="ff817-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="ff817-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="ff817-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff817-102">SYNOPSIS</span></span>
<span data-ttu-id="ff817-103">Добавляет источник данных на компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="ff817-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="ff817-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff817-104">SYNTAX</span></span>

### <span data-ttu-id="ff817-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff817-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff817-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ff817-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff817-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff817-107">DESCRIPTION</span></span>
<span data-ttu-id="ff817-108">Командлет **New-AzOperationalInsightsLinuxSyslogDataSource** добавляет источник данных syslog на подключенные компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="ff817-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="ff817-109">Azure Operational Insights может собирать данные syslog.</span><span class="sxs-lookup"><span data-stu-id="ff817-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="ff817-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff817-110">EXAMPLES</span></span>

## <span data-ttu-id="ff817-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff817-111">PARAMETERS</span></span>

### <span data-ttu-id="ff817-112">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="ff817-112">-CollectAlert</span></span>
<span data-ttu-id="ff817-113">Указывает, что оперативная аналитика собирает сообщения оповещений.</span><span class="sxs-lookup"><span data-stu-id="ff817-113">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="ff817-114">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="ff817-114">-CollectCritical</span></span>
<span data-ttu-id="ff817-115">Указывает, что оперативная аналитика собирает важные сообщения.</span><span class="sxs-lookup"><span data-stu-id="ff817-115">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="ff817-116">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="ff817-116">-CollectDebug</span></span>
<span data-ttu-id="ff817-117">Указывает, что оперативная аналитика собирает сообщения об отладке.</span><span class="sxs-lookup"><span data-stu-id="ff817-117">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="ff817-118">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="ff817-118">-CollectEmergency</span></span>
<span data-ttu-id="ff817-119">Указывает на то, что оперативная аналитика собирает сообщения для экстренного реагирования.</span><span class="sxs-lookup"><span data-stu-id="ff817-119">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="ff817-120">-CollectError</span><span class="sxs-lookup"><span data-stu-id="ff817-120">-CollectError</span></span>
<span data-ttu-id="ff817-121">Указывает на то, что оперативная аналитика собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="ff817-121">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="ff817-122">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="ff817-122">-CollectInformational</span></span>
<span data-ttu-id="ff817-123">Указывает, что при работе с аналитической аналитикой собираются информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="ff817-123">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="ff817-124">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="ff817-124">-CollectNotice</span></span>
<span data-ttu-id="ff817-125">Указывает, что оперативная аналитика собирает сообщения с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="ff817-125">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="ff817-126">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="ff817-126">-CollectWarning</span></span>
<span data-ttu-id="ff817-127">Указывает на то, что в syslog есть предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="ff817-127">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="ff817-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff817-128">-DefaultProfile</span></span>
<span data-ttu-id="ff817-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ff817-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ff817-130">-Ссуда</span><span class="sxs-lookup"><span data-stu-id="ff817-130">-Facility</span></span>
<span data-ttu-id="ff817-131">Указывает код оборудования.</span><span class="sxs-lookup"><span data-stu-id="ff817-131">Specifies a facility code.</span></span>

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

### <span data-ttu-id="ff817-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ff817-132">-Force</span></span>
<span data-ttu-id="ff817-133">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ff817-133">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff817-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ff817-134">-Name</span></span>
<span data-ttu-id="ff817-135">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="ff817-135">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="ff817-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff817-136">-ResourceGroupName</span></span>
<span data-ttu-id="ff817-137">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="ff817-137">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="ff817-138">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="ff817-138">-Workspace</span></span>
<span data-ttu-id="ff817-139">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff817-139">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff817-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ff817-140">-WorkspaceName</span></span>
<span data-ttu-id="ff817-141">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ff817-141">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="ff817-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff817-142">-Confirm</span></span>
<span data-ttu-id="ff817-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ff817-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff817-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff817-144">-WhatIf</span></span>
<span data-ttu-id="ff817-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ff817-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff817-146">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ff817-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff817-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff817-147">CommonParameters</span></span>
<span data-ttu-id="ff817-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff817-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff817-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff817-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff817-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff817-150">INPUTS</span></span>

### <span data-ttu-id="ff817-151">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ff817-151">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ff817-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ff817-152">System.String</span></span>

## <span data-ttu-id="ff817-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff817-153">OUTPUTS</span></span>

### <span data-ttu-id="ff817-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="ff817-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="ff817-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff817-155">NOTES</span></span>

## <span data-ttu-id="ff817-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff817-156">RELATED LINKS</span></span>

[<span data-ttu-id="ff817-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="ff817-157">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="ff817-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="ff817-158">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


