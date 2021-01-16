---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509254"
---
# <span data-ttu-id="e247c-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="e247c-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="e247c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e247c-102">SYNOPSIS</span></span>
<span data-ttu-id="e247c-103">Добавляет общедоступные ключи SSH для виртуальной машины при создании только виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e247c-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="e247c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e247c-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e247c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e247c-105">DESCRIPTION</span></span>
<span data-ttu-id="e247c-106">С **помощью cmdlet Add-AzVMSshPublicKey** можно добавить общедоступные ключи, которые можно использовать для подключения к виртуальной машине Linux через безопасную оболочку (SSH).</span><span class="sxs-lookup"><span data-stu-id="e247c-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="e247c-107">Этот не может использоваться после создания VM, если вы попытались использовать его после создания VM без Update-AzVM, ошибки не будет, если вы используете команду с Update-AzVM, команда будет иметь ошибку.</span><span class="sxs-lookup"><span data-stu-id="e247c-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="e247c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e247c-108">EXAMPLES</span></span>

### <span data-ttu-id="e247c-109">Пример 1. Добавление открытого ключа на виртуальную машину</span><span class="sxs-lookup"><span data-stu-id="e247c-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="e247c-110">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью **командлета Get-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="e247c-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="e247c-111">Эта команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e247c-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e247c-112">Вторая команда добавляет открытый ключ к расположению в VirtualMachine07, указанному параметром Path.</span><span class="sxs-lookup"><span data-stu-id="e247c-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="e247c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e247c-113">PARAMETERS</span></span>

### <span data-ttu-id="e247c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e247c-114">-DefaultProfile</span></span>
<span data-ttu-id="e247c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e247c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e247c-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="e247c-116">-KeyData</span></span>
<span data-ttu-id="e247c-117">Определяет кодику с основанием 64 для открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="e247c-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="e247c-118">Вы можете подключиться к виртуальной машине Linux с помощью SSH или ключа, указанного для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="e247c-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="e247c-119">-Path</span><span class="sxs-lookup"><span data-stu-id="e247c-119">-Path</span></span>
<span data-ttu-id="e247c-120">Указывает полный путь к файлу на виртуальной машине, где этот cmdlet хранит общедоступный ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="e247c-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="e247c-121">Если файл уже существует, этот cmdlet будет выдан с ключом.</span><span class="sxs-lookup"><span data-stu-id="e247c-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="e247c-122">-VM</span><span class="sxs-lookup"><span data-stu-id="e247c-122">-VM</span></span>
<span data-ttu-id="e247c-123">Определяет объект виртуальной машины, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e247c-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="e247c-124">Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="e247c-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="e247c-125">Для создания объекта виртуальной машины можно использовать [cmdlet New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="e247c-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="e247c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e247c-126">CommonParameters</span></span>
<span data-ttu-id="e247c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e247c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e247c-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e247c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e247c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e247c-129">INPUTS</span></span>

### <span data-ttu-id="e247c-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="e247c-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e247c-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e247c-131">System.String</span></span>

## <span data-ttu-id="e247c-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e247c-132">OUTPUTS</span></span>

### <span data-ttu-id="e247c-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="e247c-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="e247c-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e247c-134">NOTES</span></span>

## <span data-ttu-id="e247c-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e247c-135">RELATED LINKS</span></span>

[<span data-ttu-id="e247c-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="e247c-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="e247c-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="e247c-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)