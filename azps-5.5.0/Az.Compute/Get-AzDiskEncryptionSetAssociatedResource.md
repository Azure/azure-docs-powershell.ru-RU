---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215788"
---
# <span data-ttu-id="fe9e4-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="fe9e4-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="fe9e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe9e4-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9e4-103">Возвращает список ресурсов, связанных с указанным набором шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="fe9e4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fe9e4-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe9e4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe9e4-105">DESCRIPTION</span></span>
<span data-ttu-id="fe9e4-106">С **помощью cmdlet Get-AzDiskEncryptionSetAssociatedResource** можно получить список ресурсов, связанных с указанным набором шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="fe9e4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fe9e4-107">EXAMPLES</span></span>

### <span data-ttu-id="fe9e4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe9e4-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="fe9e4-109">Он извлекает два ресурса: exampleDisk01 и exampleDisk02, связанные с предоставленным набором шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="fe9e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe9e4-110">PARAMETERS</span></span>

### <span data-ttu-id="fe9e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9e4-111">-DefaultProfile</span></span>
<span data-ttu-id="fe9e4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9e4-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="fe9e4-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="fe9e4-114">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9e4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9e4-115">-ResourceGroupName</span></span>
<span data-ttu-id="fe9e4-116">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-116">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fe9e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9e4-117">CommonParameters</span></span>
<span data-ttu-id="fe9e4-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe9e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9e4-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe9e4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9e4-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9e4-120">INPUTS</span></span>

### <span data-ttu-id="fe9e4-121">System.String</span><span class="sxs-lookup"><span data-stu-id="fe9e4-121">System.String</span></span>

## <span data-ttu-id="fe9e4-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fe9e4-122">OUTPUTS</span></span>

### <span data-ttu-id="fe9e4-123">System.Uri[]</span><span class="sxs-lookup"><span data-stu-id="fe9e4-123">System.Uri[]</span></span>

## <span data-ttu-id="fe9e4-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fe9e4-124">NOTES</span></span>

## <span data-ttu-id="fe9e4-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe9e4-125">RELATED LINKS</span></span>
