---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNode.md
ms.openlocfilehash: 51d7df7f6b1e99188e5be31537700f4eef019053
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565708"
---
# <span data-ttu-id="eabb3-101">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="eabb3-101">Get-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="eabb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eabb3-102">SYNOPSIS</span></span>
<span data-ttu-id="eabb3-103">Возвращает узлы DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="eabb3-103">Gets DSC nodes from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eabb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eabb3-104">SYNTAX</span></span>

### <span data-ttu-id="eabb3-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eabb3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabb3-106">ById</span><span class="sxs-lookup"><span data-stu-id="eabb3-106">ById</span></span>
```
Get-AzureRmAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabb3-107">ByName</span><span class="sxs-lookup"><span data-stu-id="eabb3-107">ByName</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eabb3-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="eabb3-108">ByNodeConfiguration</span></span>
```
Get-AzureRmAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eabb3-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="eabb3-109">ByConfiguration</span></span>
```
Get-AzureRmAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eabb3-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eabb3-110">DESCRIPTION</span></span>
<span data-ttu-id="eabb3-111">Командлет **Get-AzureRmAutomationDscNode** получает узлы точек доступа к требуемому состоянию (DSC) ТД из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="eabb3-111">The **Get-AzureRmAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="eabb3-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eabb3-112">EXAMPLES</span></span>

### <span data-ttu-id="eabb3-113">Пример 1: получение всех узлов DSC</span><span class="sxs-lookup"><span data-stu-id="eabb3-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="eabb3-114">Эта команда получает метаданные для всех узлов DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="eabb3-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="eabb3-115">Пример 2: получение всех узлов DSC для конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="eabb3-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="eabb3-116">Эта команда получает метаданные для всех узлов DSC в учетной записи автоматизации с именем Contoso17, сопоставленными с конфигурацией узла DSC, созданной с помощью конфигурации DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="eabb3-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="eabb3-117">Пример 3: получение узла DSC по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="eabb3-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="eabb3-118">Эта команда получает метаданные на узле DSC с указанным ИДЕНТИФИКАТОРом в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="eabb3-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="eabb3-119">Пример 4: получение узла DSC по имени</span><span class="sxs-lookup"><span data-stu-id="eabb3-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="eabb3-120">Эта команда получает метаданные на узле DSC с именем Computer14 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="eabb3-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="eabb3-121">Пример 5: получение всех узлов DSC, сопоставленных с конфигурацией узла DSC</span><span class="sxs-lookup"><span data-stu-id="eabb3-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="eabb3-122">Эта команда получает метаданные всех узлов DSC в учетной записи автоматизации с именем Contoso17, сопоставленными с конфигурацией узла DSC с именем ContosoConfiguration...</span><span class="sxs-lookup"><span data-stu-id="eabb3-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="eabb3-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eabb3-123">PARAMETERS</span></span>

### <span data-ttu-id="eabb3-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eabb3-124">-AutomationAccountName</span></span>
<span data-ttu-id="eabb3-125">Указывает имя учетной записи автоматизации, содержащей узлы DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eabb3-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eabb3-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="eabb3-126">-ConfigurationName</span></span>
<span data-ttu-id="eabb3-127">Указывает имя конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="eabb3-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="eabb3-128">Этот командлет получает узлы DSC, соответствующие конфигурациям узлов, созданным из конфигурации, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="eabb3-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

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

### <span data-ttu-id="eabb3-129">-ID</span><span class="sxs-lookup"><span data-stu-id="eabb3-129">-Id</span></span>
<span data-ttu-id="eabb3-130">Указывает уникальный идентификатор узла DSC, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eabb3-130">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eabb3-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="eabb3-131">-Name</span></span>
<span data-ttu-id="eabb3-132">Указывает имя узла DSC, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eabb3-132">Specifies the name of a DSC node that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eabb3-133">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="eabb3-133">-NodeConfigurationName</span></span>
<span data-ttu-id="eabb3-134">Указывает имя конфигурации узла, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eabb3-134">Specifies the name of a node configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="eabb3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eabb3-135">-ResourceGroupName</span></span>
<span data-ttu-id="eabb3-136">Указывает имя группы ресурсов, в которой этот командлет получает узлы DSC.</span><span class="sxs-lookup"><span data-stu-id="eabb3-136">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

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

### <span data-ttu-id="eabb3-137">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="eabb3-137">-Status</span></span>
<span data-ttu-id="eabb3-138">Задает состояние узлов DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="eabb3-138">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="eabb3-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eabb3-139">Valid values are:</span></span> 

- <span data-ttu-id="eabb3-140">SDMI</span><span class="sxs-lookup"><span data-stu-id="eabb3-140">Compliant</span></span> 
- <span data-ttu-id="eabb3-141">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="eabb3-141">NotCompliant</span></span>
- <span data-ttu-id="eabb3-142">Ошибкой</span><span class="sxs-lookup"><span data-stu-id="eabb3-142">Failed</span></span>
- <span data-ttu-id="eabb3-143">Типа</span><span class="sxs-lookup"><span data-stu-id="eabb3-143">Pending</span></span> 
- <span data-ttu-id="eabb3-144">Получить</span><span class="sxs-lookup"><span data-stu-id="eabb3-144">Received</span></span>
- <span data-ttu-id="eabb3-145">Отвечать</span><span class="sxs-lookup"><span data-stu-id="eabb3-145">Unresponsive</span></span>

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

### <span data-ttu-id="eabb3-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eabb3-146">-DefaultProfile</span></span>
<span data-ttu-id="eabb3-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eabb3-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eabb3-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eabb3-148">CommonParameters</span></span>
<span data-ttu-id="eabb3-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eabb3-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eabb3-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eabb3-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eabb3-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eabb3-151">INPUTS</span></span>

## <span data-ttu-id="eabb3-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eabb3-152">OUTPUTS</span></span>

### <span data-ttu-id="eabb3-153">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="eabb3-153">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="eabb3-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="eabb3-154">NOTES</span></span>

## <span data-ttu-id="eabb3-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eabb3-155">RELATED LINKS</span></span>

[<span data-ttu-id="eabb3-156">Регистрация — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="eabb3-156">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="eabb3-157">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="eabb3-157">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="eabb3-158">Отмена регистрации — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="eabb3-158">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


