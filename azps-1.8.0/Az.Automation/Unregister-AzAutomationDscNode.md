---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: fc4696a26c10ace497c6ff64a7ac4c1ac49279c7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731480"
---
# <span data-ttu-id="3af0b-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3af0b-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="3af0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3af0b-102">SYNOPSIS</span></span>
<span data-ttu-id="3af0b-103">Удаляет узел DSC из управления с помощью учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3af0b-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="3af0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3af0b-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3af0b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3af0b-105">DESCRIPTION</span></span>
<span data-ttu-id="3af0b-106">Командлет **Unregister-AzAutomationDscNode** удаляет узел настройки нужного состояния ТД из управления с помощью учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3af0b-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="3af0b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3af0b-107">EXAMPLES</span></span>

### <span data-ttu-id="3af0b-108">Пример 1: Удаление узла Azure DSC из управления с помощью учетной записи службы автоматизации</span><span class="sxs-lookup"><span data-stu-id="3af0b-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="3af0b-109">Эта команда удаляет узел DSC с указанным GUID из управления с помощью учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3af0b-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3af0b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3af0b-110">PARAMETERS</span></span>

### <span data-ttu-id="3af0b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3af0b-111">-AutomationAccountName</span></span>
<span data-ttu-id="3af0b-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="3af0b-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="3af0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3af0b-113">-DefaultProfile</span></span>
<span data-ttu-id="3af0b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3af0b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3af0b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3af0b-115">-Force</span></span>
<span data-ttu-id="3af0b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3af0b-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3af0b-117">-ID</span><span class="sxs-lookup"><span data-stu-id="3af0b-117">-Id</span></span>
<span data-ttu-id="3af0b-118">Указывает уникальный идентификатор узла DSC, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3af0b-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3af0b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3af0b-119">-ResourceGroupName</span></span>
<span data-ttu-id="3af0b-120">Указывает имя группы ресурсов, в которой командлет удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="3af0b-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="3af0b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3af0b-121">-Confirm</span></span>
<span data-ttu-id="3af0b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3af0b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3af0b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3af0b-123">-WhatIf</span></span>
<span data-ttu-id="3af0b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3af0b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3af0b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3af0b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3af0b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3af0b-126">CommonParameters</span></span>
<span data-ttu-id="3af0b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3af0b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3af0b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3af0b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3af0b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3af0b-129">INPUTS</span></span>

### <span data-ttu-id="3af0b-130">System. GUID</span><span class="sxs-lookup"><span data-stu-id="3af0b-130">System.Guid</span></span>

### <span data-ttu-id="3af0b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3af0b-131">System.String</span></span>

## <span data-ttu-id="3af0b-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3af0b-132">OUTPUTS</span></span>

### <span data-ttu-id="3af0b-133">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="3af0b-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="3af0b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3af0b-134">NOTES</span></span>

## <span data-ttu-id="3af0b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3af0b-135">RELATED LINKS</span></span>

[<span data-ttu-id="3af0b-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3af0b-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="3af0b-137">Регистрация — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3af0b-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="3af0b-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="3af0b-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


