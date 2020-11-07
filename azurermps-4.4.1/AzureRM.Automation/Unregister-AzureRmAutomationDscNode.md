---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 76de3ad08e6acb0035cfa2a9ca5d353fcbf38033
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734272"
---
# <span data-ttu-id="de52d-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="de52d-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="de52d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="de52d-102">SYNOPSIS</span></span>
<span data-ttu-id="de52d-103">Удаляет узел DSC из управления с помощью учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="de52d-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de52d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="de52d-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de52d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="de52d-105">DESCRIPTION</span></span>
<span data-ttu-id="de52d-106">Командлет **Unregister-AzureRmAutomationDscNode** удаляет узел настройки нужного состояния ТД из управления с помощью учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="de52d-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="de52d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="de52d-107">EXAMPLES</span></span>

### <span data-ttu-id="de52d-108">Пример 1: Удаление узла Azure DSC из управления с помощью учетной записи службы автоматизации</span><span class="sxs-lookup"><span data-stu-id="de52d-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="de52d-109">Эта команда удаляет узел DSC с указанным GUID из управления с помощью учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="de52d-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="de52d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="de52d-110">PARAMETERS</span></span>

### <span data-ttu-id="de52d-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de52d-111">-AutomationAccountName</span></span>
<span data-ttu-id="de52d-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="de52d-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="de52d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="de52d-113">-Force</span></span>
<span data-ttu-id="de52d-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="de52d-114">ps_force</span></span>

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

### <span data-ttu-id="de52d-115">-ID</span><span class="sxs-lookup"><span data-stu-id="de52d-115">-Id</span></span>
<span data-ttu-id="de52d-116">Указывает уникальный идентификатор узла DSC, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="de52d-116">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

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

### <span data-ttu-id="de52d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de52d-117">-ResourceGroupName</span></span>
<span data-ttu-id="de52d-118">Указывает имя группы ресурсов, в которой командлет удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="de52d-118">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="de52d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de52d-119">-Confirm</span></span>
<span data-ttu-id="de52d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="de52d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de52d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de52d-121">-WhatIf</span></span>
<span data-ttu-id="de52d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="de52d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de52d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="de52d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de52d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de52d-124">-DefaultProfile</span></span>
<span data-ttu-id="de52d-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="de52d-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de52d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de52d-126">CommonParameters</span></span>
<span data-ttu-id="de52d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="de52d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de52d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de52d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de52d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="de52d-129">INPUTS</span></span>

## <span data-ttu-id="de52d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="de52d-130">OUTPUTS</span></span>

### <span data-ttu-id="de52d-131">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="de52d-131">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="de52d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="de52d-132">NOTES</span></span>

## <span data-ttu-id="de52d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="de52d-133">RELATED LINKS</span></span>

[<span data-ttu-id="de52d-134">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="de52d-134">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="de52d-135">Регистрация — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="de52d-135">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="de52d-136">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="de52d-136">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


