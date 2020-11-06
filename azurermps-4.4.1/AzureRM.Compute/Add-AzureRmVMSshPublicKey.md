---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: 24c97e73728dab656a1d9fe3283e4eba6aae4ea2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557940"
---
# <span data-ttu-id="b1b48-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="b1b48-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="b1b48-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b1b48-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b48-103">Добавляет открытые ключи для SSH для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1b48-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b48-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b1b48-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b48-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1b48-105">DESCRIPTION</span></span>
<span data-ttu-id="b1b48-106">Командлет **Add-AzureRmVMSshPublicKey** добавляет открытые ключи, которые можно использовать для подключения к виртуальной машине по защищенной оболочке (SSH).</span><span class="sxs-lookup"><span data-stu-id="b1b48-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="b1b48-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b1b48-107">EXAMPLES</span></span>

### <span data-ttu-id="b1b48-108">Пример 1: Добавление открытого ключа для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="b1b48-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="b1b48-109">Первая команда получает виртуальную машину с именем VirtualMachine07 с помощью командлета **Get-AzureRmVM** .</span><span class="sxs-lookup"><span data-stu-id="b1b48-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="b1b48-110">Команда сохраняет виртуальную машину в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b1b48-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="b1b48-111">Вторая команда добавляет открытый ключ в расположение в VirtualMachine07, которое указывает параметр path.</span><span class="sxs-lookup"><span data-stu-id="b1b48-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="b1b48-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b1b48-112">PARAMETERS</span></span>

### <span data-ttu-id="b1b48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b48-113">-DefaultProfile</span></span>
<span data-ttu-id="b1b48-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1b48-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="b1b48-115">-KeyData</span></span>
<span data-ttu-id="b1b48-116">Задает базовую кодировку 64 для открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b1b48-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="b1b48-117">Вы можете подключаться к виртуальной машине с помощью SSH или ключа, который указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="b1b48-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="b1b48-118">-Path</span><span class="sxs-lookup"><span data-stu-id="b1b48-118">-Path</span></span>
<span data-ttu-id="b1b48-119">Задает полный путь к файлу на виртуальной машине, в которой этот командлет хранит открытый ключ SSH.</span><span class="sxs-lookup"><span data-stu-id="b1b48-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="b1b48-120">Если файл уже существует, этот командлет добавляет ключ к файлу.</span><span class="sxs-lookup"><span data-stu-id="b1b48-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="b1b48-121">-VM</span><span class="sxs-lookup"><span data-stu-id="b1b48-121">-VM</span></span>
<span data-ttu-id="b1b48-122">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b1b48-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="b1b48-123">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b48-123">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="b1b48-124">Вы можете использовать командлет [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1b48-124">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="b1b48-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b48-125">CommonParameters</span></span>
<span data-ttu-id="b1b48-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b1b48-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b48-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b48-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b48-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b1b48-128">INPUTS</span></span>

## <span data-ttu-id="b1b48-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1b48-129">OUTPUTS</span></span>

## <span data-ttu-id="b1b48-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="b1b48-130">NOTES</span></span>

## <span data-ttu-id="b1b48-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1b48-131">RELATED LINKS</span></span>

[<span data-ttu-id="b1b48-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b1b48-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b1b48-133">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="b1b48-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
