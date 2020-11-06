---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 2cd60a70b057689cf7edf154df28253b86e110a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565673"
---
# <span data-ttu-id="587fb-101">Remove-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="587fb-101">Remove-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="587fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="587fb-102">SYNOPSIS</span></span>
<span data-ttu-id="587fb-103">Удаляет конфигурации DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="587fb-103">Removes DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="587fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="587fb-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="587fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="587fb-105">DESCRIPTION</span></span>
<span data-ttu-id="587fb-106">Командлет **Remove-AzureRmAutomationDscConfiguration** удаляет из Azure Automation параметры необходимой конфигурации состояния (DSC).</span><span class="sxs-lookup"><span data-stu-id="587fb-106">The **Remove-AzureRmAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="587fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="587fb-107">EXAMPLES</span></span>

## <span data-ttu-id="587fb-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="587fb-108">PARAMETERS</span></span>

### <span data-ttu-id="587fb-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="587fb-109">-AutomationAccountName</span></span>
<span data-ttu-id="587fb-110">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые удаляются этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="587fb-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="587fb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="587fb-111">-Force</span></span>
<span data-ttu-id="587fb-112">ps_force</span><span class="sxs-lookup"><span data-stu-id="587fb-112">ps_force</span></span>

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

### <span data-ttu-id="587fb-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="587fb-113">-Name</span></span>
<span data-ttu-id="587fb-114">Указывает имя конфигурации DSC, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="587fb-114">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="587fb-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="587fb-115">-ResourceGroupName</span></span>
<span data-ttu-id="587fb-116">Указывает имя группы ресурсов, для которой этот командлет получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="587fb-116">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="587fb-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="587fb-117">-Confirm</span></span>
<span data-ttu-id="587fb-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="587fb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="587fb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="587fb-119">-WhatIf</span></span>
<span data-ttu-id="587fb-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="587fb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="587fb-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="587fb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="587fb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="587fb-122">-DefaultProfile</span></span>
<span data-ttu-id="587fb-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="587fb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="587fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="587fb-124">CommonParameters</span></span>
<span data-ttu-id="587fb-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="587fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="587fb-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="587fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="587fb-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="587fb-127">INPUTS</span></span>

## <span data-ttu-id="587fb-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="587fb-128">OUTPUTS</span></span>

## <span data-ttu-id="587fb-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="587fb-129">NOTES</span></span>

## <span data-ttu-id="587fb-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="587fb-130">RELATED LINKS</span></span>

[<span data-ttu-id="587fb-131">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="587fb-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="587fb-132">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="587fb-132">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="587fb-133">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="587fb-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


