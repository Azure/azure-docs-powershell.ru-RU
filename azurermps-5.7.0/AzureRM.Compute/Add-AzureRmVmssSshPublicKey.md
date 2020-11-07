---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 6ca619ba75fcf639e36650dc66d45d2f86ec8375
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734487"
---
# <span data-ttu-id="03499-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="03499-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="03499-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03499-102">SYNOPSIS</span></span>
<span data-ttu-id="03499-103">Добавляет открытые ключи SSH в VMSS.</span><span class="sxs-lookup"><span data-stu-id="03499-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03499-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03499-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03499-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03499-105">DESCRIPTION</span></span>
<span data-ttu-id="03499-106">Командлет **Add-AzureRmVmssSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальным машинам с установленной масштабируемостью виртуальных машин (VMSS) по защищенной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="03499-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="03499-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03499-107">EXAMPLES</span></span>

### <span data-ttu-id="03499-108">Пример 1: Добавление открытого ключа SSH в VMSS</span><span class="sxs-lookup"><span data-stu-id="03499-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="03499-109">В этом примере в VMSS добавляется открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="03499-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="03499-110">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="03499-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="03499-111">Вторая команда добавляет ключ SSH с указанными данными ключа и сохраняет ключ по указанному пути на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="03499-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="03499-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03499-112">PARAMETERS</span></span>

### <span data-ttu-id="03499-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="03499-113">-KeyData</span></span>
<span data-ttu-id="03499-114">Задает данные открытого ключа RSA (SSH).</span><span class="sxs-lookup"><span data-stu-id="03499-114">Specifies a SSH RSA public key data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03499-115">-Path</span><span class="sxs-lookup"><span data-stu-id="03499-115">-Path</span></span>
<span data-ttu-id="03499-116">Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="03499-116">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="03499-117">Если файл уже существует, этот командлет добавляет ключ к файлу.</span><span class="sxs-lookup"><span data-stu-id="03499-117">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03499-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="03499-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="03499-119">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="03499-119">Specifies the VMSS object.</span></span>
<span data-ttu-id="03499-120">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="03499-120">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03499-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03499-121">-Confirm</span></span>
<span data-ttu-id="03499-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03499-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03499-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03499-123">-WhatIf</span></span>
<span data-ttu-id="03499-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03499-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03499-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03499-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03499-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03499-126">CommonParameters</span></span>
<span data-ttu-id="03499-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03499-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03499-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03499-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03499-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03499-129">INPUTS</span></span>

### <span data-ttu-id="03499-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="03499-130">None</span></span>
<span data-ttu-id="03499-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="03499-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="03499-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03499-132">OUTPUTS</span></span>

###  
<span data-ttu-id="03499-133">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="03499-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="03499-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="03499-134">NOTES</span></span>

## <span data-ttu-id="03499-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03499-135">RELATED LINKS</span></span>

[<span data-ttu-id="03499-136">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="03499-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
