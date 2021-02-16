---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D6CBDF09-E243-425B-8677-256163A6DFBF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinuxsyslogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinuxSyslogDataSource.md
ms.openlocfilehash: 12d9ff89ea87ae24d3817cdd3ec0b706582e4849
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100220809"
---
# <span data-ttu-id="35688-101">New-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="35688-101">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>

## <span data-ttu-id="35688-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35688-102">SYNOPSIS</span></span>
<span data-ttu-id="35688-103">Добавляет источник данных на компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="35688-103">Adds a data source to Linux computers.</span></span>

## <span data-ttu-id="35688-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35688-104">SYNTAX</span></span>

### <span data-ttu-id="35688-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35688-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Facility] <String> [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError]
 [-CollectWarning] [-CollectNotice] [-CollectDebug] [-CollectInformational] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35688-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="35688-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsLinuxSyslogDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Facility] <String>
 [-CollectEmergency] [-CollectAlert] [-CollectCritical] [-CollectError] [-CollectWarning] [-CollectNotice]
 [-CollectDebug] [-CollectInformational] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35688-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35688-107">DESCRIPTION</span></span>
<span data-ttu-id="35688-108">**Новый-AzOperationalInsightsLinuxSyslogDataSource** добавляет источник данных syslog к подключенным компьютерам Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="35688-108">The **New-AzOperationalInsightsLinuxSyslogDataSource** cmdlet adds a syslog data source to connected Linux computers in a workspace.</span></span>
<span data-ttu-id="35688-109">Azure Operational Insights может собирать данные для слоги.</span><span class="sxs-lookup"><span data-stu-id="35688-109">Azure Operational Insights can collect syslog data.</span></span>

## <span data-ttu-id="35688-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35688-110">EXAMPLES</span></span>

### <span data-ttu-id="35688-111">Пример 1. Создание источников данных для слоги</span><span class="sxs-lookup"><span data-stu-id="35688-111">Example 1: Create syslog data sources</span></span>
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

## <span data-ttu-id="35688-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35688-112">PARAMETERS</span></span>

### <span data-ttu-id="35688-113">-CollectAlert</span><span class="sxs-lookup"><span data-stu-id="35688-113">-CollectAlert</span></span>
<span data-ttu-id="35688-114">Указывает на то, что операционная информация собирает оповещения.</span><span class="sxs-lookup"><span data-stu-id="35688-114">Indicates that Operational Insights collects alert messages.</span></span>

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

### <span data-ttu-id="35688-115">-CollectCritical</span><span class="sxs-lookup"><span data-stu-id="35688-115">-CollectCritical</span></span>
<span data-ttu-id="35688-116">Указывает на то, что операционная информация собирает критически важные сообщения.</span><span class="sxs-lookup"><span data-stu-id="35688-116">Indicates that Operational Insights collects critical messages.</span></span>

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

### <span data-ttu-id="35688-117">-CollectDebug</span><span class="sxs-lookup"><span data-stu-id="35688-117">-CollectDebug</span></span>
<span data-ttu-id="35688-118">Указывает на то, что операционная информация собирает сообщения отлагки.</span><span class="sxs-lookup"><span data-stu-id="35688-118">Indicates that Operational Insights collects debug messages.</span></span>

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

### <span data-ttu-id="35688-119">-CollectEmergency</span><span class="sxs-lookup"><span data-stu-id="35688-119">-CollectEmergency</span></span>
<span data-ttu-id="35688-120">Указывает на то, что операционная информация собирает сообщения в экстренных службах.</span><span class="sxs-lookup"><span data-stu-id="35688-120">Indicates that Operational Insights collects emergency messages.</span></span>

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

### <span data-ttu-id="35688-121">-CollectError</span><span class="sxs-lookup"><span data-stu-id="35688-121">-CollectError</span></span>
<span data-ttu-id="35688-122">Указывает на то, что операционная информация собирает сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="35688-122">Indicates that Operational Insights collects error messages.</span></span>

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

### <span data-ttu-id="35688-123">-CollectInformational</span><span class="sxs-lookup"><span data-stu-id="35688-123">-CollectInformational</span></span>
<span data-ttu-id="35688-124">Указывает на то, что операционная информация собирает информационные сообщения.</span><span class="sxs-lookup"><span data-stu-id="35688-124">Indicates that Operational Insights collects informational messages.</span></span>

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

### <span data-ttu-id="35688-125">-CollectNotice</span><span class="sxs-lookup"><span data-stu-id="35688-125">-CollectNotice</span></span>
<span data-ttu-id="35688-126">Указывает на то, что операционная информация собирает сообщения с уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="35688-126">Indicates that Operational Insights collects notice messages.</span></span>

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

### <span data-ttu-id="35688-127">-CollectWarning</span><span class="sxs-lookup"><span data-stu-id="35688-127">-CollectWarning</span></span>
<span data-ttu-id="35688-128">Указывает на то, что в этом слоге содержатся предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="35688-128">Indicates that the syslog includes warning messages.</span></span>

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

### <span data-ttu-id="35688-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35688-129">-DefaultProfile</span></span>
<span data-ttu-id="35688-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35688-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35688-131">-Facility</span><span class="sxs-lookup"><span data-stu-id="35688-131">-Facility</span></span>
<span data-ttu-id="35688-132">Определяет код объекта.</span><span class="sxs-lookup"><span data-stu-id="35688-132">Specifies a facility code.</span></span>

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

### <span data-ttu-id="35688-133">-Force</span><span class="sxs-lookup"><span data-stu-id="35688-133">-Force</span></span>
<span data-ttu-id="35688-134">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="35688-134">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35688-135">-Name</span><span class="sxs-lookup"><span data-stu-id="35688-135">-Name</span></span>
<span data-ttu-id="35688-136">Указывает имя источника данных.</span><span class="sxs-lookup"><span data-stu-id="35688-136">Specifies a name for the data source.</span></span> <span data-ttu-id="35688-137">Имя не используется на портале Azure, и любую строку можно использовать, если она является уникальной.</span><span class="sxs-lookup"><span data-stu-id="35688-137">The name is not exposed in the Azure Portal and any string can be used as long as it is unique.</span></span>

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

### <span data-ttu-id="35688-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35688-138">-ResourceGroupName</span></span>
<span data-ttu-id="35688-139">Имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="35688-139">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="35688-140">-Workspace</span><span class="sxs-lookup"><span data-stu-id="35688-140">-Workspace</span></span>
<span data-ttu-id="35688-141">Определяет рабочее пространство, в котором выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35688-141">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="35688-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35688-142">-WorkspaceName</span></span>
<span data-ttu-id="35688-143">Указывает имя рабочей области, в которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35688-143">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="35688-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35688-144">-Confirm</span></span>
<span data-ttu-id="35688-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35688-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35688-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35688-146">-WhatIf</span></span>
<span data-ttu-id="35688-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35688-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35688-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="35688-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35688-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35688-149">CommonParameters</span></span>
<span data-ttu-id="35688-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35688-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35688-151">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35688-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35688-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35688-152">INPUTS</span></span>

### <span data-ttu-id="35688-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="35688-153">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="35688-154">System.String</span><span class="sxs-lookup"><span data-stu-id="35688-154">System.String</span></span>

## <span data-ttu-id="35688-155">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35688-155">OUTPUTS</span></span>

### <span data-ttu-id="35688-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="35688-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="35688-157">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35688-157">NOTES</span></span>

## <span data-ttu-id="35688-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35688-158">RELATED LINKS</span></span>

[<span data-ttu-id="35688-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="35688-159">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="35688-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="35688-160">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Enable-AzOperationalInsightsLinuxSyslogCollection.md)


