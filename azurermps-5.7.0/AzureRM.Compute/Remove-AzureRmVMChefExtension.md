---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563667"
---
# <span data-ttu-id="bfecf-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="bfecf-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="bfecf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfecf-102">SYNOPSIS</span></span>
<span data-ttu-id="bfecf-103">Удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bfecf-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfecf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfecf-104">SYNTAX</span></span>

### <span data-ttu-id="bfecf-105">Linux</span><span class="sxs-lookup"><span data-stu-id="bfecf-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfecf-106">Windows</span><span class="sxs-lookup"><span data-stu-id="bfecf-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfecf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfecf-107">DESCRIPTION</span></span>
<span data-ttu-id="bfecf-108">Командлет **Remove-AzureVMChefExtension** удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bfecf-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="bfecf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfecf-109">EXAMPLES</span></span>

### <span data-ttu-id="bfecf-110">Пример 1: удаление расширения Chef из виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="bfecf-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="bfecf-111">Эта команда удаляет расширение Chef с виртуальной машины под управлением Windows с именем WindowsVM001, которая входит в группу ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="bfecf-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="bfecf-112">Пример 2: удаление расширения Chef из виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="bfecf-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="bfecf-113">Эта команда удаляет расширение Chef с виртуальной машины на базе Linux с именем LinuxVM001, которая входит в группу ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="bfecf-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="bfecf-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfecf-114">PARAMETERS</span></span>

### <span data-ttu-id="bfecf-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="bfecf-115">-Linux</span></span>
<span data-ttu-id="bfecf-116">Указывает на то, что этот командлет предназначен для виртуальной машины Linux.</span><span class="sxs-lookup"><span data-stu-id="bfecf-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfecf-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfecf-117">-Name</span></span>
<span data-ttu-id="bfecf-118">Указывает имя расширения Chef, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bfecf-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfecf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfecf-119">-ResourceGroupName</span></span>
<span data-ttu-id="bfecf-120">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="bfecf-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="bfecf-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="bfecf-121">-VMName</span></span>
<span data-ttu-id="bfecf-122">Указывает имя виртуальной машины, для которой этот командлет удаляет расширение Chef.</span><span class="sxs-lookup"><span data-stu-id="bfecf-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bfecf-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="bfecf-123">-Windows</span></span>
<span data-ttu-id="bfecf-124">Указывает на то, что этот командлет предназначен для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="bfecf-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfecf-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bfecf-125">-Confirm</span></span>
<span data-ttu-id="bfecf-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bfecf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfecf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfecf-127">-WhatIf</span></span>
<span data-ttu-id="bfecf-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bfecf-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="bfecf-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bfecf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfecf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfecf-130">CommonParameters</span></span>
<span data-ttu-id="bfecf-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfecf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfecf-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfecf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfecf-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfecf-133">INPUTS</span></span>

### <span data-ttu-id="bfecf-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="bfecf-134">None</span></span>
<span data-ttu-id="bfecf-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="bfecf-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bfecf-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfecf-136">OUTPUTS</span></span>

## <span data-ttu-id="bfecf-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfecf-137">NOTES</span></span>

## <span data-ttu-id="bfecf-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfecf-138">RELATED LINKS</span></span>

[<span data-ttu-id="bfecf-139">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="bfecf-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="bfecf-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="bfecf-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
