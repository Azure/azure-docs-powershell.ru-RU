---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssSshPublicKey.md
ms.openlocfilehash: 2fb8d5956cf783940e32f49019115dd911050749
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911580"
---
# <span data-ttu-id="53705-101">Add-AzVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="53705-101">Add-AzVmssSshPublicKey</span></span>

## <span data-ttu-id="53705-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53705-102">SYNOPSIS</span></span>
<span data-ttu-id="53705-103">Добавляет открытые ключи SSH в VMSS.</span><span class="sxs-lookup"><span data-stu-id="53705-103">Adds SSH public keys to the VMSS.</span></span>

## <span data-ttu-id="53705-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53705-104">SYNTAX</span></span>

```
Add-AzVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53705-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53705-105">DESCRIPTION</span></span>
<span data-ttu-id="53705-106">Командлет **Add-AzVmssSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальным машинам с установленной масштабируемостью виртуальных машин (VMSS) по защищенной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="53705-106">The **Add-AzVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="53705-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53705-107">EXAMPLES</span></span>

### <span data-ttu-id="53705-108">Пример 1: Добавление открытого ключа SSH в VMSS</span><span class="sxs-lookup"><span data-stu-id="53705-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="53705-109">В этом примере в VMSS добавляется открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="53705-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="53705-110">Первая команда использует командлет **New-AzVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="53705-110">The first command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="53705-111">Вторая команда добавляет ключ SSH с указанными данными ключа и сохраняет ключ по указанному пути на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="53705-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="53705-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53705-112">PARAMETERS</span></span>

### <span data-ttu-id="53705-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53705-113">-DefaultProfile</span></span>
<span data-ttu-id="53705-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53705-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53705-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="53705-115">-KeyData</span></span>
<span data-ttu-id="53705-116">Задает данные открытого ключа RSA (SSH).</span><span class="sxs-lookup"><span data-stu-id="53705-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="53705-117">-Path</span><span class="sxs-lookup"><span data-stu-id="53705-117">-Path</span></span>
<span data-ttu-id="53705-118">Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="53705-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="53705-119">Если файл уже существует, этот командлет добавляет ключ к файлу.</span><span class="sxs-lookup"><span data-stu-id="53705-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="53705-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="53705-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="53705-121">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="53705-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="53705-122">Для создания объекта можно использовать командлет [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="53705-122">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53705-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53705-123">-Confirm</span></span>
<span data-ttu-id="53705-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53705-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53705-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53705-125">-WhatIf</span></span>
<span data-ttu-id="53705-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53705-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53705-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53705-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53705-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53705-128">CommonParameters</span></span>
<span data-ttu-id="53705-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53705-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53705-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53705-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53705-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53705-131">INPUTS</span></span>

### <span data-ttu-id="53705-132">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="53705-132">VirtualMachineScaleSet</span></span>
<span data-ttu-id="53705-133">Параметр "VirtualMachineScaleSet" принимает значение типа "VirtualMachineScaleSet" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="53705-133">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="53705-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53705-134">OUTPUTS</span></span>

###  
<span data-ttu-id="53705-135">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="53705-135">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="53705-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="53705-136">NOTES</span></span>

## <span data-ttu-id="53705-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53705-137">RELATED LINKS</span></span>

[<span data-ttu-id="53705-138">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="53705-138">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
