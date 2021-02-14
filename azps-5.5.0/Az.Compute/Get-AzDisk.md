---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: f249b20fdae02315511434e4703f741f25b2a295
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244168"
---
# <span data-ttu-id="d25a1-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="d25a1-101">Get-AzDisk</span></span>

## <span data-ttu-id="d25a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d25a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d25a1-103">Свойства управляемого диска.</span><span class="sxs-lookup"><span data-stu-id="d25a1-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="d25a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d25a1-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d25a1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d25a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d25a1-106">Для управляемого диска свойства управляемого диска получает **cmdlet Get-AzDisk.**</span><span class="sxs-lookup"><span data-stu-id="d25a1-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="d25a1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d25a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d25a1-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d25a1-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/Disk01
Name               : Disk01
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d25a1-109">Эта команда получает свойства диска "Диск01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="d25a1-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d25a1-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d25a1-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d25a1-111">Эта команда получает свойства всех дисков группы ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="d25a1-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="d25a1-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d25a1-112">Example 3</span></span>
```
PS C:\> Get-AzDisk

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d25a1-113">Эта команда получает свойства всех дисков подписки.</span><span class="sxs-lookup"><span data-stu-id="d25a1-113">This command gets the properties of all disks under the subscription.</span></span>

### <span data-ttu-id="d25a1-114">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d25a1-114">Example 4</span></span>
```
PS C:\> Get-AzDisk -Name win_OsDisk*

ResourceGroupName  : ResourceGroup01
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:26:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_1
Name               : win1_OsDisk_1
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}

ResourceGroupName  : ResourceGroup02
ManagedBy          :
Sku                : Microsoft.Azure.Management.Compute.Models.DiskSku
Zones              :
TimeCreated        : 6/29/2018 4:27:27 PM
OsType             : Windows
CreationData       : Microsoft.Azure.Management.Compute.Models.CreationData
DiskSizeGB         : 127
EncryptionSettings :
ProvisioningState  : Succeeded
DiskIOPSReadWrite  : 500
DiskMBpsReadWrite  : 100
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup02/providers/Microsoft.Compu
                     te/disks/win1_OsDisk_2
Name               : win1_OsDisk_2
Type               : Microsoft.Compute/disks
Location           : westus2
Tags               : {}
```

<span data-ttu-id="d25a1-115">Эта команда получает свойства всех дисков под именем подписки, начиная с win1_OsDisk.</span><span class="sxs-lookup"><span data-stu-id="d25a1-115">This command gets the properties of all disks under the subscription name starting with win1_OsDisk.</span></span>

## <span data-ttu-id="d25a1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d25a1-116">PARAMETERS</span></span>

### <span data-ttu-id="d25a1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25a1-117">-DefaultProfile</span></span>
<span data-ttu-id="d25a1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d25a1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d25a1-119">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d25a1-119">-DiskName</span></span>
<span data-ttu-id="d25a1-120">Указывает имя диска.</span><span class="sxs-lookup"><span data-stu-id="d25a1-120">Specifies the name of a disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d25a1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25a1-121">-ResourceGroupName</span></span>
<span data-ttu-id="d25a1-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d25a1-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="d25a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25a1-123">CommonParameters</span></span>
<span data-ttu-id="d25a1-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25a1-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d25a1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25a1-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d25a1-126">INPUTS</span></span>

### <span data-ttu-id="d25a1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d25a1-127">System.String</span></span>

## <span data-ttu-id="d25a1-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d25a1-128">OUTPUTS</span></span>

### <span data-ttu-id="d25a1-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="d25a1-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="d25a1-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d25a1-130">NOTES</span></span>

## <span data-ttu-id="d25a1-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d25a1-131">RELATED LINKS</span></span>
