---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565707"
---
# <span data-ttu-id="23ce7-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="23ce7-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="23ce7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="23ce7-103">Получает метаданные для конфигураций узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="23ce7-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23ce7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23ce7-104">SYNTAX</span></span>

### <span data-ttu-id="23ce7-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23ce7-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ce7-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="23ce7-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ce7-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="23ce7-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="23ce7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ce7-108">DESCRIPTION</span></span>
<span data-ttu-id="23ce7-109">Командлет **Get-AzureRmAutomationDscNodeConfiguration** получает метаданные для конфигураций узла ТД для необходимой конфигурации состояния (DSC) в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="23ce7-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="23ce7-110">Модель автоматизации хранит конфигурацию узла DSC в виде документа конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="23ce7-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="23ce7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23ce7-111">EXAMPLES</span></span>

### <span data-ttu-id="23ce7-112">Пример 1: получение всех конфигураций узлов DSC</span><span class="sxs-lookup"><span data-stu-id="23ce7-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="23ce7-113">Эта команда получает метаданные для всех конфигураций узла DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="23ce7-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="23ce7-114">Пример 2: получение всех конфигураций узлов DSC для конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="23ce7-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="23ce7-115">Эта команда получает метаданные для всех конфигураций узла DSC в учетной записи автоматизации с именем Contoso17, что конфигурация DSC с именем ContosoConfiguration создана.</span><span class="sxs-lookup"><span data-stu-id="23ce7-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="23ce7-116">Пример 3: получение конфигурации узла DSC по имени</span><span class="sxs-lookup"><span data-stu-id="23ce7-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="23ce7-117">Эта команда получает метаданные для конфигурации узла DSC с именем ContosoConfiguration. веб-сервером в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="23ce7-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="23ce7-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23ce7-118">PARAMETERS</span></span>

### <span data-ttu-id="23ce7-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="23ce7-119">-AutomationAccountName</span></span>
<span data-ttu-id="23ce7-120">Указывает имя учетной записи службы автоматизации, содержащей конфигурации узла DSC, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="23ce7-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="23ce7-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="23ce7-121">-ConfigurationName</span></span>
<span data-ttu-id="23ce7-122">Указывает имя конфигурации DSC, для которой этот командлет получает метаданные конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="23ce7-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="23ce7-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23ce7-123">-Name</span></span>
<span data-ttu-id="23ce7-124">Указывает имя конфигурации узла DSC, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="23ce7-124">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="23ce7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ce7-125">-ResourceGroupName</span></span>
<span data-ttu-id="23ce7-126">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23ce7-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="23ce7-127">Этот командлет получает метаданные для конфигураций узла DSC в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="23ce7-127">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="23ce7-128">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="23ce7-128">-RollupStatus</span></span>
<span data-ttu-id="23ce7-129">Указывает состояние свертки для конфигураций узла DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="23ce7-129">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="23ce7-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="23ce7-130">Valid values are:</span></span> 

- <span data-ttu-id="23ce7-131">Сбой</span><span class="sxs-lookup"><span data-stu-id="23ce7-131">Bad</span></span> 
- <span data-ttu-id="23ce7-132">Правильного</span><span class="sxs-lookup"><span data-stu-id="23ce7-132">Good</span></span>

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

### <span data-ttu-id="23ce7-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ce7-133">-DefaultProfile</span></span>
<span data-ttu-id="23ce7-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23ce7-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23ce7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ce7-135">CommonParameters</span></span>
<span data-ttu-id="23ce7-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23ce7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ce7-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23ce7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ce7-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23ce7-138">INPUTS</span></span>

## <span data-ttu-id="23ce7-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ce7-139">OUTPUTS</span></span>

### <span data-ttu-id="23ce7-140">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="23ce7-140">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="23ce7-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="23ce7-141">NOTES</span></span>

## <span data-ttu-id="23ce7-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23ce7-142">RELATED LINKS</span></span>

[<span data-ttu-id="23ce7-143">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="23ce7-143">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


