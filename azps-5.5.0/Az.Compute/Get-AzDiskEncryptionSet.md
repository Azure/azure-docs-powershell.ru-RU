---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215793"
---
# <span data-ttu-id="90acd-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="90acd-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="90acd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90acd-102">SYNOPSIS</span></span>
<span data-ttu-id="90acd-103">Получить наборы шифрования дисков или списков.</span><span class="sxs-lookup"><span data-stu-id="90acd-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="90acd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90acd-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90acd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90acd-105">DESCRIPTION</span></span>
<span data-ttu-id="90acd-106">Получить наборы шифрования дисков или списков.</span><span class="sxs-lookup"><span data-stu-id="90acd-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="90acd-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90acd-107">EXAMPLES</span></span>

### <span data-ttu-id="90acd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90acd-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1 -Name enc1;

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="90acd-109">Получить набор шифрования диска (enc1)</span><span class="sxs-lookup"><span data-stu-id="90acd-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="90acd-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="90acd-110">Example 2</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="90acd-111">Получите все наборы шифрования диска в группе ресурсов "rg1".</span><span class="sxs-lookup"><span data-stu-id="90acd-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="90acd-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="90acd-112">Example 3</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSet -ResourceGroupName rg1

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc1
Name              : enc1
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg1
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc2
Name              : enc2
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}

ResourceGroupName : rg2
Identity          : Microsoft.Azure.Management.Compute.Models.EncryptionSetIdentity
ActiveKey         : Microsoft.Azure.Management.Compute.Models.KeyVaultAndKeyReference
PreviousKeys      : {}
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/diskEncryptionSets/enc3
Name              : enc3
Type              : Microsoft.Compute/diskEncryptionSets
Location          : westcentralus
Tags              : {}
```

<span data-ttu-id="90acd-113">Получите все наборы шифрования дисков в подписке.</span><span class="sxs-lookup"><span data-stu-id="90acd-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="90acd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90acd-114">PARAMETERS</span></span>

### <span data-ttu-id="90acd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90acd-115">-DefaultProfile</span></span>
<span data-ttu-id="90acd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90acd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90acd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="90acd-117">-Name</span></span>
<span data-ttu-id="90acd-118">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="90acd-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90acd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90acd-119">-ResourceGroupName</span></span>
<span data-ttu-id="90acd-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90acd-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="90acd-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90acd-121">CommonParameters</span></span>
<span data-ttu-id="90acd-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90acd-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90acd-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90acd-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90acd-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90acd-124">INPUTS</span></span>

### <span data-ttu-id="90acd-125">System.String</span><span class="sxs-lookup"><span data-stu-id="90acd-125">System.String</span></span>

## <span data-ttu-id="90acd-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90acd-126">OUTPUTS</span></span>

### <span data-ttu-id="90acd-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="90acd-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="90acd-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90acd-128">NOTES</span></span>

## <span data-ttu-id="90acd-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90acd-129">RELATED LINKS</span></span>
