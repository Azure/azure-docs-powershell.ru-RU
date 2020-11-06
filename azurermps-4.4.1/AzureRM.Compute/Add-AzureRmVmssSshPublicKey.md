---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9C216103-EB77-468E-8684-F5E5400B73A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSshPublicKey.md
ms.openlocfilehash: 113af7a35ffee5960f4be6fe2fe989d9c1b36956
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568087"
---
# <span data-ttu-id="89ca6-101">Add-AzureRmVmssSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="89ca6-101">Add-AzureRmVmssSshPublicKey</span></span>

## <span data-ttu-id="89ca6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="89ca6-103">Добавляет открытые ключи SSH в VMSS.</span><span class="sxs-lookup"><span data-stu-id="89ca6-103">Adds SSH public keys to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89ca6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89ca6-104">SYNTAX</span></span>

```
Add-AzureRmVmssSshPublicKey [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Path] <String>]
 [[-KeyData] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89ca6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ca6-105">DESCRIPTION</span></span>
<span data-ttu-id="89ca6-106">Командлет **Add-AzureRmVmssSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальным машинам с установленной масштабируемостью виртуальных машин (VMSS) по защищенной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="89ca6-106">The **Add-AzureRmVmssSshPublicKey** cmdlet adds the public keys that you can use to connect to the Virtual Machine Scale Set (VMSS) virtual machines over Secure Shell (SSH).</span></span>

## <span data-ttu-id="89ca6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89ca6-107">EXAMPLES</span></span>

### <span data-ttu-id="89ca6-108">Пример 1: Добавление открытого ключа SSH в VMSS</span><span class="sxs-lookup"><span data-stu-id="89ca6-108">Example 1: Add an SSH public key to the VMSS</span></span>
```
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSshPublicKey -VirtualMachineScaleSet $VMSS -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="89ca6-109">В этом примере в VMSS добавляется открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="89ca6-109">This example adds an SSH public key to the VMSS.</span></span>

<span data-ttu-id="89ca6-110">Первая команда использует командлет **New-AzureRmVmssConfig** для создания объекта конфигурации VMSS и сохраняет результат в переменной с именем $VMSS.</span><span class="sxs-lookup"><span data-stu-id="89ca6-110">The first command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="89ca6-111">Вторая команда добавляет ключ SSH с указанными данными ключа и сохраняет ключ по указанному пути на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="89ca6-111">The second command adds an SSH key with the specified key data and stores the key at the specified path on the virtual machine.</span></span>

## <span data-ttu-id="89ca6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89ca6-112">PARAMETERS</span></span>

### <span data-ttu-id="89ca6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ca6-113">-DefaultProfile</span></span>
<span data-ttu-id="89ca6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89ca6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89ca6-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="89ca6-115">-KeyData</span></span>
<span data-ttu-id="89ca6-116">Задает данные открытого ключа RSA (SSH).</span><span class="sxs-lookup"><span data-stu-id="89ca6-116">Specifies a SSH RSA public key data.</span></span>

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

### <span data-ttu-id="89ca6-117">-Path</span><span class="sxs-lookup"><span data-stu-id="89ca6-117">-Path</span></span>
<span data-ttu-id="89ca6-118">Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="89ca6-118">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="89ca6-119">Если файл уже существует, этот командлет добавляет ключ к файлу.</span><span class="sxs-lookup"><span data-stu-id="89ca6-119">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="89ca6-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="89ca6-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="89ca6-121">Указывает объект VMSS.</span><span class="sxs-lookup"><span data-stu-id="89ca6-121">Specifies the VMSS object.</span></span>
<span data-ttu-id="89ca6-122">Для создания объекта можно использовать командлет [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="89ca6-122">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="89ca6-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89ca6-123">-Confirm</span></span>
<span data-ttu-id="89ca6-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89ca6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ca6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ca6-125">-WhatIf</span></span>
<span data-ttu-id="89ca6-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89ca6-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="89ca6-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89ca6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ca6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ca6-128">CommonParameters</span></span>
<span data-ttu-id="89ca6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89ca6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ca6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89ca6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ca6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89ca6-131">INPUTS</span></span>

## <span data-ttu-id="89ca6-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ca6-132">OUTPUTS</span></span>

###  
<span data-ttu-id="89ca6-133">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="89ca6-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="89ca6-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="89ca6-134">NOTES</span></span>

## <span data-ttu-id="89ca6-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ca6-135">RELATED LINKS</span></span>

[<span data-ttu-id="89ca6-136">New-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="89ca6-136">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
