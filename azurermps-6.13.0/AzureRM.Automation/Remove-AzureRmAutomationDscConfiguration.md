---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e5d7f6c75624fcfb15fa08718acc24e02336cb5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732325"
---
# <span data-ttu-id="beb2d-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="beb2d-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="beb2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="beb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="beb2d-103">Удаляет конфигурации DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="beb2d-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="beb2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="beb2d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="beb2d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="beb2d-105">DESCRIPTION</span></span>
<span data-ttu-id="beb2d-106">Командлет **Remove-AzureRmAutomationDscConfiguration** удаляет из Azure Automation параметры необходимой конфигурации состояния (DSC).</span><span class="sxs-lookup"><span data-stu-id="beb2d-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="beb2d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="beb2d-107">EXAMPLES</span></span>

## <span data-ttu-id="beb2d-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="beb2d-108">PARAMETERS</span></span>

### <span data-ttu-id="beb2d-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="beb2d-109">-AutomationAccountName</span></span>
<span data-ttu-id="beb2d-110">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые удаляются этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="beb2d-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="beb2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="beb2d-111">-DefaultProfile</span></span>
<span data-ttu-id="beb2d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="beb2d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="beb2d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="beb2d-113">-Force</span></span>
<span data-ttu-id="beb2d-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="beb2d-114">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb2d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="beb2d-115">-Name</span></span>
<span data-ttu-id="beb2d-116">Указывает имя конфигурации DSC, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="beb2d-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="beb2d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="beb2d-117">-ResourceGroupName</span></span>
<span data-ttu-id="beb2d-118">Указывает имя группы ресурсов, для которой этот командлет получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="beb2d-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="beb2d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="beb2d-119">-Confirm</span></span>
<span data-ttu-id="beb2d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="beb2d-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb2d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="beb2d-121">-WhatIf</span></span>
<span data-ttu-id="beb2d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="beb2d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="beb2d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="beb2d-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="beb2d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="beb2d-124">CommonParameters</span></span>
<span data-ttu-id="beb2d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="beb2d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="beb2d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="beb2d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="beb2d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="beb2d-127">INPUTS</span></span>

### <span data-ttu-id="beb2d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="beb2d-128">System.String</span></span>

## <span data-ttu-id="beb2d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="beb2d-129">OUTPUTS</span></span>

### <span data-ttu-id="beb2d-130">System. void</span><span class="sxs-lookup"><span data-stu-id="beb2d-130">System.Void</span></span>

## <span data-ttu-id="beb2d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="beb2d-131">NOTES</span></span>

## <span data-ttu-id="beb2d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="beb2d-132">RELATED LINKS</span></span>

[<span data-ttu-id="beb2d-133">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="beb2d-133">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="beb2d-134">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="beb2d-134">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="beb2d-135">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="beb2d-135">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


