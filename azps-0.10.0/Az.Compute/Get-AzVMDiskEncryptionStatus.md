---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 30c8b79d3951f0d557704bc3d0c0ac4919fccac1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911530"
---
# <span data-ttu-id="d6a57-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d6a57-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d6a57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6a57-102">SYNOPSIS</span></span>
<span data-ttu-id="d6a57-103">Возвращает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6a57-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="d6a57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6a57-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6a57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6a57-105">DESCRIPTION</span></span>
<span data-ttu-id="d6a57-106">Командлет **Get-AzVMDiskEncryptionStatus** получает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6a57-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d6a57-107">Отображается состояние шифрования операционной системы и томов данных.</span><span class="sxs-lookup"><span data-stu-id="d6a57-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d6a57-108">Помимо состояния шифрования, в нем также отображаются секретный URL-адрес шифрования, URL-адрес ключа шифрования, идентификаторы ресурсов **KeyVaults** , в котором находится ключ шифрования и ключ шифрования для тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d6a57-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d6a57-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6a57-109">EXAMPLES</span></span>

### <span data-ttu-id="d6a57-110">Пример 1: получение состояния шифрования виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="d6a57-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d6a57-111">Эта команда возвращает состояние шифрования виртуальной машины с именем VM001.</span><span class="sxs-lookup"><span data-stu-id="d6a57-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d6a57-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6a57-112">PARAMETERS</span></span>

### <span data-ttu-id="d6a57-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6a57-113">-DefaultProfile</span></span>
<span data-ttu-id="d6a57-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d6a57-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6a57-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="d6a57-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d6a57-116">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="d6a57-116">The extension publisher name.</span></span> <span data-ttu-id="d6a57-117">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="d6a57-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a57-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d6a57-118">-ExtensionType</span></span>
<span data-ttu-id="d6a57-119">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="d6a57-119">The extension type.</span></span> <span data-ttu-id="d6a57-120">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="d6a57-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6a57-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d6a57-121">-Name</span></span>
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

### <span data-ttu-id="d6a57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6a57-122">-ResourceGroupName</span></span>
<span data-ttu-id="d6a57-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6a57-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d6a57-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d6a57-124">-VMName</span></span>
<span data-ttu-id="d6a57-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d6a57-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d6a57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6a57-126">CommonParameters</span></span>
<span data-ttu-id="d6a57-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6a57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6a57-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6a57-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6a57-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6a57-129">INPUTS</span></span>

### <span data-ttu-id="d6a57-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="d6a57-130">None</span></span>
<span data-ttu-id="d6a57-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d6a57-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6a57-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6a57-132">OUTPUTS</span></span>

### <span data-ttu-id="d6a57-133">Microsoft. Azure. Commands. COMPUTE. extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="d6a57-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d6a57-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6a57-134">NOTES</span></span>

## <span data-ttu-id="d6a57-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6a57-135">RELATED LINKS</span></span>

[<span data-ttu-id="d6a57-136">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d6a57-136">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="d6a57-137">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d6a57-137">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


