---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416764"
---
# <span data-ttu-id="8ad85-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ad85-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="8ad85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad85-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad85-103">Получает настройки DSC от автоматизации.</span><span class="sxs-lookup"><span data-stu-id="8ad85-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="8ad85-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ad85-104">SYNTAX</span></span>

### <span data-ttu-id="8ad85-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ad85-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ad85-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8ad85-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ad85-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ad85-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad85-108">Для **работы с cmdlet get-AzAutomationDscConfiguration** от автоматизации Azure получаются конфигурации APS Desired State Configuration (DSC).</span><span class="sxs-lookup"><span data-stu-id="8ad85-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="8ad85-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ad85-109">EXAMPLES</span></span>

### <span data-ttu-id="8ad85-110">Пример 1. Получить все конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="8ad85-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8ad85-111">Эта команда получает метаданные для всех конфигураций DSC в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ad85-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8ad85-112">Пример 2. Настройка DSC по имени</span><span class="sxs-lookup"><span data-stu-id="8ad85-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="8ad85-113">Эта команда получает метаданные для конфигурации DSC MyConfiguration в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8ad85-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8ad85-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ad85-114">PARAMETERS</span></span>

### <span data-ttu-id="8ad85-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ad85-115">-AutomationAccountName</span></span>
<span data-ttu-id="8ad85-116">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ad85-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8ad85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad85-117">-DefaultProfile</span></span>
<span data-ttu-id="8ad85-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8ad85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8ad85-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad85-119">-Name</span></span>
<span data-ttu-id="8ad85-120">Указывает имя конфигурации DSC, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ad85-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8ad85-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad85-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ad85-122">Имя группы ресурсов, для которой этот cmdlet получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="8ad85-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="8ad85-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad85-123">CommonParameters</span></span>
<span data-ttu-id="8ad85-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad85-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad85-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ad85-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad85-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad85-126">INPUTS</span></span>

### <span data-ttu-id="8ad85-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8ad85-127">System.String</span></span>

## <span data-ttu-id="8ad85-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ad85-128">OUTPUTS</span></span>

### <span data-ttu-id="8ad85-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ad85-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="8ad85-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ad85-130">NOTES</span></span>

## <span data-ttu-id="8ad85-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ad85-131">RELATED LINKS</span></span>

[<span data-ttu-id="8ad85-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ad85-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="8ad85-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ad85-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


