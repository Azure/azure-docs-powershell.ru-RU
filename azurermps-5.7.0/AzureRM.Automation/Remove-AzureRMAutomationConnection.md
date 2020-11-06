---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C1C0F69D-6A3F-4523-BB70-27676A3DDCBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationConnection.md
ms.openlocfilehash: 4fb4bbab5c774cacd274754a106aacfeebdb533c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569060"
---
# <span data-ttu-id="3797f-101">Remove-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3797f-101">Remove-AzureRmAutomationConnection</span></span>

## <span data-ttu-id="3797f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3797f-102">SYNOPSIS</span></span>
<span data-ttu-id="3797f-103">Удаляет подключение автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3797f-103">Removes an Automation connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3797f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3797f-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationConnection [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3797f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3797f-105">DESCRIPTION</span></span>
<span data-ttu-id="3797f-106">Командлет **Remove-AzureRmAutomationConnection** удаляет подключение из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3797f-106">The **Remove-AzureRmAutomationConnection** cmdlet removes a connection from Azure Automation.</span></span>

## <span data-ttu-id="3797f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3797f-107">EXAMPLES</span></span>

### <span data-ttu-id="3797f-108">Пример 1: Удаление соединения</span><span class="sxs-lookup"><span data-stu-id="3797f-108">Example 1: Remove a connection</span></span>
```
PS C:\>Remove-AzureRmAutomationConnection -AutomationAccountName "Contoso17" -Name "ContosoConnection" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3797f-109">Эта команда удаляет сертификат с именем ContosoConnection в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3797f-109">This command removes a certificate named ContosoConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3797f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3797f-110">PARAMETERS</span></span>

### <span data-ttu-id="3797f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3797f-111">-AutomationAccountName</span></span>
<span data-ttu-id="3797f-112">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет подключение.</span><span class="sxs-lookup"><span data-stu-id="3797f-112">Specifies the name of the automation account for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="3797f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3797f-113">-DefaultProfile</span></span>
<span data-ttu-id="3797f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3797f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3797f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3797f-115">-Force</span></span>
<span data-ttu-id="3797f-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3797f-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797f-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3797f-117">-Name</span></span>
<span data-ttu-id="3797f-118">Указывает имя подключения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3797f-118">Specifies the name of the connection that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3797f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3797f-119">-ResourceGroupName</span></span>
<span data-ttu-id="3797f-120">Указывает имя группы ресурсов, для которой этот командлет удаляет подключение.</span><span class="sxs-lookup"><span data-stu-id="3797f-120">Specifies the name of the resource group for which this cmdlet removes a connection.</span></span>

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

### <span data-ttu-id="3797f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3797f-121">-Confirm</span></span>
<span data-ttu-id="3797f-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3797f-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3797f-123">-WhatIf</span></span>
<span data-ttu-id="3797f-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3797f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3797f-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3797f-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3797f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3797f-126">CommonParameters</span></span>
<span data-ttu-id="3797f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3797f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3797f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3797f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3797f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3797f-129">INPUTS</span></span>

### <span data-ttu-id="3797f-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3797f-130">None</span></span>
<span data-ttu-id="3797f-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3797f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3797f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3797f-132">OUTPUTS</span></span>

## <span data-ttu-id="3797f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="3797f-133">NOTES</span></span>

## <span data-ttu-id="3797f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3797f-134">RELATED LINKS</span></span>

[<span data-ttu-id="3797f-135">Get-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3797f-135">Get-AzureRmAutomationConnection</span></span>](./Get-AzureRMAutomationConnection.md)

[<span data-ttu-id="3797f-136">New-AzureRmAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="3797f-136">New-AzureRmAutomationConnection</span></span>](./New-AzureRMAutomationConnection.md)


