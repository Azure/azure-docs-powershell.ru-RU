---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSet.md
ms.openlocfilehash: 7d2b23c08f7ce910daf87f7cebbea844d5bda6f0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318140"
---
# <span data-ttu-id="85a01-101">Get-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="85a01-101">Get-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="85a01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85a01-102">SYNOPSIS</span></span>
<span data-ttu-id="85a01-103">Получение или перечисление наборов шифрования дисков.</span><span class="sxs-lookup"><span data-stu-id="85a01-103">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="85a01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85a01-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85a01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a01-105">DESCRIPTION</span></span>
<span data-ttu-id="85a01-106">Получение или перечисление наборов шифрования дисков.</span><span class="sxs-lookup"><span data-stu-id="85a01-106">Get or list disk encryption sets.</span></span>

## <span data-ttu-id="85a01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85a01-107">EXAMPLES</span></span>

### <span data-ttu-id="85a01-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85a01-108">Example 1</span></span>
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

<span data-ttu-id="85a01-109">Получить доступ к параметру шифрования диска "enc1"</span><span class="sxs-lookup"><span data-stu-id="85a01-109">Get disk encryption set 'enc1'</span></span>

### <span data-ttu-id="85a01-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="85a01-110">Example 2</span></span>
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

<span data-ttu-id="85a01-111">Получить все наборы шифрования дисков в группе ресурсов "Rg1".</span><span class="sxs-lookup"><span data-stu-id="85a01-111">Get all disk encryption sets in resource group 'rg1'.</span></span>

### <span data-ttu-id="85a01-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="85a01-112">Example 3</span></span>
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

<span data-ttu-id="85a01-113">Получение всех наборов шифрования дисков в подписке.</span><span class="sxs-lookup"><span data-stu-id="85a01-113">Get all disk encryption sets in subscription.</span></span>

## <span data-ttu-id="85a01-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85a01-114">PARAMETERS</span></span>

### <span data-ttu-id="85a01-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a01-115">-DefaultProfile</span></span>
<span data-ttu-id="85a01-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85a01-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a01-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="85a01-117">-Name</span></span>
<span data-ttu-id="85a01-118">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="85a01-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="85a01-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85a01-119">-ResourceGroupName</span></span>
<span data-ttu-id="85a01-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85a01-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85a01-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a01-121">CommonParameters</span></span>
<span data-ttu-id="85a01-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85a01-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a01-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85a01-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a01-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85a01-124">INPUTS</span></span>

### <span data-ttu-id="85a01-125">System. String</span><span class="sxs-lookup"><span data-stu-id="85a01-125">System.String</span></span>

## <span data-ttu-id="85a01-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a01-126">OUTPUTS</span></span>

### <span data-ttu-id="85a01-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="85a01-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="85a01-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="85a01-128">NOTES</span></span>

## <span data-ttu-id="85a01-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85a01-129">RELATED LINKS</span></span>