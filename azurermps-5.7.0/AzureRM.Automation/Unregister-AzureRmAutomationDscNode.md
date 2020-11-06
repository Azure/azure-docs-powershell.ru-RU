---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRmAutomationDscNode.md
ms.openlocfilehash: 486664833e585733dc02a5c6f1c94d8673dfc4a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567469"
---
# <span data-ttu-id="872a3-101">Unregister-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="872a3-101">Unregister-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="872a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="872a3-102">SYNOPSIS</span></span>
<span data-ttu-id="872a3-103">Удаляет узел DSC из управления с помощью учетной записи службы автоматизации.</span><span class="sxs-lookup"><span data-stu-id="872a3-103">Removes a DSC node from management by an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="872a3-104">SYNTAX</span></span>

```
Unregister-AzureRmAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="872a3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="872a3-105">DESCRIPTION</span></span>
<span data-ttu-id="872a3-106">Командлет **Unregister-AzureRmAutomationDscNode** удаляет узел настройки нужного состояния ТД из управления с помощью учетной записи службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="872a3-106">The **Unregister-AzureRmAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="872a3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="872a3-107">EXAMPLES</span></span>

### <span data-ttu-id="872a3-108">Пример 1: Удаление узла Azure DSC из управления с помощью учетной записи службы автоматизации</span><span class="sxs-lookup"><span data-stu-id="872a3-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="872a3-109">Эта команда удаляет узел DSC с указанным GUID из управления с помощью учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="872a3-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="872a3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="872a3-110">PARAMETERS</span></span>

### <span data-ttu-id="872a3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="872a3-111">-AutomationAccountName</span></span>
<span data-ttu-id="872a3-112">Указывает имя учетной записи автоматизации, из которой этот командлет удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="872a3-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="872a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872a3-113">-DefaultProfile</span></span>
<span data-ttu-id="872a3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="872a3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="872a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="872a3-115">-Force</span></span>
<span data-ttu-id="872a3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="872a3-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872a3-117">-ID</span><span class="sxs-lookup"><span data-stu-id="872a3-117">-Id</span></span>
<span data-ttu-id="872a3-118">Указывает уникальный идентификатор узла DSC, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="872a3-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="872a3-120">Указывает имя группы ресурсов, в которой командлет удаляет узел DSC.</span><span class="sxs-lookup"><span data-stu-id="872a3-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="872a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="872a3-121">-Confirm</span></span>
<span data-ttu-id="872a3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="872a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="872a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="872a3-123">-WhatIf</span></span>
<span data-ttu-id="872a3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="872a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="872a3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="872a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="872a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872a3-126">CommonParameters</span></span>
<span data-ttu-id="872a3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="872a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872a3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="872a3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872a3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="872a3-129">INPUTS</span></span>

### <span data-ttu-id="872a3-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="872a3-130">None</span></span>
<span data-ttu-id="872a3-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="872a3-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="872a3-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="872a3-132">OUTPUTS</span></span>

### <span data-ttu-id="872a3-133">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="872a3-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="872a3-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="872a3-134">NOTES</span></span>

## <span data-ttu-id="872a3-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="872a3-135">RELATED LINKS</span></span>

[<span data-ttu-id="872a3-136">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="872a3-136">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="872a3-137">Регистрация — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="872a3-137">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="872a3-138">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="872a3-138">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)


