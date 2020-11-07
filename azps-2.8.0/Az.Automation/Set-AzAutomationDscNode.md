---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 60023C8D-EA37-41DA-97E6-AF89F7F9BADD
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationDscNode.md
ms.openlocfilehash: 2b0d6096e9691445c939daea113dcdac2fa6c5fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727738"
---
# <span data-ttu-id="d7a30-101">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d7a30-101">Set-AzAutomationDscNode</span></span>

## <span data-ttu-id="d7a30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7a30-102">SYNOPSIS</span></span>
<span data-ttu-id="d7a30-103">Изменяет конфигурацию узла, с которой сопоставлен узел DSC.</span><span class="sxs-lookup"><span data-stu-id="d7a30-103">Modifies the node configuration that a DSC node is mapped to.</span></span>

## <span data-ttu-id="d7a30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7a30-104">SYNTAX</span></span>

```
Set-AzAutomationDscNode -Id <Guid> -NodeConfigurationName <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7a30-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7a30-105">DESCRIPTION</span></span>
<span data-ttu-id="d7a30-106">Командлет **Set-AzAutomationDscNode** изменяет конфигурацию узла ТД нужной конфигурации (DSC).</span><span class="sxs-lookup"><span data-stu-id="d7a30-106">The **Set-AzAutomationDscNode** cmdlet modifies an APS Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="d7a30-107">Служба автоматизации Azure хранит конфигурацию узла DSC как документ конфигурации MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="d7a30-107">Azure Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="d7a30-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7a30-108">EXAMPLES</span></span>

### <span data-ttu-id="d7a30-109">Пример 1: изменение сопоставления конфигурации узла</span><span class="sxs-lookup"><span data-stu-id="d7a30-109">Example 1: Modify node configuration mapping</span></span>
```
PS C:\>Set-AzAutomationDscNode -NodeConfigurationName "Contoso.NodeConfiguration01" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111c8a6067j8
```

<span data-ttu-id="d7a30-110">Эта команда назначает конфигурацию узла с именем Contoso. NodeConfiguration01 на узле с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="d7a30-110">This command assigns the node configuration named Contoso.NodeConfiguration01 to the node that has the specified GUID.</span></span>

## <span data-ttu-id="d7a30-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7a30-111">PARAMETERS</span></span>

### <span data-ttu-id="d7a30-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d7a30-112">-AutomationAccountName</span></span>
<span data-ttu-id="d7a30-113">Указывает имя учетной записи автоматизации, содержащей узел DSC, для которого этот командлет изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d7a30-113">Specifies the name of the Automation account that contains the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="d7a30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7a30-114">-DefaultProfile</span></span>
<span data-ttu-id="d7a30-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d7a30-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7a30-116">-Force</span><span class="sxs-lookup"><span data-stu-id="d7a30-116">-Force</span></span>
<span data-ttu-id="d7a30-117">ps_force команды для запуска без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d7a30-117">ps_force the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d7a30-118">-ID</span><span class="sxs-lookup"><span data-stu-id="d7a30-118">-Id</span></span>
<span data-ttu-id="d7a30-119">Указывает уникальный идентификатор узла DSC, для которого этот командлет изменяет конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="d7a30-119">Specifies the unique ID of the DSC node for which this cmdlet modifies the configuration.</span></span>

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

### <span data-ttu-id="d7a30-120">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d7a30-120">-NodeConfigurationName</span></span>
<span data-ttu-id="d7a30-121">Указывает имя конфигурации узла, на которую этот командлет сопоставляет узел.</span><span class="sxs-lookup"><span data-stu-id="d7a30-121">Specifies the name of the node configuration to which this cmdlet maps the node.</span></span>

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

### <span data-ttu-id="d7a30-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7a30-122">-ResourceGroupName</span></span>
<span data-ttu-id="d7a30-123">Указывает имя группы ресурсов, в которой этот командлет изменяет конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="d7a30-123">Specifies the name of a resource group in which this cmdlet modifies a DSC node configuration.</span></span>

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

### <span data-ttu-id="d7a30-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7a30-124">-Confirm</span></span>
<span data-ttu-id="d7a30-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7a30-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7a30-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7a30-126">-WhatIf</span></span>
<span data-ttu-id="d7a30-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7a30-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7a30-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7a30-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7a30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7a30-129">CommonParameters</span></span>
<span data-ttu-id="d7a30-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7a30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7a30-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7a30-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7a30-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7a30-132">INPUTS</span></span>

### <span data-ttu-id="d7a30-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d7a30-133">System.Guid</span></span>

### <span data-ttu-id="d7a30-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d7a30-134">System.String</span></span>

## <span data-ttu-id="d7a30-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7a30-135">OUTPUTS</span></span>

### <span data-ttu-id="d7a30-136">Microsoft. Azure. Commands. Automation. Model. DscNode</span><span class="sxs-lookup"><span data-stu-id="d7a30-136">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="d7a30-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7a30-137">NOTES</span></span>

## <span data-ttu-id="d7a30-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7a30-138">RELATED LINKS</span></span>

[<span data-ttu-id="d7a30-139">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d7a30-139">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="d7a30-140">Регистрация — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d7a30-140">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="d7a30-141">Отмена регистрации — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d7a30-141">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


