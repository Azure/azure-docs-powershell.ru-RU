---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246788"
---
# <span data-ttu-id="f0496-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f0496-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="f0496-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0496-102">SYNOPSIS</span></span>
<span data-ttu-id="f0496-103">Удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0496-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="f0496-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0496-104">SYNTAX</span></span>

### <span data-ttu-id="f0496-105">Linux</span><span class="sxs-lookup"><span data-stu-id="f0496-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0496-106">Windows</span><span class="sxs-lookup"><span data-stu-id="f0496-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0496-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0496-107">DESCRIPTION</span></span>
<span data-ttu-id="f0496-108">Командлет **Remove-AzVMChefExtension** удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f0496-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="f0496-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0496-109">EXAMPLES</span></span>

### <span data-ttu-id="f0496-110">Пример 1: удаление расширения Chef из виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="f0496-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="f0496-111">Эта команда удаляет расширение Chef с виртуальной машины под управлением Windows с именем WindowsVM001, которая входит в группу ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="f0496-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="f0496-112">Пример 2: удаление расширения Chef из виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="f0496-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="f0496-113">Эта команда удаляет расширение Chef с виртуальной машины на базе Linux с именем LinuxVM001, которая входит в группу ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="f0496-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="f0496-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0496-114">PARAMETERS</span></span>

### <span data-ttu-id="f0496-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0496-115">-DefaultProfile</span></span>
<span data-ttu-id="f0496-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0496-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0496-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="f0496-117">-Linux</span></span>
<span data-ttu-id="f0496-118">Указывает на то, что этот командлет предназначен для виртуальной машины Linux.</span><span class="sxs-lookup"><span data-stu-id="f0496-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0496-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f0496-119">-Name</span></span>
<span data-ttu-id="f0496-120">Указывает имя расширения Chef, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f0496-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0496-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="f0496-121">-NoWait</span></span>
<span data-ttu-id="f0496-122">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="f0496-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f0496-123">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="f0496-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f0496-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0496-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0496-125">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="f0496-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="f0496-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="f0496-126">-VMName</span></span>
<span data-ttu-id="f0496-127">Указывает имя виртуальной машины, для которой этот командлет удаляет расширение Chef.</span><span class="sxs-lookup"><span data-stu-id="f0496-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="f0496-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="f0496-128">-Windows</span></span>
<span data-ttu-id="f0496-129">Указывает на то, что этот командлет предназначен для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="f0496-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0496-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0496-130">-Confirm</span></span>
<span data-ttu-id="f0496-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f0496-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0496-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0496-132">-WhatIf</span></span>
<span data-ttu-id="f0496-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f0496-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0496-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f0496-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0496-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0496-135">CommonParameters</span></span>
<span data-ttu-id="f0496-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0496-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0496-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0496-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0496-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0496-138">INPUTS</span></span>

### <span data-ttu-id="f0496-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f0496-139">System.String</span></span>

## <span data-ttu-id="f0496-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0496-140">OUTPUTS</span></span>

### <span data-ttu-id="f0496-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f0496-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f0496-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0496-142">NOTES</span></span>

## <span data-ttu-id="f0496-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0496-143">RELATED LINKS</span></span>

[<span data-ttu-id="f0496-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f0496-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="f0496-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="f0496-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)