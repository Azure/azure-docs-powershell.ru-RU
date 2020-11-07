---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: 9d4efbccffeae2654b5be6d6db8635e588fd87f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727861"
---
# <span data-ttu-id="36247-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="36247-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="36247-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36247-102">SYNOPSIS</span></span>
<span data-ttu-id="36247-103">Возвращает узлы DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="36247-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="36247-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36247-104">SYNTAX</span></span>

### <span data-ttu-id="36247-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36247-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36247-106">ById</span><span class="sxs-lookup"><span data-stu-id="36247-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36247-107">ByName</span><span class="sxs-lookup"><span data-stu-id="36247-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36247-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="36247-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36247-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="36247-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36247-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36247-110">DESCRIPTION</span></span>
<span data-ttu-id="36247-111">Командлет **Get-AzAutomationDscNode** получает узлы точек доступа к требуемому состоянию (DSC) ТД из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="36247-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="36247-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36247-112">EXAMPLES</span></span>

### <span data-ttu-id="36247-113">Пример 1: получение всех узлов DSC</span><span class="sxs-lookup"><span data-stu-id="36247-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="36247-114">Эта команда получает метаданные для всех узлов DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36247-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="36247-115">Пример 2: получение всех узлов DSC для конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="36247-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="36247-116">Эта команда получает метаданные для всех узлов DSC в учетной записи автоматизации с именем Contoso17, сопоставленными с конфигурацией узла DSC, созданной с помощью конфигурации DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="36247-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="36247-117">Пример 3: получение узла DSC по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="36247-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="36247-118">Эта команда получает метаданные на узле DSC с указанным ИДЕНТИФИКАТОРом в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36247-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="36247-119">Пример 4: получение узла DSC по имени</span><span class="sxs-lookup"><span data-stu-id="36247-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="36247-120">Эта команда получает метаданные на узле DSC с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="36247-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="36247-121">Пример 5: получение всех узлов DSC, сопоставленных с конфигурацией узла DSC</span><span class="sxs-lookup"><span data-stu-id="36247-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="36247-122">Эта команда получает метаданные всех узлов DSC в учетной записи автоматизации с именем Contoso17, сопоставленными с конфигурацией узла DSC с именем ContosoConfiguration...</span><span class="sxs-lookup"><span data-stu-id="36247-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="36247-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36247-123">PARAMETERS</span></span>

### <span data-ttu-id="36247-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="36247-124">-AutomationAccountName</span></span>
<span data-ttu-id="36247-125">Указывает имя учетной записи автоматизации, содержащей узлы DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36247-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="36247-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="36247-126">-ConfigurationName</span></span>
<span data-ttu-id="36247-127">Указывает имя конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="36247-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="36247-128">Этот командлет получает узлы DSC, соответствующие конфигурациям узлов, созданным из конфигурации, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="36247-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36247-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36247-129">-DefaultProfile</span></span>
<span data-ttu-id="36247-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="36247-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36247-131">-ID</span><span class="sxs-lookup"><span data-stu-id="36247-131">-Id</span></span>
<span data-ttu-id="36247-132">Указывает уникальный идентификатор узла DSC, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36247-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36247-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36247-133">-Name</span></span>
<span data-ttu-id="36247-134">Указывает имя узла DSC, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36247-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36247-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="36247-135">-NodeConfigurationName</span></span>
<span data-ttu-id="36247-136">Указывает имя конфигурации узла, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36247-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36247-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36247-137">-ResourceGroupName</span></span>
<span data-ttu-id="36247-138">Указывает имя группы ресурсов, в которой этот командлет получает узлы DSC.</span><span class="sxs-lookup"><span data-stu-id="36247-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="36247-139">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="36247-139">-Status</span></span>
<span data-ttu-id="36247-140">Задает состояние узлов DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="36247-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="36247-141">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="36247-141">Valid values are:</span></span> 
- <span data-ttu-id="36247-142">SDMI</span><span class="sxs-lookup"><span data-stu-id="36247-142">Compliant</span></span> 
- <span data-ttu-id="36247-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="36247-143">NotCompliant</span></span>
- <span data-ttu-id="36247-144">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="36247-144">Failed</span></span>
- <span data-ttu-id="36247-145">Типа</span><span class="sxs-lookup"><span data-stu-id="36247-145">Pending</span></span> 
- <span data-ttu-id="36247-146">Получить</span><span class="sxs-lookup"><span data-stu-id="36247-146">Received</span></span>
- <span data-ttu-id="36247-147">Отвечать</span><span class="sxs-lookup"><span data-stu-id="36247-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36247-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36247-148">CommonParameters</span></span>
<span data-ttu-id="36247-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36247-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36247-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36247-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36247-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36247-151">INPUTS</span></span>

### <span data-ttu-id="36247-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="36247-152">System.Guid</span></span>

### <span data-ttu-id="36247-153">System. String</span><span class="sxs-lookup"><span data-stu-id="36247-153">System.String</span></span>

## <span data-ttu-id="36247-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36247-154">OUTPUTS</span></span>

### <span data-ttu-id="36247-155">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="36247-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="36247-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="36247-156">NOTES</span></span>

## <span data-ttu-id="36247-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36247-157">RELATED LINKS</span></span>

[<span data-ttu-id="36247-158">Регистрация — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="36247-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="36247-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="36247-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="36247-160">Отмена регистрации — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="36247-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


