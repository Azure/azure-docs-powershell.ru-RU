---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078147"
---
# <span data-ttu-id="58c4b-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="58c4b-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="58c4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58c4b-102">SYNOPSIS</span></span>
<span data-ttu-id="58c4b-103">Получение или перечисление наборов шифрования дисков.</span><span class="sxs-lookup"><span data-stu-id="58c4b-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="58c4b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58c4b-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58c4b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58c4b-105">DESCRIPTION</span></span>
<span data-ttu-id="58c4b-106">Получение или перечисление наборов шифрования дисков.</span><span class="sxs-lookup"><span data-stu-id="58c4b-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="58c4b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58c4b-107">EXAMPLES</span></span>

### <span data-ttu-id="58c4b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="58c4b-108">Example 1</span></span>
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

<span data-ttu-id="58c4b-109">Получить доступ к параметру шифрования диска "enc1"</span><span class="sxs-lookup"><span data-stu-id="58c4b-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="58c4b-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="58c4b-110">Example 2</span></span>
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

<span data-ttu-id="58c4b-111">Получить все наборы шифрования дисков в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="58c4b-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="58c4b-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="58c4b-112">Example 3</span></span>
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

<span data-ttu-id="58c4b-113">Получение всех наборов шифрования дисков в подписке.</span><span class="sxs-lookup"><span data-stu-id="58c4b-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="58c4b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58c4b-114">PARAMETERS</span></span>

### <span data-ttu-id="58c4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58c4b-115">-DefaultProfile</span></span>
<span data-ttu-id="58c4b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58c4b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58c4b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58c4b-117">-Name</span></span>
<span data-ttu-id="58c4b-118">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="58c4b-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="58c4b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58c4b-119">-ResourceGroupName</span></span>
<span data-ttu-id="58c4b-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58c4b-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="58c4b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58c4b-121">CommonParameters</span></span>
<span data-ttu-id="58c4b-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58c4b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58c4b-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58c4b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58c4b-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58c4b-124">INPUTS</span></span>

### <span data-ttu-id="58c4b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="58c4b-125">System.String</span></span>

## <span data-ttu-id="58c4b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58c4b-126">OUTPUTS</span></span>

### <span data-ttu-id="58c4b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="58c4b-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="58c4b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="58c4b-128">NOTES</span></span>

## <span data-ttu-id="58c4b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58c4b-129">RELATED LINKS</span></span>
