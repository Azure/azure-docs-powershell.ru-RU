---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248401"
---
# <span data-ttu-id="47aca-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="47aca-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="47aca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="47aca-102">SYNOPSIS</span></span>
<span data-ttu-id="47aca-103">Удаляет расширение из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="47aca-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="47aca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="47aca-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47aca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="47aca-105">DESCRIPTION</span></span>
<span data-ttu-id="47aca-106">Командлет **Remove-AzVMExtension** удаляет расширение из расширений виртуальных машин виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="47aca-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="47aca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="47aca-107">EXAMPLES</span></span>

### <span data-ttu-id="47aca-108">Пример 1: удаление расширения из виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="47aca-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="47aca-109">Эта команда удаляет расширение ContosoTest с виртуальной машины с именем VirtualMachine22 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="47aca-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="47aca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="47aca-110">PARAMETERS</span></span>

### <span data-ttu-id="47aca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47aca-111">-DefaultProfile</span></span>
<span data-ttu-id="47aca-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="47aca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47aca-113">-Force</span><span class="sxs-lookup"><span data-stu-id="47aca-113">-Force</span></span>
<span data-ttu-id="47aca-114">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="47aca-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="47aca-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="47aca-115">-Name</span></span>
<span data-ttu-id="47aca-116">Указывает имя расширения, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="47aca-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="47aca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47aca-117">-ResourceGroupName</span></span>
<span data-ttu-id="47aca-118">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="47aca-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="47aca-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="47aca-119">-VMName</span></span>
<span data-ttu-id="47aca-120">Указывает имя виртуальной машины, с помощью которой этот командлет удаляет расширение.</span><span class="sxs-lookup"><span data-stu-id="47aca-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="47aca-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47aca-121">-Confirm</span></span>
<span data-ttu-id="47aca-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="47aca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47aca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47aca-123">-WhatIf</span></span>
<span data-ttu-id="47aca-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="47aca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47aca-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="47aca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47aca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47aca-126">CommonParameters</span></span>
<span data-ttu-id="47aca-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="47aca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47aca-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47aca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47aca-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="47aca-129">INPUTS</span></span>

### <span data-ttu-id="47aca-130">System. String</span><span class="sxs-lookup"><span data-stu-id="47aca-130">System.String</span></span>

## <span data-ttu-id="47aca-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="47aca-131">OUTPUTS</span></span>

### <span data-ttu-id="47aca-132">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="47aca-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="47aca-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="47aca-133">NOTES</span></span>

## <span data-ttu-id="47aca-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="47aca-134">RELATED LINKS</span></span>

[<span data-ttu-id="47aca-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="47aca-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="47aca-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="47aca-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

