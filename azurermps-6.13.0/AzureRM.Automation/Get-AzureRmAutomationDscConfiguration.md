---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 10e04dc24c34ba60186c8166e2626524fcc60a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556883"
---
# <span data-ttu-id="00d6c-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00d6c-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="00d6c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="00d6c-103">Получение конфигураций DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="00d6c-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00d6c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00d6c-104">SYNTAX</span></span>

### <span data-ttu-id="00d6c-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00d6c-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00d6c-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="00d6c-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00d6c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00d6c-107">DESCRIPTION</span></span>
<span data-ttu-id="00d6c-108">Командлет **Get-AzureRmAutomationDscConfiguration** получает ТД конфигурации с требуемой конфигурацией (DSC) из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="00d6c-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="00d6c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00d6c-109">EXAMPLES</span></span>

### <span data-ttu-id="00d6c-110">Пример 1: получение всех конфигураций DSC</span><span class="sxs-lookup"><span data-stu-id="00d6c-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="00d6c-111">Эта команда получает метаданные для всех конфигураций DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00d6c-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="00d6c-112">Пример 2: получение конфигурации DSC по имени</span><span class="sxs-lookup"><span data-stu-id="00d6c-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="00d6c-113">Эта команда получает метаданные для конфигурации DSC с именем MyConfiguration в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="00d6c-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="00d6c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00d6c-114">PARAMETERS</span></span>

### <span data-ttu-id="00d6c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00d6c-115">-AutomationAccountName</span></span>
<span data-ttu-id="00d6c-116">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="00d6c-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00d6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00d6c-117">-DefaultProfile</span></span>
<span data-ttu-id="00d6c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="00d6c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00d6c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00d6c-119">-Name</span></span>
<span data-ttu-id="00d6c-120">Указывает имя конфигурации DSC, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="00d6c-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00d6c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00d6c-121">-ResourceGroupName</span></span>
<span data-ttu-id="00d6c-122">Указывает имя группы ресурсов, для которой этот командлет получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="00d6c-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="00d6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d6c-123">CommonParameters</span></span>
<span data-ttu-id="00d6c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00d6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d6c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d6c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d6c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00d6c-126">INPUTS</span></span>

### <span data-ttu-id="00d6c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="00d6c-127">System.String</span></span>

## <span data-ttu-id="00d6c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00d6c-128">OUTPUTS</span></span>

### <span data-ttu-id="00d6c-129">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00d6c-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="00d6c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="00d6c-130">NOTES</span></span>

## <span data-ttu-id="00d6c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00d6c-131">RELATED LINKS</span></span>

[<span data-ttu-id="00d6c-132">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00d6c-132">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="00d6c-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="00d6c-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


