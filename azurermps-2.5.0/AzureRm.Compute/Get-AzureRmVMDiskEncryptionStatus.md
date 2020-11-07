---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913395"
---
# <span data-ttu-id="3cde0-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="3cde0-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="3cde0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3cde0-102">SYNOPSIS</span></span>
<span data-ttu-id="3cde0-103">Возвращает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cde0-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cde0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3cde0-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cde0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cde0-105">DESCRIPTION</span></span>
<span data-ttu-id="3cde0-106">Командлет **Get-AzureRmVMDiskEncryptionStatus** получает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cde0-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="3cde0-107">Отображается состояние шифрования операционной системы и томов данных.</span><span class="sxs-lookup"><span data-stu-id="3cde0-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="3cde0-108">Помимо состояния шифрования, в нем также отображаются секретный URL-адрес шифрования, URL-адрес ключа шифрования, идентификаторы ресурсов **KeyVaults** , в котором находится ключ шифрования и ключ шифрования для тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3cde0-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="3cde0-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3cde0-109">EXAMPLES</span></span>

### <span data-ttu-id="3cde0-110">Пример 1: получение состояния шифрования виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="3cde0-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="3cde0-111">Эта команда возвращает состояние шифрования виртуальной машины с именем VM001.</span><span class="sxs-lookup"><span data-stu-id="3cde0-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="3cde0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3cde0-112">PARAMETERS</span></span>

### <span data-ttu-id="3cde0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cde0-113">-DefaultProfile</span></span>
<span data-ttu-id="3cde0-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cde0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cde0-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="3cde0-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="3cde0-116">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="3cde0-116">The extension publisher name.</span></span> <span data-ttu-id="3cde0-117">Указывайте этот параметр только для переопределения значения по умолчанию Microsoft. Azure. Security.</span><span class="sxs-lookup"><span data-stu-id="3cde0-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="3cde0-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="3cde0-118">-ExtensionType</span></span>
<span data-ttu-id="3cde0-119">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="3cde0-119">The extension type.</span></span> <span data-ttu-id="3cde0-120">Укажите этот параметр для переопределения значения по умолчанию "AzureDiskEncryption" для виртуальных машин и "AzureDiskEncryptionForLinux" для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="3cde0-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="3cde0-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3cde0-121">-Name</span></span>
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

### <span data-ttu-id="3cde0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cde0-122">-ResourceGroupName</span></span>
<span data-ttu-id="3cde0-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cde0-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3cde0-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="3cde0-124">-VMName</span></span>
<span data-ttu-id="3cde0-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3cde0-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="3cde0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cde0-126">CommonParameters</span></span>
<span data-ttu-id="3cde0-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3cde0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cde0-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cde0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cde0-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3cde0-129">INPUTS</span></span>

### <span data-ttu-id="3cde0-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="3cde0-130">None</span></span>
<span data-ttu-id="3cde0-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="3cde0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3cde0-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cde0-132">OUTPUTS</span></span>

### <span data-ttu-id="3cde0-133">Microsoft. Azure. Commands. COMPUTE. extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="3cde0-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="3cde0-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="3cde0-134">NOTES</span></span>

## <span data-ttu-id="3cde0-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cde0-135">RELATED LINKS</span></span>

[<span data-ttu-id="3cde0-136">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3cde0-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="3cde0-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="3cde0-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


