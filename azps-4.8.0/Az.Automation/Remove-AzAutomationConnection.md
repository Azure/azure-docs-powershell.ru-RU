---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnection.md
ms.openlocfilehash: 1beda1b4db41c2aa3bf40bba7b72e0e684ba3196
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078516"
---
# <span data-ttu-id="56126-101">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="56126-101">Remove-AzAutomationConnection</span></span>

## <span data-ttu-id="56126-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56126-102">SYNOPSIS</span></span>
<span data-ttu-id="56126-103">Удаляет подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="56126-103">Removes an Automation connection.</span></span>

## <span data-ttu-id="56126-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56126-104">SYNTAX</span></span>

```
Remove-AzAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56126-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56126-105">DESCRIPTION</span></span>
<span data-ttu-id="56126-106">Командлет **Remove-AzAutomationConnection** удаляет подключение из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="56126-106">The **Remove-AzAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="56126-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56126-107">EXAMPLES</span></span>

### <span data-ttu-id="56126-108">Пример 1: Удаление соединения</span><span class="sxs-lookup"><span data-stu-id="56126-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="56126-109">Эта команда удаляет сертификат с именем ContosoConnection в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="56126-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="56126-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56126-110">PARAMETERS</span></span>

### <span data-ttu-id="56126-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56126-111">-AutomationAccountName</span></span>
<span data-ttu-id="56126-112">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет подключение.</span><span class="sxs-lookup"><span data-stu-id="56126-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="56126-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56126-113">-DefaultProfile</span></span>
<span data-ttu-id="56126-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="56126-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56126-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56126-115">-Force</span></span>
<span data-ttu-id="56126-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="56126-116">ps_force</span></span>

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

### <span data-ttu-id="56126-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="56126-117">-Name</span></span>
<span data-ttu-id="56126-118">Указывает имя подключения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="56126-118">Specifies the name of the connection that this cmdlet removes.</span></span>

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

### <span data-ttu-id="56126-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56126-119">-ResourceGroupName</span></span>
<span data-ttu-id="56126-120">Указывает имя группы ресурсов, для которой этот командлет удаляет подключение.</span><span class="sxs-lookup"><span data-stu-id="56126-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="56126-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56126-121">-Confirm</span></span>
<span data-ttu-id="56126-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56126-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56126-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56126-123">-WhatIf</span></span>
<span data-ttu-id="56126-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56126-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56126-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56126-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56126-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56126-126">CommonParameters</span></span>
<span data-ttu-id="56126-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56126-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56126-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56126-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56126-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56126-129">INPUTS</span></span>

### <span data-ttu-id="56126-130">System. String</span><span class="sxs-lookup"><span data-stu-id="56126-130">System.String</span></span>

## <span data-ttu-id="56126-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56126-131">OUTPUTS</span></span>

### <span data-ttu-id="56126-132">System. void</span><span class="sxs-lookup"><span data-stu-id="56126-132">System.Void</span></span>

## <span data-ttu-id="56126-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="56126-133">NOTES</span></span>

## <span data-ttu-id="56126-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56126-134">RELATED LINKS</span></span>

[<span data-ttu-id="56126-135">Get-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="56126-135">Get-AzAutomationConnection</span></span>](./Get-AzAutomationConnection.md)

[<span data-ttu-id="56126-136">New-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="56126-136">New-AzAutomationConnection</span></span>](./New-AzAutomationConnection.md)


