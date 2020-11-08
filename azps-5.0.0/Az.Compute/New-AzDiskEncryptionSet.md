---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246247"
---
# <span data-ttu-id="12053-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="12053-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="12053-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="12053-102">SYNOPSIS</span></span>
<span data-ttu-id="12053-103">Создание набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="12053-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="12053-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="12053-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12053-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12053-105">DESCRIPTION</span></span>
<span data-ttu-id="12053-106">Создание набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="12053-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="12053-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="12053-107">EXAMPLES</span></span>

### <span data-ttu-id="12053-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="12053-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="12053-109">Создание шифрования диска с помощью заданного активного ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="12053-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="12053-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="12053-110">PARAMETERS</span></span>

### <span data-ttu-id="12053-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="12053-111">-AsJob</span></span>
<span data-ttu-id="12053-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="12053-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12053-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12053-113">-DefaultProfile</span></span>
<span data-ttu-id="12053-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="12053-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12053-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12053-115">-InputObject</span></span>
<span data-ttu-id="12053-116">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="12053-116">The local object of the disk encryption set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet
Parameter Sets: (All)
Aliases: DiskEncryptionSet

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12053-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="12053-117">-Name</span></span>
<span data-ttu-id="12053-118">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="12053-118">Name of disk encryption set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskEncryptionSetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12053-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12053-119">-ResourceGroupName</span></span>
<span data-ttu-id="12053-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="12053-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="12053-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12053-121">-Confirm</span></span>
<span data-ttu-id="12053-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="12053-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12053-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12053-123">-WhatIf</span></span>
<span data-ttu-id="12053-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="12053-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12053-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="12053-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12053-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12053-126">CommonParameters</span></span>
<span data-ttu-id="12053-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="12053-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12053-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12053-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12053-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="12053-129">INPUTS</span></span>

### <span data-ttu-id="12053-130">System. String</span><span class="sxs-lookup"><span data-stu-id="12053-130">System.String</span></span>

### <span data-ttu-id="12053-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="12053-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="12053-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="12053-132">OUTPUTS</span></span>

### <span data-ttu-id="12053-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="12053-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="12053-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="12053-134">NOTES</span></span>

## <span data-ttu-id="12053-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12053-135">RELATED LINKS</span></span>
