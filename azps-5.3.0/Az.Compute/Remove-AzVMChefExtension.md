---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 79b16afbd6188682ff68ba5b2f2d9ccae67ff630
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519527"
---
# <span data-ttu-id="68faa-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="68faa-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="68faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68faa-102">SYNOPSIS</span></span>
<span data-ttu-id="68faa-103">Удаляет расширение "Валенка" с виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68faa-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="68faa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68faa-104">SYNTAX</span></span>

### <span data-ttu-id="68faa-105">Linux</span><span class="sxs-lookup"><span data-stu-id="68faa-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68faa-106">Windows</span><span class="sxs-lookup"><span data-stu-id="68faa-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68faa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68faa-107">DESCRIPTION</span></span>
<span data-ttu-id="68faa-108">При **этом с** виртуальной машины удаляется расширение "Неотвеченный".</span><span class="sxs-lookup"><span data-stu-id="68faa-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="68faa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68faa-109">EXAMPLES</span></span>

### <span data-ttu-id="68faa-110">Пример 1. Удаление расширения Валенки с виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="68faa-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="68faa-111">Эта команда удаляет расширение в составе группы ресурсов ResourceGroup001 из виртуальной машины Windows с именем WindowsVM001.</span><span class="sxs-lookup"><span data-stu-id="68faa-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="68faa-112">Пример 2. Удаление расширения Валенки с виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="68faa-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="68faa-113">Эта команда удаляет расширение Валенки из виртуальной машины На Linux с именем LinuxVM001, которое принадлежит к группе ресурсов ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="68faa-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="68faa-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68faa-114">PARAMETERS</span></span>

### <span data-ttu-id="68faa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68faa-115">-DefaultProfile</span></span>
<span data-ttu-id="68faa-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68faa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68faa-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="68faa-117">-Linux</span></span>
<span data-ttu-id="68faa-118">Указывает на то, что этот cmdlet нацелен на виртуальную машину Linux.</span><span class="sxs-lookup"><span data-stu-id="68faa-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="68faa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="68faa-119">-Name</span></span>
<span data-ttu-id="68faa-120">Указывает имя расширения "Вадим", которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68faa-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="68faa-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="68faa-121">-NoWait</span></span>
<span data-ttu-id="68faa-122">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="68faa-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="68faa-123">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="68faa-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="68faa-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68faa-124">-ResourceGroupName</span></span>
<span data-ttu-id="68faa-125">Имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="68faa-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="68faa-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="68faa-126">-VMName</span></span>
<span data-ttu-id="68faa-127">Указывает имя виртуальной машины, для которой этот cmdlet удаляет расширение "Неявный".</span><span class="sxs-lookup"><span data-stu-id="68faa-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="68faa-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="68faa-128">-Windows</span></span>
<span data-ttu-id="68faa-129">Указывает на то, что этот cmdlet нацелен на виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="68faa-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="68faa-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68faa-130">-Confirm</span></span>
<span data-ttu-id="68faa-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68faa-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68faa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68faa-132">-WhatIf</span></span>
<span data-ttu-id="68faa-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68faa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68faa-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="68faa-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68faa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68faa-135">CommonParameters</span></span>
<span data-ttu-id="68faa-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68faa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68faa-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68faa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68faa-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68faa-138">INPUTS</span></span>

### <span data-ttu-id="68faa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="68faa-139">System.String</span></span>

## <span data-ttu-id="68faa-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68faa-140">OUTPUTS</span></span>

### <span data-ttu-id="68faa-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="68faa-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="68faa-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68faa-142">NOTES</span></span>

## <span data-ttu-id="68faa-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68faa-143">RELATED LINKS</span></span>

[<span data-ttu-id="68faa-144">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="68faa-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="68faa-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="68faa-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
