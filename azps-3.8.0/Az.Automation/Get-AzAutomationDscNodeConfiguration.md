---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072701"
---
# <span data-ttu-id="50247-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="50247-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="50247-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50247-102">SYNOPSIS</span></span>
<span data-ttu-id="50247-103">Получает метаданные для конфигураций узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="50247-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="50247-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50247-104">SYNTAX</span></span>

### <span data-ttu-id="50247-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="50247-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50247-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="50247-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50247-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="50247-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50247-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50247-108">DESCRIPTION</span></span>
<span data-ttu-id="50247-109">Командлет **Get-AzAutomationDscNodeConfiguration** получает метаданные для конфигураций узла ТД для необходимой конфигурации состояния (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="50247-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="50247-110">Модель автоматизации хранит конфигурацию узла DSC в виде документа конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="50247-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="50247-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50247-111">EXAMPLES</span></span>

### <span data-ttu-id="50247-112">Пример 1: получение всех конфигураций узлов DSC</span><span class="sxs-lookup"><span data-stu-id="50247-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="50247-113">Эта команда получает метаданные для всех конфигураций узла DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="50247-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="50247-114">Пример 2: получение всех конфигураций узлов DSC для конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="50247-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="50247-115">Эта команда получает метаданные для всех конфигураций узла DSC в учетной записи автоматизации с именем Contoso17, что конфигурация DSC с именем ContosoConfiguration создана.</span><span class="sxs-lookup"><span data-stu-id="50247-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="50247-116">Пример 3: получение конфигурации узла DSC по имени</span><span class="sxs-lookup"><span data-stu-id="50247-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="50247-117">Эта команда получает метаданные для конфигурации узла DSC с именем ContosoConfiguration. веб-сервером в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="50247-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="50247-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50247-118">PARAMETERS</span></span>

### <span data-ttu-id="50247-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="50247-119">-AutomationAccountName</span></span>
<span data-ttu-id="50247-120">Указывает имя учетной записи службы автоматизации, содержащей конфигурации узла DSC, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="50247-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="50247-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="50247-121">-ConfigurationName</span></span>
<span data-ttu-id="50247-122">Указывает имя конфигурации DSC, для которой этот командлет получает метаданные конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="50247-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="50247-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50247-123">-DefaultProfile</span></span>
<span data-ttu-id="50247-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="50247-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50247-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="50247-125">-Name</span></span>
<span data-ttu-id="50247-126">Указывает имя конфигурации узла DSC, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="50247-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="50247-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50247-127">-ResourceGroupName</span></span>
<span data-ttu-id="50247-128">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="50247-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="50247-129">Этот командлет получает метаданные для конфигураций узла DSC в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="50247-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="50247-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="50247-130">-RollupStatus</span></span>
<span data-ttu-id="50247-131">Указывает состояние свертки для конфигураций узла DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="50247-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="50247-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="50247-132">Valid values are:</span></span> 
- <span data-ttu-id="50247-133">Сбой</span><span class="sxs-lookup"><span data-stu-id="50247-133">Bad</span></span> 
- <span data-ttu-id="50247-134">Правильного</span><span class="sxs-lookup"><span data-stu-id="50247-134">Good</span></span>

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

### <span data-ttu-id="50247-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50247-135">CommonParameters</span></span>
<span data-ttu-id="50247-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50247-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50247-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50247-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50247-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50247-138">INPUTS</span></span>

### <span data-ttu-id="50247-139">System. String</span><span class="sxs-lookup"><span data-stu-id="50247-139">System.String</span></span>

## <span data-ttu-id="50247-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50247-140">OUTPUTS</span></span>

### <span data-ttu-id="50247-141">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="50247-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="50247-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="50247-142">NOTES</span></span>

## <span data-ttu-id="50247-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50247-143">RELATED LINKS</span></span>

[<span data-ttu-id="50247-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="50247-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


