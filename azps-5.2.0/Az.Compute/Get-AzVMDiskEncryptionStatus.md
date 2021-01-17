---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406391"
---
# <span data-ttu-id="f8d8b-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="f8d8b-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="f8d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f8d8b-103">Возвращает состояние шифрования виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="f8d8b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8d8b-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8d8b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8d8b-105">DESCRIPTION</span></span>
<span data-ttu-id="f8d8b-106">Для получения состояния шифрования виртуальной машины используется **cmdlet Get-AzVMDiskEncryptionStatus.**</span><span class="sxs-lookup"><span data-stu-id="f8d8b-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="f8d8b-107">Здесь отображается состояние шифрования операционной системы и томов данных.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="f8d8b-108">Помимо состояния шифрования, здесь также отображаются секретный URL-адрес шифрования, URL-адрес ключа шифрования, коды ресурсов **KeyVaults,** в которых указаны ключ шифрования и ключ шифрования операционной системы.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="f8d8b-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8d8b-109">EXAMPLES</span></span>

### <span data-ttu-id="f8d8b-110">Пример 1. Просмотр состояния шифрования виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="f8d8b-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="f8d8b-111">Эта команда получает состояние шифрования виртуальной машины с именем VM001.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="f8d8b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8d8b-112">PARAMETERS</span></span>

### <span data-ttu-id="f8d8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8d8b-113">-DefaultProfile</span></span>
<span data-ttu-id="f8d8b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8d8b-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="f8d8b-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="f8d8b-116">Имя издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-116">The extension publisher name.</span></span> <span data-ttu-id="f8d8b-117">Укажите этот параметр только для переопределения значения по умолчанию microsoft.Azure.Security.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d8b-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="f8d8b-118">-ExtensionType</span></span>
<span data-ttu-id="f8d8b-119">Тип расширения.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-119">The extension type.</span></span> <span data-ttu-id="f8d8b-120">Укажите этот параметр, чтобы переопречить стандартное значение AzureDiskEncryption для VMs Windows и AzureDiskEncryptionForLinux для VMs для Linux.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d8b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8d8b-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d8b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8d8b-122">-ResourceGroupName</span></span>
<span data-ttu-id="f8d8b-123">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d8b-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="f8d8b-124">-VMName</span></span>
<span data-ttu-id="f8d8b-125">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f8d8b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8d8b-126">CommonParameters</span></span>
<span data-ttu-id="f8d8b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8d8b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8d8b-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8d8b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8d8b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8d8b-129">INPUTS</span></span>

### <span data-ttu-id="f8d8b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f8d8b-130">System.String</span></span>

## <span data-ttu-id="f8d8b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8d8b-131">OUTPUTS</span></span>

### <span data-ttu-id="f8d8b-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="f8d8b-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="f8d8b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8d8b-133">NOTES</span></span>

## <span data-ttu-id="f8d8b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8d8b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f8d8b-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f8d8b-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="f8d8b-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="f8d8b-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


