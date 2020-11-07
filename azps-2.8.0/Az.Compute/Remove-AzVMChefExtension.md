---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 8a64b97fb936daae2840392abe7dff8702207638
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721772"
---
# <span data-ttu-id="9232a-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9232a-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="9232a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9232a-102">SYNOPSIS</span></span>
<span data-ttu-id="9232a-103">Удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9232a-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="9232a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9232a-104">SYNTAX</span></span>

### <span data-ttu-id="9232a-105">Linux</span><span class="sxs-lookup"><span data-stu-id="9232a-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9232a-106">Windows</span><span class="sxs-lookup"><span data-stu-id="9232a-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9232a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9232a-107">DESCRIPTION</span></span>
<span data-ttu-id="9232a-108">Командлет **Remove-AzVMChefExtension** удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9232a-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="9232a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9232a-109">EXAMPLES</span></span>

### <span data-ttu-id="9232a-110">Пример 1: удаление расширения Chef из виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="9232a-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="9232a-111">Эта команда удаляет расширение Chef с виртуальной машины под управлением Windows с именем WindowsVM001, которая входит в группу ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="9232a-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="9232a-112">Пример 2: удаление расширения Chef из виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="9232a-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="9232a-113">Эта команда удаляет расширение Chef с виртуальной машины на базе Linux с именем LinuxVM001, которая входит в группу ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="9232a-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="9232a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9232a-114">PARAMETERS</span></span>

### <span data-ttu-id="9232a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9232a-115">-DefaultProfile</span></span>
<span data-ttu-id="9232a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9232a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9232a-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="9232a-117">-Linux</span></span>
<span data-ttu-id="9232a-118">Указывает на то, что этот командлет предназначен для виртуальной машины Linux.</span><span class="sxs-lookup"><span data-stu-id="9232a-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="9232a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9232a-119">-Name</span></span>
<span data-ttu-id="9232a-120">Указывает имя расширения Chef, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9232a-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9232a-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="9232a-121">-NoWait</span></span>
<span data-ttu-id="9232a-122">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="9232a-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9232a-123">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="9232a-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="9232a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9232a-124">-ResourceGroupName</span></span>
<span data-ttu-id="9232a-125">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="9232a-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="9232a-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="9232a-126">-VMName</span></span>
<span data-ttu-id="9232a-127">Указывает имя виртуальной машины, для которой этот командлет удаляет расширение Chef.</span><span class="sxs-lookup"><span data-stu-id="9232a-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="9232a-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="9232a-128">-Windows</span></span>
<span data-ttu-id="9232a-129">Указывает на то, что этот командлет предназначен для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="9232a-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="9232a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9232a-130">-Confirm</span></span>
<span data-ttu-id="9232a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9232a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9232a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9232a-132">-WhatIf</span></span>
<span data-ttu-id="9232a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9232a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9232a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9232a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9232a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9232a-135">CommonParameters</span></span>
<span data-ttu-id="9232a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9232a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9232a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9232a-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9232a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9232a-138">INPUTS</span></span>

### <span data-ttu-id="9232a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="9232a-139">System.String</span></span>

## <span data-ttu-id="9232a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9232a-140">OUTPUTS</span></span>

### <span data-ttu-id="9232a-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9232a-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9232a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="9232a-142">NOTES</span></span>

## <span data-ttu-id="9232a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9232a-143">RELATED LINKS</span></span>

[<span data-ttu-id="9232a-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9232a-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="9232a-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="9232a-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
