---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: de0864f91ccda3bbf30ec60d06aba60f992baf26
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904666"
---
# <span data-ttu-id="38c3b-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="38c3b-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="38c3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38c3b-102">SYNOPSIS</span></span>
<span data-ttu-id="38c3b-103">Добавляет источник данных на компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="38c3b-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="38c3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38c3b-104">SYNTAX</span></span>

### <span data-ttu-id="38c3b-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38c3b-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38c3b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="38c3b-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38c3b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38c3b-107">DESCRIPTION</span></span>
<span data-ttu-id="38c3b-108">Командлет **New-AzOperationalInsightsLinuxSyslogDataSource** добавляет источник данных syslog на подключенные компьютеры Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="38c3b-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="38c3b-109">Azure Operational Insights может собирать данные syslog.</span><span class="sxs-lookup"><span data-stu-id="38c3b-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="38c3b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38c3b-110">EXAMPLES</span></span>

### <span data-ttu-id="38c3b-111">Пример 1: создание источников данных syslog</span><span class="sxs-lookup"><span data-stu-id="38c3b-111">Example 1: Create syslog data sources</span></span>
```
$FacilityNames       = @()
$FacilityNames      += 'auth'
$FacilityNames      += 'authpriv'
$FacilityNames      += 'cron'
$FacilityNames      += 'daemon'
$FacilityNames      += 'ftp'
$FacilityNames      += 'kern'
$FacilityNames      += 'mail'
$FacilityNames      += 'syslog'
$FacilityNames      += 'user'
$FacilityNames      += 'uucp'
$ResourceGroupName   = 'MyResourceGroup'
$WorkspaceName       = 'MyWorkspaceName'

$Count = 0
foreach ($FacilityName in $FacilityNames) {
    $Count++
    $null = New-AzOperationalInsightsLinuxSyslogDataSource `
    -ResourceGroupName $ResourceGroupName `
    -WorkspaceName $WorkspaceName `
    -Name "Linux-syslog-$($Count)" `
    -Facility $FacilityName `
    -CollectEmergency `
    -CollectAlert `
    -CollectCritical `
    -CollectError `
    -CollectWarning `
    -CollectNotice `
    -CollectDebug `
    -CollectInformational
}

Get-AzOperationalInsightsDataSource `
   -ResourceGroupName $ResourceGroupName `
   -WorkspaceName $WorkspaceName `
   -Kind 'LinuxSyslog'
```

## <span data-ttu-id="38c3b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38c3b-112">PARAMETERS</span></span>

### <span data-ttu-id="38c3b-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="38c3b-113">-CollectAlert</span></span>
<span data-ttu-id="38c3b-114">Указывает, что оперативная аналитика собирает сообщения оповещений.</span><span class="sxs-lookup"><span data-stu-id="38c3b-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="38c3b-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="38c3b-115">-CollectCritical</span></span>
<span data-ttu-id="38c3b-116">Указывает, что оперативная аналитика собирает важные сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c3b-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="38c3b-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="38c3b-117">-CollectDebug</span></span>
<span data-ttu-id="38c3b-118">Указывает, что оперативная аналитика собирает сообщения об отладке.</span><span class="sxs-lookup"><span data-stu-id="38c3b-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="38c3b-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="38c3b-119">-CollectEmergency</span></span>
<span data-ttu-id="38c3b-120">Указывает на то, что оперативная аналитика собирает сообщения для экстренного реагирования.</span><span class="sxs-lookup"><span data-stu-id="38c3b-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="38c3b-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="38c3b-121">-CollectError</span></span>
<span data-ttu-id="38c3b-122">Указывает на то, что оперативная аналитика собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="38c3b-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="38c3b-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="38c3b-123">-CollectInformational</span></span>
<span data-ttu-id="38c3b-124">Указывает, что при работе с аналитической аналитикой собираются информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c3b-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="38c3b-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="38c3b-125">-CollectNotice</span></span>
<span data-ttu-id="38c3b-126">Указывает, что оперативная аналитика собирает сообщения с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="38c3b-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="38c3b-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="38c3b-127">-CollectWarning</span></span>
<span data-ttu-id="38c3b-128">Указывает на то, что в syslog есть предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="38c3b-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="38c3b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c3b-129">-DefaultProfile</span></span>
<span data-ttu-id="38c3b-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="38c3b-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38c3b-131">-Ссуда</span><span class="sxs-lookup"><span data-stu-id="38c3b-131">-Facility</span></span>
<span data-ttu-id="38c3b-132">Указывает код оборудования.</span><span class="sxs-lookup"><span data-stu-id="38c3b-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="38c3b-133">-Force</span><span class="sxs-lookup"><span data-stu-id="38c3b-133">-Force</span></span>
<span data-ttu-id="38c3b-134">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="38c3b-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38c3b-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38c3b-135">-Name</span></span>
<span data-ttu-id="38c3b-136">Задает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="38c3b-136">Specifies a name for the data source.</span></span> <span data-ttu-id="38c3b-137">Имя не отображается на портале Azure, и любая строка может быть использована в том случае, если она является уникальной.</span><span class="sxs-lookup"><span data-stu-id="38c3b-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="38c3b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c3b-138">-ResourceGroupName</span></span>
<span data-ttu-id="38c3b-139">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="38c3b-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="38c3b-140">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="38c3b-140">-Workspace</span></span>
<span data-ttu-id="38c3b-141">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="38c3b-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="38c3b-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="38c3b-142">-WorkspaceName</span></span>
<span data-ttu-id="38c3b-143">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="38c3b-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="38c3b-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38c3b-144">-Confirm</span></span>
<span data-ttu-id="38c3b-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38c3b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38c3b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38c3b-146">-WhatIf</span></span>
<span data-ttu-id="38c3b-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38c3b-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38c3b-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38c3b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38c3b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c3b-149">CommonParameters</span></span>
<span data-ttu-id="38c3b-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38c3b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c3b-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c3b-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c3b-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38c3b-152">INPUTS</span></span>

### <span data-ttu-id="38c3b-153">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="38c3b-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="38c3b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="38c3b-154">System.String</span></span>

## <span data-ttu-id="38c3b-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38c3b-155">OUTPUTS</span></span>

### <span data-ttu-id="38c3b-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="38c3b-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="38c3b-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="38c3b-157">NOTES</span></span>

## <span data-ttu-id="38c3b-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38c3b-158">RELATED LINKS</span></span>

[<span data-ttu-id="38c3b-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="38c3b-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="38c3b-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="38c3b-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


