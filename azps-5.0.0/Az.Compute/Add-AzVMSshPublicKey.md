---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249513"
---
# <span data-ttu-id="2f2e4-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2f2e4-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="2f2e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2f2e4-102">SYNOPSIS</span></span>
<span data-ttu-id="2f2e4-103">Добавляет открытые ключи для SSH для виртуальной машины при создании ВМ.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="2f2e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2f2e4-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f2e4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f2e4-105">DESCRIPTION</span></span>
<span data-ttu-id="2f2e4-106">Командлет **Add-AzVMSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальной машине Linux по защищенной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="2f2e4-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="2f2e4-107">Этот параметр не может использоваться после создания виртуальной машины, если при попытке использовать его после создания виртуальной машины без Update-AzVM ошибка не возникнет, но при использовании команды с параметром Update-AzVM команда завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="2f2e4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2f2e4-108">EXAMPLES</span></span>

### <span data-ttu-id="2f2e4-109">Пример 1: Добавление открытого ключа для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2f2e4-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="2f2e4-110">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="2f2e4-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="2f2e4-111">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="2f2e4-112">Вторая команда добавляет открытый ключ в расположение в VirtualMachine07, которое указывает параметр path.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="2f2e4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2f2e4-113">PARAMETERS</span></span>

### <span data-ttu-id="2f2e4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f2e4-114">-DefaultProfile</span></span>
<span data-ttu-id="2f2e4-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f2e4-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="2f2e4-116">-KeyData</span></span>
<span data-ttu-id="2f2e4-117">Задает базовую кодировку 64 для открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="2f2e4-118">Вы можете подключаться к виртуальной машине Linux с помощью SSH или ключа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="2f2e4-119">-Path</span><span class="sxs-lookup"><span data-stu-id="2f2e4-119">-Path</span></span>
<span data-ttu-id="2f2e4-120">Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="2f2e4-121">Если файл уже существует, этот командлет добавляет ключ к файлу.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="2f2e4-122">-VM</span><span class="sxs-lookup"><span data-stu-id="2f2e4-122">-VM</span></span>
<span data-ttu-id="2f2e4-123">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="2f2e4-124">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="2f2e4-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="2f2e4-125">Вы можете использовать командлет [New-AzVMConfig](./New-AzVMConfig.md) для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f2e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f2e4-126">CommonParameters</span></span>
<span data-ttu-id="2f2e4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2f2e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f2e4-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2f2e4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f2e4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2f2e4-129">INPUTS</span></span>

### <span data-ttu-id="2f2e4-130">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2f2e4-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2f2e4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="2f2e4-131">System.String</span></span>

## <span data-ttu-id="2f2e4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f2e4-132">OUTPUTS</span></span>

### <span data-ttu-id="2f2e4-133">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="2f2e4-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2f2e4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2f2e4-134">NOTES</span></span>

## <span data-ttu-id="2f2e4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f2e4-135">RELATED LINKS</span></span>

[<span data-ttu-id="2f2e4-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2f2e4-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2f2e4-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2f2e4-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
