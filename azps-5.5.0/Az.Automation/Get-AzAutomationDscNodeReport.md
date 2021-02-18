---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: cc7beb921e09a2cdf1568e9cb693dd01f059e562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239632"
---
# <span data-ttu-id="4205f-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="4205f-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="4205f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4205f-102">SYNOPSIS</span></span>
<span data-ttu-id="4205f-103">Возвращает отчеты, отправленные с узла DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="4205f-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="4205f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4205f-104">SYNTAX</span></span>

### <span data-ttu-id="4205f-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4205f-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4205f-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="4205f-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4205f-107">ById</span><span class="sxs-lookup"><span data-stu-id="4205f-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4205f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4205f-108">DESCRIPTION</span></span>
<span data-ttu-id="4205f-109">Cmdlet **Get-AzAutomationDscNodeReport** получает отчеты, отправленные с узла APS Desired State Configuration (DSC) в автоматизацию Azure.</span><span class="sxs-lookup"><span data-stu-id="4205f-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="4205f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4205f-110">EXAMPLES</span></span>

### <span data-ttu-id="4205f-111">Пример 1. Получить все отчеты для узла DSC</span><span class="sxs-lookup"><span data-stu-id="4205f-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="4205f-112">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4205f-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4205f-113">Эта команда сохраняет этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="4205f-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="4205f-114">Вторая команда получает метаданные для всех отчетов, отправленных с узла DSC "Компьютер14" в учетную запись автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4205f-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="4205f-115">Команда определяет узел с помощью свойства **"ИД"** объекта $Node.</span><span class="sxs-lookup"><span data-stu-id="4205f-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="4205f-116">Пример 2. Получить отчет для узла DSC по ИД отчета</span><span class="sxs-lookup"><span data-stu-id="4205f-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="4205f-117">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4205f-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4205f-118">Эта команда сохраняет этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="4205f-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="4205f-119">Вторая команда получает метаданные отчета, указанного по указанному ИД, отправленного с узла DSC Computer14 в учетную запись автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4205f-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4205f-120">Пример 3. Получить последний отчет для узла DSC</span><span class="sxs-lookup"><span data-stu-id="4205f-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="4205f-121">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4205f-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="4205f-122">Команда сохраняет этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="4205f-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="4205f-123">Вторая команда получает метаданные для последнего отчета, отправленного с узла DSC "Компьютер14" в учетную запись автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4205f-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4205f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4205f-124">PARAMETERS</span></span>

### <span data-ttu-id="4205f-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4205f-125">-AutomationAccountName</span></span>
<span data-ttu-id="4205f-126">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4205f-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="4205f-127">Этот cmdlet экспортирует отчеты для узла DSC, принадлежаного учетной записи, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="4205f-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4205f-128">-DefaultProfile</span></span>
<span data-ttu-id="4205f-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4205f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4205f-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="4205f-130">-EndTime</span></span>
<span data-ttu-id="4205f-131">Время окончания.</span><span class="sxs-lookup"><span data-stu-id="4205f-131">Specifies an end time.</span></span>
<span data-ttu-id="4205f-132">Этот cmdlet получает отчеты, полученные автоматизацией до этого времени.</span><span class="sxs-lookup"><span data-stu-id="4205f-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-133">-Id</span><span class="sxs-lookup"><span data-stu-id="4205f-133">-Id</span></span>
<span data-ttu-id="4205f-134">Указывает уникальный код отчета узла DSC, который должен получить этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4205f-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-135">-Последняя версия</span><span class="sxs-lookup"><span data-stu-id="4205f-135">-Latest</span></span>
<span data-ttu-id="4205f-136">Указывает на то, что этот cmdlet получает последний отчет DSC только для указанного узла.</span><span class="sxs-lookup"><span data-stu-id="4205f-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="4205f-137">-NodeId</span></span>
<span data-ttu-id="4205f-138">Указывает уникальный код узла DSC, для которого этот cmdlet получает отчеты.</span><span class="sxs-lookup"><span data-stu-id="4205f-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4205f-139">-ResourceGroupName</span></span>
<span data-ttu-id="4205f-140">Имя группы ресурсов, которая содержит узел DSC, для которого этот cmdlet получает отчеты.</span><span class="sxs-lookup"><span data-stu-id="4205f-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4205f-141">-StartTime</span></span>
<span data-ttu-id="4205f-142">Время начала.</span><span class="sxs-lookup"><span data-stu-id="4205f-142">Specifies a start time.</span></span>
<span data-ttu-id="4205f-143">Этот cmdlet получает отчеты, полученные автоматизацией после этого времени.</span><span class="sxs-lookup"><span data-stu-id="4205f-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4205f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4205f-144">CommonParameters</span></span>
<span data-ttu-id="4205f-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4205f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4205f-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4205f-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4205f-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4205f-147">INPUTS</span></span>

### <span data-ttu-id="4205f-148">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4205f-148">System.Guid</span></span>

### <span data-ttu-id="4205f-149">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4205f-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4205f-150">System.String</span><span class="sxs-lookup"><span data-stu-id="4205f-150">System.String</span></span>

## <span data-ttu-id="4205f-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4205f-151">OUTPUTS</span></span>

### <span data-ttu-id="4205f-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span><span class="sxs-lookup"><span data-stu-id="4205f-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="4205f-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4205f-153">NOTES</span></span>

## <span data-ttu-id="4205f-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4205f-154">RELATED LINKS</span></span>

[<span data-ttu-id="4205f-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="4205f-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="4205f-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="4205f-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


