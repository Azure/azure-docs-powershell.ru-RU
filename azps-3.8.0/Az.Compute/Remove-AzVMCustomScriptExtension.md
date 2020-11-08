---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 48e2a48eab4a75634f8868b2f25e435faf3de496
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066578"
---
# <span data-ttu-id="e0163-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e0163-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="e0163-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0163-102">SYNOPSIS</span></span>
<span data-ttu-id="e0163-103">Удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e0163-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="e0163-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0163-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0163-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0163-105">DESCRIPTION</span></span>
<span data-ttu-id="e0163-106">Командлет **Remove-AzVMCustomScriptExtension** удаляет расширение виртуальной машины специального сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e0163-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="e0163-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0163-107">EXAMPLES</span></span>

## <span data-ttu-id="e0163-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0163-108">PARAMETERS</span></span>

### <span data-ttu-id="e0163-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0163-109">-DefaultProfile</span></span>
<span data-ttu-id="e0163-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0163-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0163-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e0163-111">-Force</span></span>
<span data-ttu-id="e0163-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e0163-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e0163-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0163-113">-Name</span></span>
<span data-ttu-id="e0163-114">Указывает имя настраиваемого расширения скрипта, которое удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e0163-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0163-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="e0163-115">-NoWait</span></span>
<span data-ttu-id="e0163-116">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="e0163-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e0163-117">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="e0163-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e0163-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0163-118">-ResourceGroupName</span></span>
<span data-ttu-id="e0163-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e0163-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e0163-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="e0163-120">-VMName</span></span>
<span data-ttu-id="e0163-121">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет настраиваемое расширение сценария.</span><span class="sxs-lookup"><span data-stu-id="e0163-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0163-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0163-122">-Confirm</span></span>
<span data-ttu-id="e0163-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0163-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0163-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0163-124">-WhatIf</span></span>
<span data-ttu-id="e0163-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0163-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0163-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0163-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0163-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0163-127">CommonParameters</span></span>
<span data-ttu-id="e0163-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0163-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0163-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0163-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0163-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0163-130">INPUTS</span></span>

### <span data-ttu-id="e0163-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e0163-131">System.String</span></span>

## <span data-ttu-id="e0163-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0163-132">OUTPUTS</span></span>

### <span data-ttu-id="e0163-133">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e0163-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e0163-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0163-134">NOTES</span></span>

## <span data-ttu-id="e0163-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0163-135">RELATED LINKS</span></span>

[<span data-ttu-id="e0163-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e0163-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="e0163-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="e0163-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
