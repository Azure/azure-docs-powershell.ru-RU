---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: eaa1195e5cb853111b6e75efbff7e37bc8ff6881
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556844"
---
# <span data-ttu-id="7d499-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7d499-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="7d499-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d499-102">SYNOPSIS</span></span>
<span data-ttu-id="7d499-103">Изменяет конфигурацию узла, с которой сопоставлен узел DSC.</span><span class="sxs-lookup"><span data-stu-id="7d499-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d499-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d499-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7d499-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d499-105">DESCRIPTION</span></span>
<span data-ttu-id="7d499-106">Командлет **Set-AzureRmAutomationDscNode** изменяет конфигурацию узла ТД нужной конфигурации (DSC).</span><span class="sxs-lookup"><span data-stu-id="7d499-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="7d499-107">Служба автоматизации Azure хранит конфигурацию узла DSC как документ конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="7d499-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="7d499-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d499-108">EXAMPLES</span></span>

### <span data-ttu-id="7d499-109">Пример 1: изменение сопоставления конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="7d499-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="7d499-110">Эта команда назначает конфигурацию узла с именем Contoso. NodeConfiguration01 на узле с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="7d499-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="7d499-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d499-111">PARAMETERS</span></span>

### <span data-ttu-id="7d499-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7d499-112">-AutomationAccountName</span></span>
<span data-ttu-id="7d499-113">Указывает имя учетной записи автоматизации, содержащей узел DSC, для которого этот командлет изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="7d499-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="7d499-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d499-114">-DefaultProfile</span></span>
<span data-ttu-id="7d499-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d499-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d499-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7d499-116">-Force</span></span>
<span data-ttu-id="7d499-117">ps_force команды для запуска без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7d499-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7d499-118">-ID</span><span class="sxs-lookup"><span data-stu-id="7d499-118">-Id</span></span>
<span data-ttu-id="7d499-119">Указывает уникальный идентификатор узла DSC, для которого этот командлет изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="7d499-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="7d499-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7d499-120">-NodeConfigurationName</span></span>
<span data-ttu-id="7d499-121">Указывает имя конфигурации узла, на которую этот командлет сопоставляет узел.</span><span class="sxs-lookup"><span data-stu-id="7d499-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d499-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d499-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d499-123">Указывает имя группы ресурсов, в которой этот командлет изменяет конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="7d499-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="7d499-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d499-124">-Confirm</span></span>
<span data-ttu-id="7d499-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d499-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d499-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d499-126">-WhatIf</span></span>
<span data-ttu-id="7d499-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d499-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d499-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d499-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d499-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d499-129">CommonParameters</span></span>
<span data-ttu-id="7d499-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d499-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d499-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d499-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d499-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d499-132">INPUTS</span></span>

### <span data-ttu-id="7d499-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="7d499-133">System.Guid</span></span>

### <span data-ttu-id="7d499-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7d499-134">System.String</span></span>

## <span data-ttu-id="7d499-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d499-135">OUTPUTS</span></span>

### <span data-ttu-id="7d499-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="7d499-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="7d499-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d499-137">NOTES</span></span>

## <span data-ttu-id="7d499-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d499-138">RELATED LINKS</span></span>

[<span data-ttu-id="7d499-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7d499-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="7d499-140">Регистрация — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7d499-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="7d499-141">Отмена регистрации — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="7d499-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


