---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564987"
---
# <span data-ttu-id="0eb2f-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="0eb2f-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="0eb2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0eb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb2f-103">Возвращает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eb2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0eb2f-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb2f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0eb2f-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb2f-106">Командлет **Get-AzureRmVMDiskEncryptionStatus** получает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="0eb2f-107">Отображается состояние шифрования операционной системы и томов данных.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="0eb2f-108">Помимо состояния шифрования, в нем также отображаются секретный URL-адрес шифрования, URL-адрес ключа шифрования, идентификаторы ресурсов **KeyVaults** , в котором находится ключ шифрования и ключ шифрования для тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="0eb2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0eb2f-109">EXAMPLES</span></span>

### <span data-ttu-id="0eb2f-110">Пример 1: получение состояния шифрования виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0eb2f-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="0eb2f-111">Эта команда возвращает состояние шифрования виртуальной машины с именем VM001.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="0eb2f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0eb2f-112">PARAMETERS</span></span>

### <span data-ttu-id="0eb2f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0eb2f-113">-Name</span></span>
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

### <span data-ttu-id="0eb2f-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb2f-114">-ResourceGroupName</span></span>
<span data-ttu-id="0eb2f-115">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0eb2f-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="0eb2f-116">-VMName</span></span>
<span data-ttu-id="0eb2f-117">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0eb2f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb2f-118">CommonParameters</span></span>
<span data-ttu-id="0eb2f-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb2f-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb2f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb2f-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0eb2f-121">INPUTS</span></span>

### <span data-ttu-id="0eb2f-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="0eb2f-122">None</span></span>
<span data-ttu-id="0eb2f-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0eb2f-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0eb2f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0eb2f-124">OUTPUTS</span></span>

## <span data-ttu-id="0eb2f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="0eb2f-125">NOTES</span></span>

## <span data-ttu-id="0eb2f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0eb2f-126">RELATED LINKS</span></span>

[<span data-ttu-id="0eb2f-127">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0eb2f-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="0eb2f-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="0eb2f-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


