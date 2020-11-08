---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: 81a50a8c805d05b47b934b899eff708031ac6beb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072698"
---
# <span data-ttu-id="54155-101">Get-AzAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="54155-101">Get-AzAutomationDscNodeReport</span></span>

## <span data-ttu-id="54155-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54155-102">SYNOPSIS</span></span>
<span data-ttu-id="54155-103">Возвращает отчеты, отправленные с узла DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="54155-103">Gets reports sent from a DSC node to Automation.</span></span>

## <span data-ttu-id="54155-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54155-104">SYNTAX</span></span>

### <span data-ttu-id="54155-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54155-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="54155-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="54155-106">ByLatest</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="54155-107">ById</span><span class="sxs-lookup"><span data-stu-id="54155-107">ById</span></span>
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54155-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54155-108">DESCRIPTION</span></span>
<span data-ttu-id="54155-109">Командлет **Get-AzAutomationDscNodeReport** получает отчеты от узла DSC нужной конфигурации для Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="54155-109">The **Get-AzAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="54155-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54155-110">EXAMPLES</span></span>

### <span data-ttu-id="54155-111">Пример 1: получение всех отчетов для узла DSC</span><span class="sxs-lookup"><span data-stu-id="54155-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="54155-112">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54155-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="54155-113">Команда хранит этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="54155-113">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="54155-114">Вторая команда получает метаданные для всех отчетов, отправленных с узла DSC с именем Computer14, в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54155-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="54155-115">Команда задает узел с помощью свойства **ID** объекта $node.</span><span class="sxs-lookup"><span data-stu-id="54155-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="54155-116">Пример 2: получение отчета об узле DSC по ИДЕНТИФИКАТОРу отчета</span><span class="sxs-lookup"><span data-stu-id="54155-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="54155-117">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54155-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="54155-118">Команда хранит этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="54155-118">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="54155-119">Вторая команда получает метаданные для отчета, идентифицируемого по указанному ИДЕНТИФИКАТОРу, отправленному с узла DSC с именем Computer14, в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54155-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="54155-120">Пример 3: Получение последнего отчета об узле DSC</span><span class="sxs-lookup"><span data-stu-id="54155-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="54155-121">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54155-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="54155-122">Команда хранит этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="54155-122">The command stores this object in the $Node variable.</span></span>
<span data-ttu-id="54155-123">Вторая команда получает метаданные для последнего отчета, отправленного с узла DSC с именем Computer14, в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="54155-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="54155-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54155-124">PARAMETERS</span></span>

### <span data-ttu-id="54155-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="54155-125">-AutomationAccountName</span></span>
<span data-ttu-id="54155-126">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="54155-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="54155-127">Этот командлет экспортирует отчеты для узла DSC, который принадлежит учетной записи, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="54155-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="54155-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54155-128">-DefaultProfile</span></span>
<span data-ttu-id="54155-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="54155-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54155-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="54155-130">-EndTime</span></span>
<span data-ttu-id="54155-131">Указывает время окончания.</span><span class="sxs-lookup"><span data-stu-id="54155-131">Specifies an end time.</span></span>
<span data-ttu-id="54155-132">Этот командлет получает отчеты, которые были получены до этого времени.</span><span class="sxs-lookup"><span data-stu-id="54155-132">This cmdlet gets reports that Automation received before this time.</span></span>

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

### <span data-ttu-id="54155-133">-ID</span><span class="sxs-lookup"><span data-stu-id="54155-133">-Id</span></span>
<span data-ttu-id="54155-134">Указывает уникальный идентификатор отчета узла DSC для получения этого командлета.</span><span class="sxs-lookup"><span data-stu-id="54155-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

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

### <span data-ttu-id="54155-135">-Последние</span><span class="sxs-lookup"><span data-stu-id="54155-135">-Latest</span></span>
<span data-ttu-id="54155-136">Указывает, что этот командлет получает последний отчет DSC только для указанного узла.</span><span class="sxs-lookup"><span data-stu-id="54155-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

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

### <span data-ttu-id="54155-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="54155-137">-NodeId</span></span>
<span data-ttu-id="54155-138">Указывает уникальный идентификатор узла DSC, для которого этот командлет получает отчеты.</span><span class="sxs-lookup"><span data-stu-id="54155-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="54155-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54155-139">-ResourceGroupName</span></span>
<span data-ttu-id="54155-140">Указывает имя группы ресурсов, содержащей узел DSC, для которого этот командлет получает отчеты.</span><span class="sxs-lookup"><span data-stu-id="54155-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

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

### <span data-ttu-id="54155-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="54155-141">-StartTime</span></span>
<span data-ttu-id="54155-142">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="54155-142">Specifies a start time.</span></span>
<span data-ttu-id="54155-143">Этот командлет получает отчеты о том, что автоматизация была получена после этого времени.</span><span class="sxs-lookup"><span data-stu-id="54155-143">This cmdlet gets reports that Automation received after this time.</span></span>

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

### <span data-ttu-id="54155-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54155-144">CommonParameters</span></span>
<span data-ttu-id="54155-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54155-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54155-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54155-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54155-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54155-147">INPUTS</span></span>

### <span data-ttu-id="54155-148">System. GUID</span><span class="sxs-lookup"><span data-stu-id="54155-148">System.Guid</span></span>

### <span data-ttu-id="54155-149">System. Nullable "1 [[System. DateTimeOffset, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="54155-149">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="54155-150">System. String</span><span class="sxs-lookup"><span data-stu-id="54155-150">System.String</span></span>

## <span data-ttu-id="54155-151">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54155-151">OUTPUTS</span></span>

### <span data-ttu-id="54155-152">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="54155-152">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="54155-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="54155-153">NOTES</span></span>

## <span data-ttu-id="54155-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54155-154">RELATED LINKS</span></span>

[<span data-ttu-id="54155-155">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="54155-155">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="54155-156">Export-AzAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="54155-156">Export-AzAutomationDscNodeReportContent</span></span>](./Export-AzAutomationDscNodeReportContent.md)


