---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 0ba5f9cd618c86eec15eb8b0a02956e5997fc627
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509241"
---
# <span data-ttu-id="28309-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="28309-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="28309-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28309-102">SYNOPSIS</span></span>
<span data-ttu-id="28309-103">Добавляет общедоступные ключи SSH в VMSS.</span><span class="sxs-lookup"><span data-stu-id="28309-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="28309-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="28309-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28309-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28309-105">DESCRIPTION</span></span>
<span data-ttu-id="28309-106">С помощью **cmdlet Add-AzVmssSshPublicKey** можно добавить общедоступные ключи, которые можно использовать для подключения к виртуальной машине (VMSS) по безопасной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="28309-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="28309-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="28309-107">EXAMPLES</span></span>

### <span data-ttu-id="28309-108">Пример 1. Добавление открытого ключа SSH в VMSS</span><span class="sxs-lookup"><span data-stu-id="28309-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="28309-109">В этом примере к VMSS добавляется открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="28309-109">This example adds an SSH public key to the VMSS.</span></span>
<span data-ttu-id="28309-110">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="28309-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="28309-111">Вторая команда добавляет ключ SSH с указанными ключевыми данными и сохраняет ключ в указанном пути на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="28309-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="28309-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28309-112">PARAMETERS</span></span>

### <span data-ttu-id="28309-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28309-113">-DefaultProfile</span></span>
<span data-ttu-id="28309-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="28309-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28309-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="28309-115">-KeyData</span></span>
<span data-ttu-id="28309-116">Указывает данные открытого ключа RSA службы SSH.</span><span class="sxs-lookup"><span data-stu-id="28309-116">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28309-117">-Path</span><span class="sxs-lookup"><span data-stu-id="28309-117">-Path</span></span>
<span data-ttu-id="28309-118">Указывает полный путь к файлу на виртуальной машине, где этот cmdlet хранит общедоступный ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="28309-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="28309-119">Если файл уже существует, этот cmdlet будет выдан с ключом.</span><span class="sxs-lookup"><span data-stu-id="28309-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28309-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="28309-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="28309-121">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="28309-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="28309-122">Для создания объекта можно использовать [cmdlet New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="28309-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28309-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28309-123">-Confirm</span></span>
<span data-ttu-id="28309-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="28309-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28309-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28309-125">-WhatIf</span></span>
<span data-ttu-id="28309-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28309-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="28309-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="28309-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28309-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28309-128">CommonParameters</span></span>
<span data-ttu-id="28309-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28309-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28309-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28309-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28309-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="28309-131">INPUTS</span></span>

### <span data-ttu-id="28309-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="28309-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="28309-133">System.String</span><span class="sxs-lookup"><span data-stu-id="28309-133">System.String</span></span>

## <span data-ttu-id="28309-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="28309-134">OUTPUTS</span></span>

### <span data-ttu-id="28309-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMa modelseScaleSet</span><span class="sxs-lookup"><span data-stu-id="28309-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="28309-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="28309-136">NOTES</span></span>

## <span data-ttu-id="28309-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28309-137">RELATED LINKS</span></span>

[<span data-ttu-id="28309-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="28309-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
