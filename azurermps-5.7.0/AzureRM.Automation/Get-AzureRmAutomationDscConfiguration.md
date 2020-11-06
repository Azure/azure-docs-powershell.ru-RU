---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 3d6d3628ba15fa4b775f4c747a29645ec0628402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570296"
---
# <span data-ttu-id="699e5-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="699e5-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="699e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="699e5-102">SYNOPSIS</span></span>
<span data-ttu-id="699e5-103">Получение конфигураций DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="699e5-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="699e5-104">SYNTAX</span></span>

### <span data-ttu-id="699e5-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="699e5-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="699e5-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="699e5-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="699e5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="699e5-107">DESCRIPTION</span></span>
<span data-ttu-id="699e5-108">Командлет **Get-AzureRmAutomationDscConfiguration** получает ТД конфигурации с требуемой конфигурацией (DSC) из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="699e5-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="699e5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="699e5-109">EXAMPLES</span></span>

### <span data-ttu-id="699e5-110">Пример 1: получение всех конфигураций DSC</span><span class="sxs-lookup"><span data-stu-id="699e5-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="699e5-111">Эта команда получает метаданные для всех конфигураций DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="699e5-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="699e5-112">Пример 2: получение конфигурации DSC по имени</span><span class="sxs-lookup"><span data-stu-id="699e5-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="699e5-113">Эта команда получает метаданные для конфигурации DSC с именем MyConfiguration в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="699e5-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="699e5-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="699e5-114">PARAMETERS</span></span>

### <span data-ttu-id="699e5-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="699e5-115">-AutomationAccountName</span></span>
<span data-ttu-id="699e5-116">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="699e5-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="699e5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699e5-117">-DefaultProfile</span></span>
<span data-ttu-id="699e5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="699e5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="699e5-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="699e5-119">-Name</span></span>
<span data-ttu-id="699e5-120">Указывает имя конфигурации DSC, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="699e5-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699e5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699e5-121">-ResourceGroupName</span></span>
<span data-ttu-id="699e5-122">Указывает имя группы ресурсов, для которой этот командлет получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="699e5-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="699e5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699e5-123">CommonParameters</span></span>
<span data-ttu-id="699e5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="699e5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699e5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699e5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699e5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="699e5-126">INPUTS</span></span>

### <span data-ttu-id="699e5-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="699e5-127">None</span></span>
<span data-ttu-id="699e5-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="699e5-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="699e5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="699e5-129">OUTPUTS</span></span>

### <span data-ttu-id="699e5-130">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="699e5-130">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="699e5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="699e5-131">NOTES</span></span>

## <span data-ttu-id="699e5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="699e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="699e5-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="699e5-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="699e5-134">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="699e5-134">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


