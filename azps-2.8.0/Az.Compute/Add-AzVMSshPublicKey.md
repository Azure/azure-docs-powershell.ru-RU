---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 7e1ad3c052c30744762e4e5ec53bfb09b89a3056
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727517"
---
# <span data-ttu-id="a7707-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="a7707-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="a7707-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a7707-102">SYNOPSIS</span></span>
<span data-ttu-id="a7707-103">Добавляет открытые ключи для SSH для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7707-103">Adds the public keys for SSH for a virtual machine.</span></span>

## <span data-ttu-id="a7707-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a7707-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7707-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7707-105">DESCRIPTION</span></span>
<span data-ttu-id="a7707-106">Командлет **Add-AzVMSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальной машине Linux по защищенной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="a7707-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="a7707-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a7707-107">EXAMPLES</span></span>

### <span data-ttu-id="a7707-108">Пример 1: Добавление открытого ключа для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="a7707-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="a7707-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzVM** .</span><span class="sxs-lookup"><span data-stu-id="a7707-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="a7707-110">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="a7707-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="a7707-111">Вторая команда добавляет открытый ключ в расположение в VirtualMachine07, которое указывает параметр path.</span><span class="sxs-lookup"><span data-stu-id="a7707-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="a7707-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a7707-112">PARAMETERS</span></span>

### <span data-ttu-id="a7707-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7707-113">-DefaultProfile</span></span>
<span data-ttu-id="a7707-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7707-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7707-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="a7707-115">-KeyData</span></span>
<span data-ttu-id="a7707-116">Задает базовую кодировку 64 для открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="a7707-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="a7707-117">Вы можете подключаться к виртуальной машине Linux с помощью SSH или ключа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="a7707-117">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="a7707-118">-Path</span><span class="sxs-lookup"><span data-stu-id="a7707-118">-Path</span></span>
<span data-ttu-id="a7707-119">Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="a7707-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="a7707-120">Если файл уже существует, этот командлет добавляет ключ к файлу.</span><span class="sxs-lookup"><span data-stu-id="a7707-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="a7707-121">-VM</span><span class="sxs-lookup"><span data-stu-id="a7707-121">-VM</span></span>
<span data-ttu-id="a7707-122">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a7707-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="a7707-123">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="a7707-123">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="a7707-124">Вы можете использовать командлет [New-AzVMConfig](./New-AzVMConfig.md) для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a7707-124">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="a7707-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7707-125">CommonParameters</span></span>
<span data-ttu-id="a7707-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a7707-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7707-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7707-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7707-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a7707-128">INPUTS</span></span>

### <span data-ttu-id="a7707-129">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a7707-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="a7707-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a7707-130">System.String</span></span>

## <span data-ttu-id="a7707-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7707-131">OUTPUTS</span></span>

### <span data-ttu-id="a7707-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="a7707-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="a7707-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="a7707-133">NOTES</span></span>

## <span data-ttu-id="a7707-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7707-134">RELATED LINKS</span></span>

[<span data-ttu-id="a7707-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a7707-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="a7707-136">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="a7707-136">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
