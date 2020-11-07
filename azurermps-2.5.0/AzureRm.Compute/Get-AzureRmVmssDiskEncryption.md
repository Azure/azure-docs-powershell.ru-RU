---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssdiskencryption
schema: 2.0.0
ms.openlocfilehash: c49fc472c6cc3693145487bdfe7488d0eabfe237
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913913"
---
# <span data-ttu-id="fe4dc-101">Get-AzureRmVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fe4dc-101">Get-AzureRmVmssDiskEncryption</span></span>

## <span data-ttu-id="fe4dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe4dc-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4dc-103">Показывает состояние шифрования диска для набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-103">Shows the disk encryption status of a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe4dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe4dc-104">SYNTAX</span></span>

```
Get-AzureRmVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe4dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe4dc-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4dc-106">Показывает состояние шифрования диска для набора масштабирования виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="fe4dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe4dc-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4dc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe4dc-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="fe4dc-109">Показывает состояние шифрования диска, установленное для набора виртуальных машин с именем VMSS001, которое принадлежит группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="fe4dc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe4dc-110">PARAMETERS</span></span>

### <span data-ttu-id="fe4dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4dc-111">-DefaultProfile</span></span>
<span data-ttu-id="fe4dc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe4dc-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="fe4dc-113">-ExtensionName</span></span>
<span data-ttu-id="fe4dc-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-114">The extension name.</span></span>
<span data-ttu-id="fe4dc-115">Если этот параметр не указан, используются значения по умолчанию AzureDiskEncryption для ВМ и AzureDiskEncryptionForLinux для виртуальных машин Linux.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4dc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4dc-116">-ResourceGroupName</span></span>
<span data-ttu-id="fe4dc-117">Имя группы ресурсов для набора шкал виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="fe4dc-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4dc-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fe4dc-118">-VMScaleSetName</span></span>
<span data-ttu-id="fe4dc-119">Имя множества шкал виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-119">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4dc-120">CommonParameters</span></span>
<span data-ttu-id="fe4dc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe4dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4dc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4dc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe4dc-123">INPUTS</span></span>

### <span data-ttu-id="fe4dc-124">System. String</span><span class="sxs-lookup"><span data-stu-id="fe4dc-124">System.String</span></span>

## <span data-ttu-id="fe4dc-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe4dc-125">OUTPUTS</span></span>

### <span data-ttu-id="fe4dc-126">Microsoft. Azure. Commands. COMPUTE. Models. PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="fe4dc-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="fe4dc-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe4dc-127">NOTES</span></span>

## <span data-ttu-id="fe4dc-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe4dc-128">RELATED LINKS</span></span>

