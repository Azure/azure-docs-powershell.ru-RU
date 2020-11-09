---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246809"
---
# <span data-ttu-id="65c97-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="65c97-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="65c97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65c97-102">SYNOPSIS</span></span>
<span data-ttu-id="65c97-103">Показывает состояние шифрования диска для виртуальных машин в наборе масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65c97-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="65c97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65c97-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65c97-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c97-105">DESCRIPTION</span></span>
<span data-ttu-id="65c97-106">Показывает состояние шифрования диска для набора шкал виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65c97-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="65c97-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65c97-107">EXAMPLES</span></span>

### <span data-ttu-id="65c97-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="65c97-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="65c97-109">Показывает состояние шифрования диска для экземпляра VM 1 в наборе масштабирования ВИРТУАЛЬНЫХ машин с именем VMSS001, который принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="65c97-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="65c97-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65c97-110">PARAMETERS</span></span>

### <span data-ttu-id="65c97-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c97-111">-DefaultProfile</span></span>
<span data-ttu-id="65c97-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65c97-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c97-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="65c97-113">-ExtensionName</span></span>
<span data-ttu-id="65c97-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="65c97-114">The extension name.</span></span>
<span data-ttu-id="65c97-115">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="65c97-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="65c97-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="65c97-116">-InstanceId</span></span>
<span data-ttu-id="65c97-117">Указывает идентификатор экземпляра.</span><span class="sxs-lookup"><span data-stu-id="65c97-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="65c97-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c97-118">-ResourceGroupName</span></span>
<span data-ttu-id="65c97-119">Имя группы ресурсов для набора шкал виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65c97-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="65c97-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="65c97-120">-VMScaleSetName</span></span>
<span data-ttu-id="65c97-121">Имя множества шкал виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="65c97-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c97-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c97-122">CommonParameters</span></span>
<span data-ttu-id="65c97-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65c97-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c97-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65c97-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c97-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65c97-125">INPUTS</span></span>

### <span data-ttu-id="65c97-126">System. String</span><span class="sxs-lookup"><span data-stu-id="65c97-126">System.String</span></span>

## <span data-ttu-id="65c97-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c97-127">OUTPUTS</span></span>

### <span data-ttu-id="65c97-128">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="65c97-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="65c97-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="65c97-129">NOTES</span></span>

## <span data-ttu-id="65c97-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65c97-130">RELATED LINKS</span></span>