---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: da19894751c7b653dbc70d606a44464973d9b38c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568951"
---
# <span data-ttu-id="45c30-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="45c30-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="45c30-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45c30-102">SYNOPSIS</span></span>
<span data-ttu-id="45c30-103">Удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45c30-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45c30-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45c30-104">SYNTAX</span></span>

### <span data-ttu-id="45c30-105">Linux</span><span class="sxs-lookup"><span data-stu-id="45c30-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45c30-106">Windows</span><span class="sxs-lookup"><span data-stu-id="45c30-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c30-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45c30-107">DESCRIPTION</span></span>
<span data-ttu-id="45c30-108">Командлет **Remove-AzureVMChefExtension** удаляет расширение Chef из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="45c30-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="45c30-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45c30-109">EXAMPLES</span></span>

### <span data-ttu-id="45c30-110">Пример 1: удаление расширения Chef из виртуальной машины Windows</span><span class="sxs-lookup"><span data-stu-id="45c30-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="45c30-111">Эта команда удаляет расширение Chef с виртуальной машины под управлением Windows с именем WindowsVM001, которая входит в группу ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="45c30-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="45c30-112">Пример 2: удаление расширения Chef из виртуальной машины Linux</span><span class="sxs-lookup"><span data-stu-id="45c30-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="45c30-113">Эта команда удаляет расширение Chef с виртуальной машины на базе Linux с именем LinuxVM001, которая входит в группу ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="45c30-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="45c30-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45c30-114">PARAMETERS</span></span>

### <span data-ttu-id="45c30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c30-115">-DefaultProfile</span></span>
<span data-ttu-id="45c30-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45c30-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45c30-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="45c30-117">-Linux</span></span>
<span data-ttu-id="45c30-118">Указывает на то, что этот командлет предназначен для виртуальной машины Linux.</span><span class="sxs-lookup"><span data-stu-id="45c30-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="45c30-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45c30-119">-Name</span></span>
<span data-ttu-id="45c30-120">Указывает имя расширения Chef, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="45c30-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="45c30-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c30-121">-ResourceGroupName</span></span>
<span data-ttu-id="45c30-122">Указывает имя группы ресурсов, которая содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="45c30-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="45c30-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="45c30-123">-VMName</span></span>
<span data-ttu-id="45c30-124">Указывает имя виртуальной машины, для которой этот командлет удаляет расширение Chef.</span><span class="sxs-lookup"><span data-stu-id="45c30-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="45c30-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="45c30-125">-Windows</span></span>
<span data-ttu-id="45c30-126">Указывает на то, что этот командлет предназначен для виртуальной машины Windows.</span><span class="sxs-lookup"><span data-stu-id="45c30-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="45c30-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45c30-127">-Confirm</span></span>
<span data-ttu-id="45c30-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45c30-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c30-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c30-129">-WhatIf</span></span>
<span data-ttu-id="45c30-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45c30-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c30-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45c30-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c30-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c30-132">CommonParameters</span></span>
<span data-ttu-id="45c30-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45c30-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c30-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c30-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c30-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45c30-135">INPUTS</span></span>

### <span data-ttu-id="45c30-136">System. String</span><span class="sxs-lookup"><span data-stu-id="45c30-136">System.String</span></span>

## <span data-ttu-id="45c30-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45c30-137">OUTPUTS</span></span>

### <span data-ttu-id="45c30-138">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="45c30-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="45c30-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="45c30-139">NOTES</span></span>

## <span data-ttu-id="45c30-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45c30-140">RELATED LINKS</span></span>

[<span data-ttu-id="45c30-141">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="45c30-141">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="45c30-142">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="45c30-142">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
