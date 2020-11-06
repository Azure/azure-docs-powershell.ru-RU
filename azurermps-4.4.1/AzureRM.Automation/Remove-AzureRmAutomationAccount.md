---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationAccount.md
ms.openlocfilehash: 1b8e480a266459b21e6c357da156b4d4bc5165e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565678"
---
# <span data-ttu-id="1b2aa-101">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1b2aa-101">Remove-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="1b2aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1b2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2aa-103">Удаление учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-103">Removes an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1b2aa-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b2aa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2aa-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2aa-106">Командлет **Remove-AzureRmAutomationAccount** удаляет учетную запись службы автоматизации Azure из группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-106">The **Remove-AzureRmAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>

<span data-ttu-id="1b2aa-107">Дополнительные сведения об учетных записях автоматизации можно найти в командлете New-AzureRmAutomationAccount.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-107">For more information about Automation accounts, see the New-AzureRmAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="1b2aa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1b2aa-108">EXAMPLES</span></span>

### <span data-ttu-id="1b2aa-109">Пример 1: Удаление учетной записи автоматизации</span><span class="sxs-lookup"><span data-stu-id="1b2aa-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1b2aa-110">Эта команда удаляет учетную запись автоматизации с именем ContosoAutomationAccount без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="1b2aa-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1b2aa-111">PARAMETERS</span></span>

### <span data-ttu-id="1b2aa-112">-Force</span><span class="sxs-lookup"><span data-stu-id="1b2aa-112">-Force</span></span>
<span data-ttu-id="1b2aa-113">ps_force</span><span class="sxs-lookup"><span data-stu-id="1b2aa-113">ps_force</span></span>

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

### <span data-ttu-id="1b2aa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1b2aa-114">-Name</span></span>
<span data-ttu-id="1b2aa-115">Указывает имя учетной записи автоматизации, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-115">Specifies the name of the Automation account that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2aa-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b2aa-116">-ResourceGroupName</span></span>
<span data-ttu-id="1b2aa-117">Указывает имя группы ресурсов, из которой этот командлет удаляет учетную запись автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-117">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="1b2aa-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b2aa-118">-Confirm</span></span>
<span data-ttu-id="1b2aa-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b2aa-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b2aa-120">-WhatIf</span></span>
<span data-ttu-id="1b2aa-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b2aa-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b2aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2aa-123">-DefaultProfile</span></span>
<span data-ttu-id="1b2aa-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2aa-125">CommonParameters</span></span>
<span data-ttu-id="1b2aa-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1b2aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2aa-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b2aa-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2aa-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1b2aa-128">INPUTS</span></span>

## <span data-ttu-id="1b2aa-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b2aa-129">OUTPUTS</span></span>

### <span data-ttu-id="1b2aa-130">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1b2aa-130">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="1b2aa-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1b2aa-131">NOTES</span></span>

## <span data-ttu-id="1b2aa-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b2aa-132">RELATED LINKS</span></span>

[<span data-ttu-id="1b2aa-133">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1b2aa-133">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="1b2aa-134">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1b2aa-134">New-AzureRmAutomationAccount</span></span>](./New-AzureRmAutomationAccount.md)

[<span data-ttu-id="1b2aa-135">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1b2aa-135">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)


