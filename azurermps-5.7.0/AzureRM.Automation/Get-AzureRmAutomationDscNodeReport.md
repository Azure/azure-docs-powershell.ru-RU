---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeReport.md
ms.openlocfilehash: f71aef989a26ec5998ee8fd059446a2b05c2e4b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735113"
---
# <span data-ttu-id="b0470-101">Get-AzureRmAutomationDscNodeReport</span><span class="sxs-lookup"><span data-stu-id="b0470-101">Get-AzureRmAutomationDscNodeReport</span></span>

## <span data-ttu-id="b0470-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0470-102">SYNOPSIS</span></span>
<span data-ttu-id="b0470-103">Возвращает отчеты, отправленные с узла DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="b0470-103">Gets reports sent from a DSC node to Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0470-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0470-104">SYNTAX</span></span>

### <span data-ttu-id="b0470-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b0470-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b0470-106">ByLatest</span><span class="sxs-lookup"><span data-stu-id="b0470-106">ByLatest</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0470-107">ById</span><span class="sxs-lookup"><span data-stu-id="b0470-107">ById</span></span>
```
Get-AzureRmAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0470-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0470-108">DESCRIPTION</span></span>
<span data-ttu-id="b0470-109">Командлет **Get-AzureRmAutomationDscNodeReport** получает отчеты от узла DSC нужной конфигурации для Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b0470-109">The **Get-AzureRmAutomationDscNodeReport** cmdlet gets reports sent from an APS Desired State Configuration (DSC) node to Azure Automation.</span></span>

## <span data-ttu-id="b0470-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0470-110">EXAMPLES</span></span>

### <span data-ttu-id="b0470-111">Пример 1: получение всех отчетов для узла DSC</span><span class="sxs-lookup"><span data-stu-id="b0470-111">Example 1: Get all reports for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup14" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

<span data-ttu-id="b0470-112">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0470-112">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b0470-113">Команда хранит этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="b0470-113">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="b0470-114">Вторая команда получает метаданные для всех отчетов, отправленных с узла DSC с именем Computer14, в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0470-114">The second command gets metadata for all reports sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>
<span data-ttu-id="b0470-115">Команда задает узел с помощью свойства **ID** объекта $node.</span><span class="sxs-lookup"><span data-stu-id="b0470-115">The command specifies the node by using the **Id** property of the $Node object.</span></span>

### <span data-ttu-id="b0470-116">Пример 2: получение отчета об узле DSC по ИДЕНТИФИКАТОРу отчета</span><span class="sxs-lookup"><span data-stu-id="b0470-116">Example 2: Get a report for a DSC node by report ID</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="b0470-117">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0470-117">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b0470-118">Команда хранит этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="b0470-118">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="b0470-119">Вторая команда получает метаданные для отчета, идентифицируемого по указанному ИДЕНТИФИКАТОРу, отправленному с узла DSC с именем Computer14, в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0470-119">The second command gets metadata for the report identified by the specified ID sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b0470-120">Пример 3: Получение последнего отчета об узле DSC</span><span class="sxs-lookup"><span data-stu-id="b0470-120">Example 3: Get the latest report for a DSC node</span></span>
```
PS C:\>$Node = Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzureRmAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

<span data-ttu-id="b0470-121">Первая команда получает узел DSC для компьютера с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0470-121">The first command gets the DSC node for the computer named Computer14 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="b0470-122">Команда хранит этот объект в переменной $Node.</span><span class="sxs-lookup"><span data-stu-id="b0470-122">The command stores this object in the $Node variable.</span></span>

<span data-ttu-id="b0470-123">Вторая команда получает метаданные для последнего отчета, отправленного с узла DSC с именем Computer14, в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0470-123">The second command gets metadata for the latest report sent from the DSC node named Computer14 to the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b0470-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0470-124">PARAMETERS</span></span>

### <span data-ttu-id="b0470-125">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b0470-125">-AutomationAccountName</span></span>
<span data-ttu-id="b0470-126">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="b0470-126">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="b0470-127">Этот командлет экспортирует отчеты для узла DSC, который принадлежит учетной записи, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b0470-127">This cmdlet exports reports for a DSC node that belongs to the account that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0470-128">-DefaultProfile</span></span>
<span data-ttu-id="b0470-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b0470-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0470-130">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b0470-130">-EndTime</span></span>
<span data-ttu-id="b0470-131">Указывает время окончания.</span><span class="sxs-lookup"><span data-stu-id="b0470-131">Specifies an end time.</span></span>
<span data-ttu-id="b0470-132">Этот командлет получает отчеты, которые были получены до этого времени.</span><span class="sxs-lookup"><span data-stu-id="b0470-132">This cmdlet gets reports that Automation received before this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-133">-ID</span><span class="sxs-lookup"><span data-stu-id="b0470-133">-Id</span></span>
<span data-ttu-id="b0470-134">Указывает уникальный идентификатор отчета узла DSC для получения этого командлета.</span><span class="sxs-lookup"><span data-stu-id="b0470-134">Specifies the unique ID of the DSC node report for this cmdlet to get.</span></span>

```yaml
Type: Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-135">-Последние</span><span class="sxs-lookup"><span data-stu-id="b0470-135">-Latest</span></span>
<span data-ttu-id="b0470-136">Указывает, что этот командлет получает последний отчет DSC только для указанного узла.</span><span class="sxs-lookup"><span data-stu-id="b0470-136">Indicates that this cmdlet gets the latest DSC report for the specified node only.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByLatest
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-137">-NodeId</span><span class="sxs-lookup"><span data-stu-id="b0470-137">-NodeId</span></span>
<span data-ttu-id="b0470-138">Указывает уникальный идентификатор узла DSC, для которого этот командлет получает отчеты.</span><span class="sxs-lookup"><span data-stu-id="b0470-138">Specifies the unique ID of the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0470-139">-ResourceGroupName</span></span>
<span data-ttu-id="b0470-140">Указывает имя группы ресурсов, содержащей узел DSC, для которого этот командлет получает отчеты.</span><span class="sxs-lookup"><span data-stu-id="b0470-140">Specifies the name of a resource group that contains the DSC node for which this cmdlet gets reports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b0470-141">-StartTime</span></span>
<span data-ttu-id="b0470-142">Указывает время начала.</span><span class="sxs-lookup"><span data-stu-id="b0470-142">Specifies a start time.</span></span>
<span data-ttu-id="b0470-143">Этот командлет получает отчеты о том, что автоматизация была получена после этого времени.</span><span class="sxs-lookup"><span data-stu-id="b0470-143">This cmdlet gets reports that Automation received after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0470-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0470-144">CommonParameters</span></span>
<span data-ttu-id="b0470-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0470-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0470-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0470-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0470-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0470-147">INPUTS</span></span>

### <span data-ttu-id="b0470-148">Ничего</span><span class="sxs-lookup"><span data-stu-id="b0470-148">None</span></span>
<span data-ttu-id="b0470-149">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b0470-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0470-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0470-150">OUTPUTS</span></span>

### <span data-ttu-id="b0470-151">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="b0470-151">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b0470-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0470-152">NOTES</span></span>

## <span data-ttu-id="b0470-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0470-153">RELATED LINKS</span></span>

[<span data-ttu-id="b0470-154">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b0470-154">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="b0470-155">Export-AzureRmAutomationDscNodeReportContent</span><span class="sxs-lookup"><span data-stu-id="b0470-155">Export-AzureRmAutomationDscNodeReportContent</span></span>](./Export-AzureRmAutomationDscNodeReportContent.md)


