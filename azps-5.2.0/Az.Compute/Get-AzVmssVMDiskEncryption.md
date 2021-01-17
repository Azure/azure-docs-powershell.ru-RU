---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVMDiskEncryption.md
ms.openlocfilehash: 8ff3ad92f976e6a8af9c4a24e143ed3859832d35
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415863"
---
# <span data-ttu-id="39db6-101">Get-AzVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="39db6-101">Get-AzVmssVMDiskEncryption</span></span>

## <span data-ttu-id="39db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39db6-102">SYNOPSIS</span></span>
<span data-ttu-id="39db6-103">Состояние шифрования диска ВМ-сообщений в наборе масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="39db6-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

## <span data-ttu-id="39db6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39db6-104">SYNTAX</span></span>

```
Get-AzVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String>]
 [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39db6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39db6-105">DESCRIPTION</span></span>
<span data-ttu-id="39db6-106">Состояние шифрования диска для набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="39db6-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="39db6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39db6-107">EXAMPLES</span></span>

### <span data-ttu-id="39db6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="39db6-108">Example 1</span></span>
```
PS C:\> Get-AzVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="39db6-109">Указывает состояние шифрования диска экземпляра VM 1 в наборе масштаба VMSS001, который принадлежит группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="39db6-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="39db6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39db6-110">PARAMETERS</span></span>

### <span data-ttu-id="39db6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39db6-111">-DefaultProfile</span></span>
<span data-ttu-id="39db6-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39db6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39db6-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="39db6-113">-ExtensionName</span></span>
<span data-ttu-id="39db6-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="39db6-114">The extension name.</span></span>
<span data-ttu-id="39db6-115">Если этот параметр не указан, по умолчанию используются значения AzureDiskEncryption для windows VMs и AzureDiskEncryptionForLinux для VMs linux.</span><span class="sxs-lookup"><span data-stu-id="39db6-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="39db6-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="39db6-116">-InstanceId</span></span>
<span data-ttu-id="39db6-117">Указывает ИД экземпляра.</span><span class="sxs-lookup"><span data-stu-id="39db6-117">Specifies the instance ID.</span></span>

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

### <span data-ttu-id="39db6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39db6-118">-ResourceGroupName</span></span>
<span data-ttu-id="39db6-119">Имя группы ресурсов набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="39db6-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="39db6-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="39db6-120">-VMScaleSetName</span></span>
<span data-ttu-id="39db6-121">Имя набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="39db6-121">The virtual machine scale set name.</span></span>

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

### <span data-ttu-id="39db6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39db6-122">CommonParameters</span></span>
<span data-ttu-id="39db6-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39db6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39db6-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39db6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39db6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39db6-125">INPUTS</span></span>

### <span data-ttu-id="39db6-126">System.String</span><span class="sxs-lookup"><span data-stu-id="39db6-126">System.String</span></span>

## <span data-ttu-id="39db6-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39db6-127">OUTPUTS</span></span>

### <span data-ttu-id="39db6-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="39db6-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="39db6-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39db6-129">NOTES</span></span>

## <span data-ttu-id="39db6-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39db6-130">RELATED LINKS</span></span>
