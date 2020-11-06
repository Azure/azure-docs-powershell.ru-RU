---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 562b5b5986d544f5fa8d91e0f39cb34ef9dababd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566320"
---
# <span data-ttu-id="7cb3d-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7cb3d-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="7cb3d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7cb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb3d-103">Удаление расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7cb3d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7cb3d-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7cb3d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cb3d-105">DESCRIPTION</span></span>
<span data-ttu-id="7cb3d-106">Командлет **Remove-AzureRmAutomationSchedule** Удаляет расписание из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="7cb3d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7cb3d-107">EXAMPLES</span></span>

### <span data-ttu-id="7cb3d-108">Пример 1: Удаление расписания</span><span class="sxs-lookup"><span data-stu-id="7cb3d-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7cb3d-109">Эта команда изменяет описание расписания с именем Schedule01.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="7cb3d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7cb3d-110">PARAMETERS</span></span>

### <span data-ttu-id="7cb3d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7cb3d-111">-AutomationAccountName</span></span>
<span data-ttu-id="7cb3d-112">Указывает имя учетной записи автоматизации, для которой этот командлет изменяет расписание.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

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

### <span data-ttu-id="7cb3d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7cb3d-113">-Force</span></span>
<span data-ttu-id="7cb3d-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="7cb3d-114">ps_force</span></span>

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

### <span data-ttu-id="7cb3d-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7cb3d-115">-Name</span></span>
<span data-ttu-id="7cb3d-116">Указывает имя расписания, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-116">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cb3d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb3d-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cb3d-118">Указывает имя группы ресурсов, для которой этот командлет удаляет расписание.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-118">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="7cb3d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7cb3d-119">-Confirm</span></span>
<span data-ttu-id="7cb3d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb3d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb3d-121">-WhatIf</span></span>
<span data-ttu-id="7cb3d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb3d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb3d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cb3d-124">-DefaultProfile</span></span>
<span data-ttu-id="7cb3d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cb3d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb3d-126">CommonParameters</span></span>
<span data-ttu-id="7cb3d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7cb3d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb3d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb3d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb3d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7cb3d-129">INPUTS</span></span>

## <span data-ttu-id="7cb3d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7cb3d-130">OUTPUTS</span></span>

## <span data-ttu-id="7cb3d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7cb3d-131">NOTES</span></span>

## <span data-ttu-id="7cb3d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7cb3d-132">RELATED LINKS</span></span>

[<span data-ttu-id="7cb3d-133">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7cb3d-133">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="7cb3d-134">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7cb3d-134">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="7cb3d-135">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7cb3d-135">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


