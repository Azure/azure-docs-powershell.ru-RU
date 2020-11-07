---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationDscNode.md
ms.openlocfilehash: 663573e7f4e111880c5ed0014dcad18480f665ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732390"
---
# <span data-ttu-id="f237d-101">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f237d-101">Set-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="f237d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f237d-102">SYNOPSIS</span></span>
<span data-ttu-id="f237d-103">Изменяет конфигурацию узла, с которой сопоставлен узел DSC.</span><span class="sxs-lookup"><span data-stu-id="f237d-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f237d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f237d-104">SYNTAX</span></span>

```
Set-AzureRmAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f237d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f237d-105">DESCRIPTION</span></span>
<span data-ttu-id="f237d-106">Командлет **Set-AzureRmAutomationDscNode** изменяет конфигурацию узла ТД нужной конфигурации (DSC).</span><span class="sxs-lookup"><span data-stu-id="f237d-106">The **Set-AzureRmAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="f237d-107">Служба автоматизации Azure хранит конфигурацию узла DSC как документ конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="f237d-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="f237d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f237d-108">EXAMPLES</span></span>

### <span data-ttu-id="f237d-109">Пример 1: изменение сопоставления конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="f237d-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzureRmAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="f237d-110">Эта команда назначает конфигурацию узла с именем Contoso. NodeConfiguration01 на узле с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="f237d-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="f237d-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f237d-111">PARAMETERS</span></span>

### <span data-ttu-id="f237d-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f237d-112">-AutomationAccountName</span></span>
<span data-ttu-id="f237d-113">Указывает имя учетной записи автоматизации, содержащей узел DSC, для которого этот командлет изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f237d-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="f237d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f237d-114">-DefaultProfile</span></span>
<span data-ttu-id="f237d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f237d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f237d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f237d-116">-Force</span></span>
<span data-ttu-id="f237d-117">ps_force команды для запуска без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f237d-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f237d-118">-ID</span><span class="sxs-lookup"><span data-stu-id="f237d-118">-Id</span></span>
<span data-ttu-id="f237d-119">Указывает уникальный идентификатор узла DSC, для которого этот командлет изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="f237d-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="f237d-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="f237d-120">-NodeConfigurationName</span></span>
<span data-ttu-id="f237d-121">Указывает имя конфигурации узла, на которую этот командлет сопоставляет узел.</span><span class="sxs-lookup"><span data-stu-id="f237d-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f237d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f237d-122">-ResourceGroupName</span></span>
<span data-ttu-id="f237d-123">Указывает имя группы ресурсов, в которой этот командлет изменяет конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="f237d-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="f237d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f237d-124">-Confirm</span></span>
<span data-ttu-id="f237d-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f237d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f237d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f237d-126">-WhatIf</span></span>
<span data-ttu-id="f237d-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f237d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f237d-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f237d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f237d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f237d-129">CommonParameters</span></span>
<span data-ttu-id="f237d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f237d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f237d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f237d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f237d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f237d-132">INPUTS</span></span>

### <span data-ttu-id="f237d-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="f237d-133">None</span></span>
<span data-ttu-id="f237d-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f237d-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f237d-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f237d-135">OUTPUTS</span></span>

### <span data-ttu-id="f237d-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="f237d-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="f237d-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f237d-137">NOTES</span></span>

## <span data-ttu-id="f237d-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f237d-138">RELATED LINKS</span></span>

[<span data-ttu-id="f237d-139">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f237d-139">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="f237d-140">Регистрация — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f237d-140">Register-AzureRmAutomationDscNode</span></span>](./Register-AzureRmAutomationDscNode.md)

[<span data-ttu-id="f237d-141">Отмена регистрации — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="f237d-141">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)


