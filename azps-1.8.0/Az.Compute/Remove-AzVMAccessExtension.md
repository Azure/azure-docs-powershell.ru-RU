---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: a409d4f6d09279aed6a22b9212894a1aca9cae1c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901194"
---
# <span data-ttu-id="a526f-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a526f-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="a526f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a526f-102">SYNOPSIS</span></span>
<span data-ttu-id="a526f-103">Удаляет расширение VMAccess из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a526f-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="a526f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a526f-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a526f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a526f-105">DESCRIPTION</span></span>
<span data-ttu-id="a526f-106">Командлет **Remove-AzVMAccessExtension** удаляет расширение виртуальной машины доступа к виртуальной машине (VMAccess) с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a526f-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="a526f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a526f-107">EXAMPLES</span></span>

## <span data-ttu-id="a526f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a526f-108">PARAMETERS</span></span>

### <span data-ttu-id="a526f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a526f-109">-DefaultProfile</span></span>
<span data-ttu-id="a526f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a526f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a526f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a526f-111">-Force</span></span>
<span data-ttu-id="a526f-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a526f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a526f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a526f-113">-Name</span></span>
<span data-ttu-id="a526f-114">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a526f-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a526f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a526f-115">-ResourceGroupName</span></span>
<span data-ttu-id="a526f-116">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a526f-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a526f-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="a526f-117">-VMName</span></span>
<span data-ttu-id="a526f-118">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a526f-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a526f-119">Этот командлет удаляет VMAccess для виртуальной машины, указывающей этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a526f-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a526f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a526f-120">-Confirm</span></span>
<span data-ttu-id="a526f-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a526f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a526f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a526f-122">-WhatIf</span></span>
<span data-ttu-id="a526f-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a526f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a526f-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a526f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a526f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a526f-125">CommonParameters</span></span>
<span data-ttu-id="a526f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a526f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a526f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a526f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a526f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a526f-128">INPUTS</span></span>

### <span data-ttu-id="a526f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a526f-129">System.String</span></span>

## <span data-ttu-id="a526f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a526f-130">OUTPUTS</span></span>

### <span data-ttu-id="a526f-131">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a526f-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a526f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="a526f-132">NOTES</span></span>

## <span data-ttu-id="a526f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a526f-133">RELATED LINKS</span></span>

[<span data-ttu-id="a526f-134">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a526f-134">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="a526f-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="a526f-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="a526f-136">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="a526f-136">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
