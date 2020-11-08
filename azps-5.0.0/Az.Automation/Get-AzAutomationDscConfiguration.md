---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246130"
---
# <span data-ttu-id="59dc2-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="59dc2-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="59dc2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="59dc2-103">Получение конфигураций DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="59dc2-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="59dc2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59dc2-104">SYNTAX</span></span>

### <span data-ttu-id="59dc2-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59dc2-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59dc2-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="59dc2-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59dc2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59dc2-107">DESCRIPTION</span></span>
<span data-ttu-id="59dc2-108">Командлет **Get-AzAutomationDscConfiguration** получает ТД конфигурации с требуемой конфигурацией (DSC) из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="59dc2-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="59dc2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59dc2-109">EXAMPLES</span></span>

### <span data-ttu-id="59dc2-110">Пример 1: получение всех конфигураций DSC</span><span class="sxs-lookup"><span data-stu-id="59dc2-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="59dc2-111">Эта команда получает метаданные для всех конфигураций DSC в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="59dc2-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="59dc2-112">Пример 2: получение конфигурации DSC по имени</span><span class="sxs-lookup"><span data-stu-id="59dc2-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="59dc2-113">Эта команда получает метаданные для конфигурации DSC с именем MyConfiguration в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="59dc2-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="59dc2-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59dc2-114">PARAMETERS</span></span>

### <span data-ttu-id="59dc2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="59dc2-115">-AutomationAccountName</span></span>
<span data-ttu-id="59dc2-116">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="59dc2-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="59dc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59dc2-117">-DefaultProfile</span></span>
<span data-ttu-id="59dc2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="59dc2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59dc2-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="59dc2-119">-Name</span></span>
<span data-ttu-id="59dc2-120">Указывает имя конфигурации DSC, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="59dc2-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="59dc2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59dc2-121">-ResourceGroupName</span></span>
<span data-ttu-id="59dc2-122">Указывает имя группы ресурсов, для которой этот командлет получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="59dc2-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="59dc2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59dc2-123">CommonParameters</span></span>
<span data-ttu-id="59dc2-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59dc2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59dc2-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59dc2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59dc2-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59dc2-126">INPUTS</span></span>

### <span data-ttu-id="59dc2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="59dc2-127">System.String</span></span>

## <span data-ttu-id="59dc2-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59dc2-128">OUTPUTS</span></span>

### <span data-ttu-id="59dc2-129">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="59dc2-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="59dc2-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="59dc2-130">NOTES</span></span>

## <span data-ttu-id="59dc2-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59dc2-131">RELATED LINKS</span></span>

[<span data-ttu-id="59dc2-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="59dc2-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="59dc2-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="59dc2-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


