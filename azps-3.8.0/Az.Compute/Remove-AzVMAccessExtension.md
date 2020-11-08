---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 6c02a8381ca1cda4fec6fb52ea3d798884b45bad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066582"
---
# <span data-ttu-id="bf83f-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bf83f-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="bf83f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bf83f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf83f-103">Удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf83f-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="bf83f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bf83f-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf83f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf83f-105">DESCRIPTION</span></span>
<span data-ttu-id="bf83f-106">Командлет **Remove-AzVMAccessExtension** удаляет расширение виртуальной машины доступа к виртуальной машине (VMAccess) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf83f-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="bf83f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bf83f-107">EXAMPLES</span></span>

## <span data-ttu-id="bf83f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bf83f-108">PARAMETERS</span></span>

### <span data-ttu-id="bf83f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf83f-109">-DefaultProfile</span></span>
<span data-ttu-id="bf83f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf83f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf83f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="bf83f-111">-Force</span></span>
<span data-ttu-id="bf83f-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="bf83f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf83f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bf83f-113">-Name</span></span>
<span data-ttu-id="bf83f-114">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bf83f-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="bf83f-115">-Wait</span><span class="sxs-lookup"><span data-stu-id="bf83f-115">-NoWait</span></span>
<span data-ttu-id="bf83f-116">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="bf83f-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bf83f-117">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="bf83f-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bf83f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf83f-118">-ResourceGroupName</span></span>
<span data-ttu-id="bf83f-119">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf83f-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bf83f-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="bf83f-120">-VMName</span></span>
<span data-ttu-id="bf83f-121">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf83f-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="bf83f-122">Этот командлет удаляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="bf83f-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf83f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf83f-123">-Confirm</span></span>
<span data-ttu-id="bf83f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bf83f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf83f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf83f-125">-WhatIf</span></span>
<span data-ttu-id="bf83f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bf83f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf83f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bf83f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf83f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf83f-128">CommonParameters</span></span>
<span data-ttu-id="bf83f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bf83f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf83f-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf83f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf83f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bf83f-131">INPUTS</span></span>

### <span data-ttu-id="bf83f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf83f-132">System.String</span></span>

## <span data-ttu-id="bf83f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf83f-133">OUTPUTS</span></span>

### <span data-ttu-id="bf83f-134">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bf83f-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bf83f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf83f-135">NOTES</span></span>

## <span data-ttu-id="bf83f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf83f-136">RELATED LINKS</span></span>

[<span data-ttu-id="bf83f-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bf83f-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="bf83f-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="bf83f-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="bf83f-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="bf83f-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
