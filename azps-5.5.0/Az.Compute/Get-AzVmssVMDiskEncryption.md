---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244133"
---
# <span data-ttu-id="f5c6e-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="f5c6e-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="f5c6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5c6e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5c6e-103">Состояние шифрования диска ВМ-сообщений в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="f5c6e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5c6e-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5c6e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5c6e-105">DESCRIPTION</span></span>
<span data-ttu-id="f5c6e-106">Состояние шифрования диска для набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="f5c6e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5c6e-107">EXAMPLES</span></span>

### <span data-ttu-id="f5c6e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f5c6e-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="f5c6e-109">Указывает состояние шифрования диска экземпляра VM 1 в наборе масштаба VM (VMSS001), который принадлежит группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="f5c6e-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="f5c6e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5c6e-110">PARAMETERS</span></span>

### <span data-ttu-id="f5c6e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5c6e-111">-DefaultProfile</span></span>
<span data-ttu-id="f5c6e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5c6e-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="f5c6e-113">-ExtensionName</span></span>
<span data-ttu-id="f5c6e-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-114">The extension name.</span></span>
<span data-ttu-id="f5c6e-115">Если этот параметр не задан, по умолчанию используются значения AzureDiskEncryption для windows VMs и AzureDiskEncryptionForLinux для VMs для Linux.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="f5c6e-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f5c6e-116">-InstanceId</span></span>
<span data-ttu-id="f5c6e-117">Определяет ИД экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="f5c6e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5c6e-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5c6e-119">Имя группы ресурсов набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f5c6e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f5c6e-120">-VMScaleSetName</span></span>
<span data-ttu-id="f5c6e-121">Имя набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="f5c6e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5c6e-122">CommonParameters</span></span>
<span data-ttu-id="f5c6e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5c6e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5c6e-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5c6e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5c6e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5c6e-125">INPUTS</span></span>

### <span data-ttu-id="f5c6e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f5c6e-126">System.String</span></span>

## <span data-ttu-id="f5c6e-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5c6e-127">OUTPUTS</span></span>

### <span data-ttu-id="f5c6e-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="f5c6e-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="f5c6e-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5c6e-129">NOTES</span></span>

## <span data-ttu-id="f5c6e-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5c6e-130">RELATED LINKS</span></span>
