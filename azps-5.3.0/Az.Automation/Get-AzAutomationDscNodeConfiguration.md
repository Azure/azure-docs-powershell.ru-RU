---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98510106"
---
# <span data-ttu-id="df397-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="df397-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="df397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df397-102">SYNOPSIS</span></span>
<span data-ttu-id="df397-103">Получает метаданные для конфигураций узлов DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="df397-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="df397-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="df397-104">SYNTAX</span></span>

### <span data-ttu-id="df397-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df397-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df397-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="df397-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df397-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="df397-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df397-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df397-108">DESCRIPTION</span></span>
<span data-ttu-id="df397-109">Cmdlet **Get-AzAutomationDscNodeConfiguration** получает метаданные для конфигураций узла APS в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="df397-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="df397-110">Автоматизация хранит конфигурацию узла DSC в документе конфигурации "Управляемый формат объекта" (MOF).</span><span class="sxs-lookup"><span data-stu-id="df397-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="df397-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="df397-111">EXAMPLES</span></span>

### <span data-ttu-id="df397-112">Пример 1. Получить все конфигурации узлов DSC</span><span class="sxs-lookup"><span data-stu-id="df397-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="df397-113">Эта команда получает метаданные для всех конфигураций узлов DSC в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df397-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="df397-114">Пример 2. Получить все конфигурации узла DSC для конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="df397-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="df397-115">Эта команда получает метаданные для всех настроек узла DSC в учетной записи автоматизации Contoso17, которую создает конфигурация DSC с именем ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="df397-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="df397-116">Пример 3. Настройка узла DSC по имени</span><span class="sxs-lookup"><span data-stu-id="df397-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="df397-117">Эта команда получает метаданные для конфигурации узла DSC с именем ContosoConfiguration.webserver в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="df397-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="df397-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df397-118">PARAMETERS</span></span>

### <span data-ttu-id="df397-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df397-119">-AutomationAccountName</span></span>
<span data-ttu-id="df397-120">Имя учетной записи автоматизации, которая содержит конфигурации узлов DSC, для которых этот cmdlet получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="df397-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="df397-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="df397-121">-ConfigurationName</span></span>
<span data-ttu-id="df397-122">Указывает имя конфигурации DSC, для которой этот cmdlet получает метаданные конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="df397-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df397-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df397-123">-DefaultProfile</span></span>
<span data-ttu-id="df397-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="df397-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df397-125">-Name</span><span class="sxs-lookup"><span data-stu-id="df397-125">-Name</span></span>
<span data-ttu-id="df397-126">Указывает имя конфигурации узла DSC, для которой этот cmdlet получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="df397-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df397-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df397-127">-ResourceGroupName</span></span>
<span data-ttu-id="df397-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df397-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="df397-129">Этот cmdlet получает метаданные для конфигураций узлов DSC в группе ресурсов, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="df397-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="df397-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="df397-130">-RollupStatus</span></span>
<span data-ttu-id="df397-131">Указывает состояние ската конфигураций узла DSC, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df397-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="df397-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="df397-132">Valid values are:</span></span> 
- <span data-ttu-id="df397-133">Плохо</span><span class="sxs-lookup"><span data-stu-id="df397-133">Bad</span></span> 
- <span data-ttu-id="df397-134">Хорошо</span><span class="sxs-lookup"><span data-stu-id="df397-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df397-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df397-135">CommonParameters</span></span>
<span data-ttu-id="df397-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df397-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df397-137">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df397-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df397-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="df397-138">INPUTS</span></span>

### <span data-ttu-id="df397-139">System.String</span><span class="sxs-lookup"><span data-stu-id="df397-139">System.String</span></span>

## <span data-ttu-id="df397-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="df397-140">OUTPUTS</span></span>

### <span data-ttu-id="df397-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="df397-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="df397-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="df397-142">NOTES</span></span>

## <span data-ttu-id="df397-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df397-143">RELATED LINKS</span></span>

[<span data-ttu-id="df397-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="df397-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


