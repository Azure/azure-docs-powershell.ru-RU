---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azdiskencryptionset.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskEncryptionSet.md
ms.openlocfilehash: 61d8d60925eb1d7e71ca85f92e30516d598facdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519590"
---
# <span data-ttu-id="89b6a-101">New-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="89b6a-101">New-AzDiskEncryptionSet</span></span>

## <span data-ttu-id="89b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="89b6a-103">Создает набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="89b6a-103">Creates a disk encryption set.</span></span>

## <span data-ttu-id="89b6a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89b6a-104">SYNTAX</span></span>

```
New-AzDiskEncryptionSet [-ResourceGroupName] <String> [-Name] <String> [-InputObject] <PSDiskEncryptionSet>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89b6a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="89b6a-106">Создает набор шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="89b6a-106">Creates a disk encryption set.</span></span>

## <span data-ttu-id="89b6a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89b6a-107">EXAMPLES</span></span>

### <span data-ttu-id="89b6a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89b6a-108">Example 1</span></span>
```powershell
PS C:\> $config = New-AzDiskEncryptionSetConfig -Location 'westcentralus' -KeyUrl "https://valut1.vault.azure.net:443/keys/key1/mykey" -SourceVaultId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.KeyVault/vaults/vault1 -IdentityType 'SystemAssigned'
PS C:\> New-AzDiskEncryptionSet -ResourceGroupName 'rg1' -Name 'enc1' -DiskEncryptionSet $config;
```

<span data-ttu-id="89b6a-109">Создает набор шифрования диска с помощью заданного активного ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="89b6a-109">Creates disk encryption set using the given active key in the key vault.</span></span>

## <span data-ttu-id="89b6a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89b6a-110">PARAMETERS</span></span>

### <span data-ttu-id="89b6a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89b6a-111">-AsJob</span></span>
<span data-ttu-id="89b6a-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="89b6a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89b6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b6a-113">-DefaultProfile</span></span>
<span data-ttu-id="89b6a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89b6a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b6a-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="89b6a-115">-InputObject</span></span>
<span data-ttu-id="89b6a-116">Локальный объект набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="89b6a-116">The local object of the disk encryption set.</span></span>

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

### <span data-ttu-id="89b6a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="89b6a-117">-Name</span></span>
<span data-ttu-id="89b6a-118">Имя набора шифрования диска.</span><span class="sxs-lookup"><span data-stu-id="89b6a-118">Name of disk encryption set.</span></span>

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

### <span data-ttu-id="89b6a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89b6a-119">-ResourceGroupName</span></span>
<span data-ttu-id="89b6a-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89b6a-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="89b6a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89b6a-121">-Confirm</span></span>
<span data-ttu-id="89b6a-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b6a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89b6a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89b6a-123">-WhatIf</span></span>
<span data-ttu-id="89b6a-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89b6a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89b6a-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89b6a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89b6a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b6a-126">CommonParameters</span></span>
<span data-ttu-id="89b6a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89b6a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b6a-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89b6a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b6a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89b6a-129">INPUTS</span></span>

### <span data-ttu-id="89b6a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="89b6a-130">System.String</span></span>

### <span data-ttu-id="89b6a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="89b6a-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="89b6a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89b6a-132">OUTPUTS</span></span>

### <span data-ttu-id="89b6a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="89b6a-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskEncryptionSet</span></span>

## <span data-ttu-id="89b6a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89b6a-134">NOTES</span></span>

## <span data-ttu-id="89b6a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89b6a-135">RELATED LINKS</span></span>
