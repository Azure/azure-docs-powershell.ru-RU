---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6389EE2A-12B5-46A1-A2B9-4B3CF5A55A30
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationDscConfiguration.md
ms.openlocfilehash: bd418037f29aefc27d92ccebe1f34024728c77c9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074934"
---
# <span data-ttu-id="812ec-101">Remove-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="812ec-101">Remove-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="812ec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="812ec-102">SYNOPSIS</span></span>
<span data-ttu-id="812ec-103">Удаляет конфигурации DSC из автоматизации.</span><span class="sxs-lookup"><span data-stu-id="812ec-103">Removes DSC configurations from Automation.</span></span>

## <span data-ttu-id="812ec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="812ec-104">SYNTAX</span></span>

```
Remove-AzAutomationDscConfiguration [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="812ec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="812ec-105">DESCRIPTION</span></span>
<span data-ttu-id="812ec-106">Командлет **Remove-AzAutomationDscConfiguration** удаляет из Azure Automation параметры необходимой конфигурации состояния (DSC).</span><span class="sxs-lookup"><span data-stu-id="812ec-106">The **Remove-AzAutomationDscConfiguration** cmdlet removes APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="812ec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="812ec-107">EXAMPLES</span></span>

## <span data-ttu-id="812ec-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="812ec-108">PARAMETERS</span></span>

### <span data-ttu-id="812ec-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="812ec-109">-AutomationAccountName</span></span>
<span data-ttu-id="812ec-110">Указывает имя учетной записи автоматизации, которая содержит конфигурации DSC, которые удаляются этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="812ec-110">Specifies the name of the Automation account that contains DSC configurations that this cmdlet removes.</span></span>

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

### <span data-ttu-id="812ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="812ec-111">-DefaultProfile</span></span>
<span data-ttu-id="812ec-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="812ec-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="812ec-113">-Force</span><span class="sxs-lookup"><span data-stu-id="812ec-113">-Force</span></span>
<span data-ttu-id="812ec-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="812ec-114">ps_force</span></span>

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

### <span data-ttu-id="812ec-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="812ec-115">-Name</span></span>
<span data-ttu-id="812ec-116">Указывает имя конфигурации DSC, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="812ec-116">Specifies the name of the DSC configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="812ec-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="812ec-117">-ResourceGroupName</span></span>
<span data-ttu-id="812ec-118">Указывает имя группы ресурсов, для которой этот командлет получает конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="812ec-118">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="812ec-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="812ec-119">-Confirm</span></span>
<span data-ttu-id="812ec-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="812ec-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="812ec-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="812ec-121">-WhatIf</span></span>
<span data-ttu-id="812ec-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="812ec-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="812ec-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="812ec-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="812ec-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="812ec-124">CommonParameters</span></span>
<span data-ttu-id="812ec-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="812ec-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="812ec-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="812ec-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="812ec-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="812ec-127">INPUTS</span></span>

### <span data-ttu-id="812ec-128">System. String</span><span class="sxs-lookup"><span data-stu-id="812ec-128">System.String</span></span>

## <span data-ttu-id="812ec-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="812ec-129">OUTPUTS</span></span>

### <span data-ttu-id="812ec-130">System. void</span><span class="sxs-lookup"><span data-stu-id="812ec-130">System.Void</span></span>

## <span data-ttu-id="812ec-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="812ec-131">NOTES</span></span>

## <span data-ttu-id="812ec-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="812ec-132">RELATED LINKS</span></span>

[<span data-ttu-id="812ec-133">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="812ec-133">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="812ec-134">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="812ec-134">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="812ec-135">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="812ec-135">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


