---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssDiskEncryption.md
ms.openlocfilehash: 5f47931817cf640349cd4d3226fe8ffa4819d259
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399175"
---
# <span data-ttu-id="26232-101">Get-AzVmssDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="26232-101">Get-AzVmssDiskEncryption</span></span>

## <span data-ttu-id="26232-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26232-102">SYNOPSIS</span></span>
<span data-ttu-id="26232-103">Состояние шифрования диска для набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="26232-103">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="26232-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26232-104">SYNTAX</span></span>

```
Get-AzVmssDiskEncryption [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [[-ExtensionName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26232-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26232-105">DESCRIPTION</span></span>
<span data-ttu-id="26232-106">Состояние шифрования диска для набора масштаба VM.</span><span class="sxs-lookup"><span data-stu-id="26232-106">Shows the disk encryption status of a VM scale set.</span></span>

## <span data-ttu-id="26232-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26232-107">EXAMPLES</span></span>

### <span data-ttu-id="26232-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26232-108">Example 1</span></span>
```
PS C:\> Get-AzVmssDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="26232-109">Состояние шифрования диска набора VM с именем VMSS001, который принадлежит группе ресурсов "Группа001".</span><span class="sxs-lookup"><span data-stu-id="26232-109">Shows the disk encryption status of the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="26232-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26232-110">PARAMETERS</span></span>

### <span data-ttu-id="26232-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26232-111">-DefaultProfile</span></span>
<span data-ttu-id="26232-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26232-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26232-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="26232-113">-ExtensionName</span></span>
<span data-ttu-id="26232-114">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="26232-114">The extension name.</span></span>
<span data-ttu-id="26232-115">Если этот параметр не указан, по умолчанию используются значения AzureDiskEncryption для windows VMs и AzureDiskEncryptionForLinux для VMs linux.</span><span class="sxs-lookup"><span data-stu-id="26232-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

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

### <span data-ttu-id="26232-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26232-116">-ResourceGroupName</span></span>
<span data-ttu-id="26232-117">Имя группы ресурсов набора масштаба виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="26232-117">Resource group name of the virtual machine scale set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26232-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="26232-118">-VMScaleSetName</span></span>
<span data-ttu-id="26232-119">Имя набора масштаба виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="26232-119">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26232-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26232-120">CommonParameters</span></span>
<span data-ttu-id="26232-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26232-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26232-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26232-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26232-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26232-123">INPUTS</span></span>

### <span data-ttu-id="26232-124">System.String</span><span class="sxs-lookup"><span data-stu-id="26232-124">System.String</span></span>

## <span data-ttu-id="26232-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26232-125">OUTPUTS</span></span>

### <span data-ttu-id="26232-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="26232-126">Microsoft.Azure.Commands.Compute.Models.PSVmssDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="26232-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26232-127">NOTES</span></span>

## <span data-ttu-id="26232-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26232-128">RELATED LINKS</span></span>
